# One More Day

**Diploma research project:** *Independent Game Development as a Catalyst for the Evolution of the Video Game Industry*  
**Practical project:** An original 2D top-down narrative indie game.

> **Current stage:** Research and pre-production. The repository contains the research, requirements, architecture drafts, and evaluation plan. A complete playable build is not yet included.

## Project Overview

The research examines how independent game development contributes to changes in game design and production, while considering the creative, technical, economic, and distribution constraints faced by independent developers.

The practical project, **One More Day**, is planned as a 2D top-down narrative game about April, an art student whose cancer diagnosis changes her everyday life and relationships. The story explores different responses to uncertainty and connection. Its final choice is not intended as a simple moral test, and neither branch promises recovery.

## Research Question

How does independent game development contribute to the evolution of the video game industry, and which lessons from independent production and narrative games can inform the design and evaluation of *One More Day*?

## Aim

To investigate the role of independent game development in the evolution of the video game industry and apply the findings to the design and planned evaluation of *One More Day*.

## Project Scope

The planned experience focuses on:

- 2D top-down exploration and character interaction;
- dialogue and a three-chapter narrative;
- a consequential choice with distinct follow-up branches;
- original music composed for the project;
- a small, testable scope suitable for independent development.

The immediate pre-defense deliverable is a coherent research and design package, not a complete commercial release. Technology choices remain provisional until validated through a small vertical slice.

## Documentation

Markdown files are the version-controlled source of truth. Word copies are provided for academic review in the [Word documents folder](https://drive.google.com/drive/folders/1ctH97rbreNvqTOoONxiDKU9G49EQ-rkG?usp=sharing).

| Document | Purpose |
|---|---|
| [Project Proposal](docs/project-proposal.md) | Problem, aim, objectives, methodology, scope, and expected outcomes |
| [Source Bibliography](docs/source-bibliography.md) | Annotated bibliography of selected publications |
| [Literature Review](docs/literature-review.md) | Critical synthesis and structured publication-analysis matrix |
| [User Research](docs/user-research.md) | Preliminary interview findings, evidence-to-requirements mapping, and limitations |
| [Independent Games Comparison](docs/indie-games-comparison.md) | Cross-genre comparison of selected independent games |
| [Narrative Games Comparison](docs/narrative-games-comparison.md) | Comparison of narrative indie games relevant to the practical project |
| [Technology Comparison](docs/technology-comparison.md) | Preliminary comparison of engines, dialogue tools, state management, and music software |
| [Requirements Specification](docs/requirements-specification.md) | Functional and non-functional requirements, priorities, and acceptance criteria |
| [Evaluation Plan](docs/evaluation-plan.md) | Planned functional tests, evaluation metrics, and data-recording procedures |
| [Documentation Index](docs/README.md) | Index of project documents and maintenance conventions |

## Architecture

Editable Mermaid sources and PNG previews are stored in [`docs/architecture/`](docs/architecture/):

- [System Context](docs/architecture/system-context.mmd) · [Preview](docs/architecture/system-context.png)
- [Use Case](docs/architecture/use-case.mmd) · [Preview](docs/architecture/use-case.png)
- [Component Diagram](docs/architecture/component-diagram.mmd) · [Preview](docs/architecture/component-diagram.png)

## Preliminary Technology Direction

The current candidates are **Unity 6 + C#** and **Yarn Spinner** for dialogue. These are preliminary choices, not claims of completed integration. The project plans to validate the engine, dialogue flow, narrative branch state, and music playback through a minimal vertical slice. Original music is planned in FL Studio.

## Current Status

### Prepared

- Project proposal and scope.
- Annotated bibliography and critical literature review with a publication-analysis matrix.
- Comparisons of independent games, narrative games, and candidate technologies.
- Preliminary user-research report based on three asynchronous text discussions.
- Requirements with priorities, acceptance criteria, and traceability.
- Draft System Context, Use Case, and Component diagrams with editable sources.
- Verification and evaluation plan with 12 functional test cases and proposed metrics.
- YouTrack project and task hierarchy maintained separately.

### Remaining Validation and Pre-Defense Work

- Validate the specific *One More Day* concept and final-choice framing with potential players; the current interviews did not evaluate the concept directly.
- Create mockups for the key user scenarios or link a prototype.
- Add the YouTrack project URL and ensure tasks, owners, priorities, milestones, and risks are documented.
- Record supervisor feedback and document any resulting changes when feedback is received.
- Keep meaningful commits and link changes to tasks where practical.
- Create the required pre-defense tags when the corresponding repository snapshots are ready.

## Build, Run, and Test

A runnable build and complete implementation setup instructions are not currently provided. Once a prototype is available, this section should specify the Unity version, dependencies, setup steps, controls, and test execution procedure.
