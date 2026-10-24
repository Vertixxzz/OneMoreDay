# One More Day

**Diploma research project:** *Independent Game Development as a Catalyst for the Evolution of the Video Game Industry*  
**Practical project:** An original 2D top-down narrative indie game.

> **Current stage:** Research and pre-production, with an initial Unity main-menu demonstration. The repository contains the research and design documentation, requirements, architecture drafts, and evaluation plan. A complete playable build is not yet included.

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

The immediate pre-defense deliverable is a coherent research and design package, not a complete commercial release. The core gameplay loop and dialogue/branching systems still require implementation and validation through a small vertical slice.

## Documentation

Markdown files are the version-controlled source of truth. Word copies are provided for academic review in the [Word documents folder](https://drive.google.com/drive/folders/1ctH97rbreNvqTOoONxiDKU9G49EQ-rkG?usp=sharing).

| Document | Purpose |
|---|---|
| [Project Proposal](docs/project-proposal.md) | Problem, aim, objectives, methodology, scope, and expected outcomes |
| [Source Bibliography](docs/source-bibliography.md) | Annotated bibliography of selected publications |
| [Literature Review](docs/literature-review.md) | Critical synthesis and structured publication-analysis matrix |
| [User Research](docs/user-research.md) | Findings from six exploratory interviews, evidence-to-requirements mapping, and limitations |
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

## Project Management

Project planning, task tracking, priorities, and progress monitoring are managed through YouTrack.

- **YouTrack project:** [OneMoreDay — Project Initiation](https://onemoreday.youtrack.cloud/projects/ONE/issues/ONE-1/Project-Initiation)
- **Task tracking:** The project contains 53 tasks covering initiation, research, design, implementation, testing, evaluation, and thesis preparation. The task set includes both completed work and planned work; it should not be read as a claim that every task is complete.

## Technology Direction

Unity 6 is being used for initial UI and audiovisual prototyping, with C# intended for implementation. Yarn Spinner remains a candidate dialogue tool and has not yet been validated in an integrated gameplay vertical slice. Original music production in FL Studio is planned as part of the game's audio work.

## Current Status

### Prepared

- Project proposal and research scope.
- Annotated bibliography and critical literature review covering 15 publications, including a publication-analysis matrix.
- Comparative analyses of independent games, narrative games, and candidate technologies.
- Exploratory user research based on six asynchronous text-based interviews: three primarily from player perspectives and three from development or industry perspectives.
- Functional and non-functional requirements with priorities, acceptance criteria, and traceability.
- Draft System Context, Use Case, and Component diagrams, with editable Mermaid sources and PNG previews.
- Evaluation plan containing 12 planned functional test cases and proposed evaluation measures.
- YouTrack project and task hierarchy.
- An initial Unity main-menu demonstration with the existing background art, menu UI, animated rain, ambient audio, and rain sound effects. This establishes an initial visual and audiovisual direction; it is not a complete playable game.

### Limitations and Remaining Work

- UX work is preliminary. The main menu has an initial visual direction, while the core gameplay view, character interaction and dialogue screens, and the Engagement/Withdrawal choice screens need further design and implementation.
- A complete playable build and a tested vertical slice are not yet available in the repository.
- The Unity main-menu demonstration has been recorded, but the repository does not yet provide a complete, reproducible Unity project or a runnable game build.
- The project is being developed individually, which limits the time available for parallel implementation, testing, and refinement. Scope control and staged delivery are therefore important project-management priorities.

### Next Steps

- Design and implement the core gameplay loop, dialogue, character interactions, and the final narrative choice in a small vertical slice.
- Run the planned functional tests, fix defects, and document results and limitations.
- Finalise the consolidated pre-defense report and ensure it matches the repository snapshot tagged `prob-period-1`.

## Build, Run, and Test

A complete runnable build and reproducible Unity setup instructions are not currently provided in this repository. The recorded main-menu demonstration shows an initial audiovisual prototype only. Once the Unity project and a playable vertical slice are added, this section should document the Unity version, dependencies, setup steps, controls, and test execution procedure. The evaluation plan defines intended tests but does not report completed test results.
