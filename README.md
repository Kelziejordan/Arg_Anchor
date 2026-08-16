# ARG Anchor

> *"Describe what you want to build. ARG organizes the work, governs execution, verifies progress, and helps you recover when something breaks."*

## What is ARG?

**ARG** is a recoverable AI build workspace that helps users move from intent to working software through structured planning, governed execution, visible verification, and checkpoint-based continuity.

ARG is designed for a common problem in AI-assisted building: generation is easy, but preserving progress, recovering from bad changes, and keeping work aligned with the actual objective is much harder. ARG addresses that by combining guided workflow structure with recovery and verification.

## Core value

ARG is built around five practical outcomes:

- **Reduce project chaos:** turn rough intent into a structured workflow.
- **Preserve progress:** maintain checkpointed continuity instead of fragile one-shot generation.
- **Govern execution:** route meaningful actions through visible rules, checks, and progression boundaries.
- **Verify outcomes:** distinguish generated output from work that has actually been validated.
- **Support both simple and advanced users:** keep the default experience clean while preserving deeper visibility for technical builders.

## Product workflow

ARG organizes work through a consistent lifecycle:

1. **Intake:** capture what the user wants to build.
2. **Scoping:** reduce ambiguity and identify constraints.
3. **Planning:** create a structured execution path.
4. **Execution:** perform bounded work steps.
5. **Verification:** confirm whether the intended result was actually achieved.
6. **Workspace:** keep the project in a usable, recoverable state ready for continuation.

## Why ARG is different

Many AI build tools focus on output generation. ARG focuses on **continuity**.

That means:

- changes should be visible,
- progress should be recoverable,
- failed steps should not erase project momentum,
- and completion should require verification rather than assumption.

ARG is intended to function as both:

- a guided build workspace for users, and
- a structured internal delivery environment for higher-trust software and architecture work.

## Modes

### Operator Mode

Operator Mode keeps the workspace low-noise and forward-moving. It emphasizes the current objective, the next best action, and simple recovery paths without overwhelming the user with internal detail.

### Builder Mode

Builder Mode exposes deeper execution detail, policy surfaces, diagnostics, verification records, and system context for users who need tighter control over the workflow.

## Recovery and trust

ARG treats recovery as a product feature, not a background utility.

Users should be able to:

- inspect meaningful checkpoints,
- understand what changed,
- review verification results,
- return to a known good state,
- and continue work without losing the wider project context.

## Portability

ARG is designed to remain portable and self-hostable.

- Run locally with Node.js.
- Containerize with Docker.
- Keep control over where your project lives.
- Avoid unnecessary platform lock-in.

## Run locally

```bash
npm install
npm run dev
```

Then open:

```text
http://localhost:3000
```

## Build for production

```bash
npm run build
npm run start
```

## Docker

```dockerfile
FROM node:20-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build
EXPOSE 3000
CMD ["npm", "run", "start"]
```

## Governance docs

- **ACR.md** â€” Architectural boundaries and non-bypass constraints.
- **AOC.md** â€” Workflow constitution, progression rules, and operating expectations.
- **ARS.md** â€” Runtime expectations for validation, observability, recovery, and execution behavior.

## Current direction

ARG should continue evolving toward a recoverable, governed AI development workspace where progress is structured, evidence is visible, and failed changes are recoverable without sacrificing speed.
---

## Credits

* **Primary Creator & Operator:** Kelsea Ziegler ([kelseaziegler@gmail.com](mailto:kelseaziegler@gmail.com))
* **Co-Architect Partner:** Many AI's including Google Gemini, ChatGPT, Perplexity, CoPilot and others. 
* **Status:** Operational Constitution v1.0 RC2
