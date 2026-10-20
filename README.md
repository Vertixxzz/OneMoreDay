# One More Day

**A research-focused diploma project on independent game development, supported by the design of an original 2D narrative indie game.**

> **Project status:** Research, requirements, and architecture documentation are in progress. The repository currently focuses on analysis and design; a complete playable build is not yet provided here.

## Project overview

The diploma topic is **“Independent Game Development as a Catalyst for the Evolution of the Video Game Industry.”** The research examines how independent developers contribute to changes in game design and production, and considers the creative, technical, and distribution constraints that shape independent projects.

The practical project, **One More Day**, is planned as a 2D top-down narrative game about April, an art student whose cancer diagnosis changes her relationships and everyday life. Its story explores different ways of responding to uncertainty and maintaining—or withdrawing from—connections with other people. The choices are not intended as a simple moral test, and neither narrative direction promises an easy or guaranteed outcome.

### Problem statement

Independent game development can enable distinctive creative approaches, but developers also face constraints involving resources, production practices, discoverability, and distribution. The project studies this tension and applies the findings to the design of a small narrative game.

### Research question

How does independent game development contribute to the evolution of the video game industry, and which lessons from independent production and narrative games can inform the design of *One More Day*?

### Aim and objectives

**Aim:** To investigate the role of independent game development in the evolution of the video game industry and apply the findings to the design and planned evaluation of *One More Day*.

**Objectives:**

1. Review and critically analyse relevant academic literature on independent game development.
2. Compare selected indie games and narrative games using consistent criteria.
3. Compare candidate technologies and justify the initial technical direction.
4. Define functional and non-functional requirements and acceptance criteria for *One More Day*.
5. Document the proposed system architecture and key user scenarios.
6. Prepare a verification and evaluation plan for a future prototype.

### Target users

The intended audience for the game is players interested in narrative-driven 2D indie games, character-focused storytelling, and meaningful dialogue choices. Potential players will also be consulted to help validate the relevance of the concept and inform requirements.

### Scope

The planned game focuses on top-down 2D exploration, character interaction, dialogue, narrative progression, music, and choices affecting how the story unfolds. The immediate pre-defense deliverable is a coherent research and design package, not a complete game release. Implementation details may be refined after the technical approach is validated with a small prototype.

## Project documentation

The `docs/` directory contains editable Markdown documents and Word copies for review. **Markdown is the preferred source for version-controlled edits; keep the corresponding `.docx` copy synchronised when it is needed for review or submission.**

| Document | Purpose |
|---|---|
| [Project Proposal](docs/project-proposal.md) · [Word copy](docs/project-proposal.docx) | Problem, aim, objectives, scope, and expected outcomes |
| [Source Bibliography](docs/source-bibliography.md) · [Word copy](docs/source-bibliography.docx) | Annotated bibliography of the publications used in the research |
| [Literature Review](docs/literature-review.md) · [Word copy](docs/literature-review.docx) | Critical synthesis of research on independent game development |
| [Independent Games Comparison](docs/indie-games-comparison.md) · [Word copy](docs/indie-games-comparison.docx) | Comparison of selected indie games against consistent criteria |
| [Narrative Games Comparison](docs/narrative-games-comparison.md) · [Word copy](docs/narrative-games-comparison.docx) | Comparison of narrative games relevant to the practical project |
| [Technology Comparison](docs/technology-comparison.md) · [Word copy](docs/technology-comparison.docx) | Preliminary comparison of engines, dialogue tools, and related technical choices |
| [Requirements Specification](docs/requirements-specification.md) · [Word copy](docs/requirements-specification.docx) | Functional/non-functional requirements, priorities, and acceptance criteria |
| [Evaluation Plan](docs/evaluation-plan.md) · [Word copy](docs/evaluation-plan.docx) | Planned tests, metrics, test conditions, and participant feedback |
| [Documentation index](docs/README.md) | Guide to the document set and file conventions |

### Architecture diagrams

Editable Mermaid source files and PNG previews are stored in [`docs/architecture/`](docs/architecture/):

- [System Context diagram source](docs/architecture/system-context.mmd) · [PNG preview](docs/architecture/system-context.png)
- [Use Case diagram source](docs/architecture/use-case.mmd) · [PNG preview](docs/architecture/use-case.png)
- [Component diagram source](docs/architecture/component-diagram.mmd) · [PNG preview](docs/architecture/component-diagram.png)

## Initial technology direction

The current candidate stack is **Unity 6 + C#**, with **Yarn Spinner** as the leading dialogue-tool candidate. These are preliminary decisions rather than final commitments; they are documented in the technology comparison and should be validated with a small vertical slice. Music is currently planned to be composed in FL Studio.

## Current status and next steps

### Prepared

- Project proposal and scope documentation.
- Annotated bibliography and critical literature review.
- Comparisons of independent games, narrative games, and candidate technologies.
- Initial requirements and acceptance criteria.
- Draft System Context, Use Case, and Component diagrams with editable sources.
- Verification and evaluation plan.

### Remaining work / validation

- Record 3–5 discussions with potential players (or document a substantive agreement with an actual client), and show how findings affect requirements.
- Add a structured literature-analysis matrix covering each publication's method, findings, limitations, and relevance to the project.
- Create mockups of the key user scenarios or link a prototype.
- Set up and link the YouTrack project; prioritise tasks and record owners, expected outcomes, acceptance criteria, and deadlines.
- Obtain and document the supervisor's feedback and the resulting revisions.
- Maintain meaningful commits, link relevant changes to tasks and reviews, and create the required pre-defense tag when the submission snapshot is ready.

Items in this list are not represented as completed until supporting evidence is added to the repository.

## Build, run, and test

A runnable game build and complete implementation setup instructions are not currently provided in this repository. Once a runnable prototype is committed, this section should specify the required Unity version, how to open the project, input controls, and how to execute any available tests.

## Repository structure

```text
.
├── README.md
└── docs/
    ├── README.md
    ├── project-proposal.md / project-proposal.docx
    ├── source-bibliography.md / source-bibliography.docx
    ├── literature-review.md / literature-review.docx
    ├── indie-games-comparison.md / indie-games-comparison.docx
    ├── narrative-games-comparison.md / narrative-games-comparison.docx
    ├── technology-comparison.md / technology-comparison.docx
    ├── requirements-specification.md / requirements-specification.docx
    ├── evaluation-plan.md / evaluation-plan.docx
    └── architecture/
        ├── system-context.mmd / system-context.png
        ├── use-case.mmd / use-case.png
        └── component-diagram.mmd / component-diagram.png
```

This outline describes the expected documentation layout. If filenames differ in the repository, update the links above to match the actual paths.

## Development practice

Use descriptive commits for coherent changes. Keep documentation and diagram sources under version control, use separate branches for substantial changes, and link implementation or documentation work to the relevant task and review where applicable. Do not commit passwords, API keys, private user data, or other confidential information.
