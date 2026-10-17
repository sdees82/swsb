# Set up Ring Builder

Read [BEFORE-YOU-BEGIN.md](BEFORE-YOU-BEGIN.md), [VERSION.md](VERSION.md) and the [authority preflight](teaching/templates/authority-preflight.md) first. The first implementation is a practice rep in Chapter 3. Follow [the complete task sequence](teaching/tasks/README.md).

You author Markdown guidance, give the agent bounded assignments, and review the application and evidence it returns. The agent scaffolds the project and creates or edits application code, configuration, package files and tests. You never need to create a TSX file manually or paste an implementation into the project.

This companion contains Markdown and assets only. The files named below are either Markdown you own or expected outputs for the agent to produce. No app, source code, scripts, package manifest, lockfile or decoder implementation is supplied.

## Prepare the Markdown guidance

Open an empty Ring Builder working folder in your agent tool. Create its root AGENTS.md using [the starting briefing](starter/AGENTS.md), and save [the first-preview spec](teaching/docs/specs/first-preview.md) as docs/specs/first-preview.md. You can ask the agent to draft these Markdown files, then edit and approve their content. Keep feature requirements separate from the whole-project briefing.

Use one authoritative briefing. If you use Claude Code, a root CLAUDE.md can import it with `@AGENTS.md`, as the inspected source project does. Confirm that your tool received the guidance in a fresh session. Preserve any framework guidance generated during setup.

Read [MODEL-INSPECTION.md](MODEL-INSPECTION.md). Ask the agent to inspect the model GLB and matching JSON, then return the actual mesh/material names, surface mappings and runtime dependencies. Review those findings and save the relevant context in your Markdown briefing. Ask the agent to copy the supplied assets into the working project as part of the authorized setup; no manual asset-placement or code-copying exercise is required.

## Give the agent the fixed stack

| Dependency | Recorded version |
| --- | --- |
| Next.js | 16.2.9 |
| React and React DOM | 19.2.4 |
| TypeScript | 5.9.3 |
| React Three Fiber | 9.6.1 |
| drei | 10.7.7 |
| three.js | 0.184.0 |
| three-stdlib | 2.36.1 |
| Zustand | 5.0.14 |
| Tailwind and Tailwind PostCSS | 4.3.1 |
| ESLint / eslint-config-next | 9.39.4 / 16.2.9 |

Use npm. Next.js requires Node >=20.9.0; preparation used Node 24.11.1. The recorded type packages are @types/node 20.19.43, @types/react 19.2.17, @types/react-dom 19.2.3 and @types/three 0.184.1. The validated test setup uses Jest 30.4.2, jest-environment-jsdom 30.4.1, @types/jest 30.0.0, React Testing Library 16.3.2 and jest-dom 6.9.1. Use the installed Next.js next/jest.js configuration factory to transform the TypeScript and TSX tests, with jsdom and jest-dom setup. The source project also records ts-jest 29.4.11; a separate ts-jest transformer is not required by the validated Next.js setup.

The agent initializes package.json, installs the appropriate recorded dependencies, establishes TypeScript/Next.js/Tailwind/ESLint configuration and retains npm's generated lockfile. These top-level versions were installed in an isolated project during this editorial revision. Lint, type checking, 21 tests and the webpack production build passed. The local browser pass covered the five feature loops, with physical-device and screen-reader coverage still open; see CLEAN-ROOM-VALIDATION.md. Once the agent has established the reader project's lockfile, it uses npm ci for reproducible installation. There is no supplied package file to copy.

## First-preview assignment

After reviewing the plan, authorize the local setup and implementation for this bounded task:

> Read AGENTS.md and docs/specs/first-preview.md. Inspect the ring and record its actual structure before implementation. Use the fixed stack in the briefing. Copy the companion assets into this project, install the required dependencies, and create the configuration, package scripts and minimal application needed to display and inspect the ring at /builder.
>
> Implement PV-01–05, including loading, camera inspection, model failure/retry and WebGL fallback. Keep player personalization, logos and material controls for later milestones. Create the application files and any relevant checks yourself. Return the changed paths, the commands actually run, the observed result and remaining gaps. Do not commit, push, publish or change external systems.

The expected agent outputs include app/builder/page.tsx, the small loader/scene and inspection camera. These paths tell you where to inspect the agent's result; they are not files you must hand-code. [MILESTONES.md](MILESTONES.md) gives the full sequence.

During the preview, ask the agent to establish dev, lint, type-check and build scripts. In Chapter 5 loop 1, it creates test and verify with the first real test suite. Their underlying commands in the source project are next dev, eslint, tsc --noEmit, jest --no-coverage and next build. A webpack production build passed during preparation; the agent may use Next.js's --webpack option and should record that choice. Tests count as evidence only after the agent has created the relevant test implementation.

Have the agent start the app and return its local address, normally http://localhost:3000/builder. Inspect the actual preview yourself and compare it with the spec. Review its diff and check output; request another agent-run check or a correction when the evidence is incomplete. Record acceptance and the next action in Markdown.

## Decoder setup belongs to the agent

The GLB uses KHR_draco_mesh_compression. After installing three.js, the agent obtains the glTF decoder builds from node_modules/three/examples/jsm/libs/draco/gltf. The inspected 0.184.0 package contains draco_decoder.js, draco_decoder.wasm and draco_wasm_wrapper.js there.

The agent creates public/draco, copies those installed dependency files there and configures the renderer to request /draco/. No decoder implementation is bundled in this companion. Applicable Apache-2.0 Draco and MIT three.js notices must accompany any later distribution of that dependency code. The installed three.js Draco README identifies its glTF builds and upstream license. The optional Node validator in the original source project uses draco3d 1.5.7; it is unnecessary just to display the browser model.

The agent serves /models/championship-ring.glb over local HTTP and keeps its four JSON assets together. Version 87870ccab314 matches the supplied GLB. It must account for a deployment base path if the project later introduces one.

## Direct each later milestone through Markdown

Author or adapt the supplied player, logo and material specs in docs/specs. Ask the agent to review a small implementation plan, create the required source and tests, then return evidence before continuing. Controls, setText, sanitizeText and their tests are agent outputs of the personalization milestone, not assumed starting files.

You can add the scoped Markdown rule once the relevant code exists, and ask the agent to install or check the supplied Markdown skills in the tool's project discovery location. The aligned source project uses .agents/skills and .claude/skills entries. Test discovery separately from skill syntax; neither installs tools nor grants permissions.

Use the logo fixtures and verification recipe to inspect the agent's result. The agent creates any browser automation and test fixtures it needs beyond the supplied input assets. Your direct interaction with the app, review decisions and Markdown records remain part of the learning workflow.

## Combined verification contract

At Chapter 5 loop 1, the agent must add `test: jest --no-coverage` and `verify: npm run lint && npm run type-check && npm test -- --runInBand && npm run build` to package.json. The underlying dev/build commands are `next dev --webpack` and `next build --webpack`; lint is `eslint .` and type-check is `tsc --noEmit`. It runs verify after establishing the first real suite and after later loops. Browser interaction and human acceptance remain separate. A missing or empty suite cannot be represented as passing.
