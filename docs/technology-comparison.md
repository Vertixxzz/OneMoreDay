# Technology Comparison for *One More Day*

**Project:** *One More Day* — a 2D top-down narrative indie game  
**Document status:** Preliminary comparison for pre-defense  
**Decision status:** Proposed choices; to be validated before implementation  
**Last reviewed:** 20 October 2026

## 1. Purpose and scope

This document compares development technologies and production tools that may be used to create *One More Day*. The comparison is based on the current project requirements rather than on a general ranking of game-development tools.

The planned game requires a 2D top-down environment, player movement and interaction, dialogue, progression through three chapters, a consequential choice in Chapter III, visibly different narrative branches, and original music. The project is intended to remain feasible for individual development and to produce a demonstrable prototype.

The comparison covers four decisions:

1. game engine;
2. dialogue and narrative scripting system;
3. narrative-state and branch-management approach;
4. music-production software.

The first three affect how the playable application is implemented. The music-production decision concerns the supporting content-creation workflow rather than the game's runtime architecture, and is therefore evaluated separately.

## 2. Evaluation method and criteria

The options are compared against project-specific criteria. The ratings below are **preliminary qualitative judgments**, not benchmark results or measurements from a completed prototype. They should be revisited if the requirements change or a short technical test produces contrary evidence.

For the game-engine comparison, the criteria are:

- **2D workflow fit:** support for a top-down 2D game, scenes/rooms, sprites, animation and UI.
- **Narrative and code integration:** suitability for integrating dialogue, player interaction, state changes and custom gameplay logic.
- **Individual-development feasibility:** ability to reach a small playable prototype without unnecessary implementation overhead.
- **Maintainability and learning resources:** clarity of project structure, documentation and available learning material.
- **Licensing and distribution constraints:** how licensing terms may affect a student project and any future release. Current terms must be checked before distribution.

No single criterion is sufficient by itself. A feature-rich engine is not automatically the best choice for a small narrative game, and low software cost does not remove the need to consider learning time, integrations and project scope.

## 3. Decision A — Game engine

### 3.1 Alternatives

| Criterion | Unity 6 | Godot | GameMaker |
|---|---|---|---|
| 2D workflow fit | Strong 2D workflow, including sprites, Tilemaps and 2D physics. | Dedicated 2D renderer and physics, with 2D-oriented tools such as TileMaps and animation systems. | Strong focus on 2D workflows, including rooms, sprites, tilesets, sequences and a debugger. |
| Programming approach | C# gameplay code and Unity scene/component model. | GDScript or C#; the choice should account for the intended target platforms and available integrations. | GML code or visual programming. |
| Integration with the proposed dialogue option | Yarn Spinner has documented Unity integration, including a Dialogue Runner and commands that can call game code. | Unity-specific Yarn Spinner integration should not be assumed to be available unchanged; a Godot implementation would need its own integration decision. | A custom dialogue implementation or a verified GameMaker-specific solution would be needed; Unity packages cannot be assumed to work. |
| Individual-development feasibility | Suitable, but the editor and ecosystem can introduce more concepts than a small 2D game strictly needs. | Suitable for a small 2D project; a new engine workflow and any dialogue integration would need to be learned and verified. | Suitable for 2D games; using GML would make this a different language/workflow from the planned C# approach. |
| Licensing and distribution | Unity Personal eligibility and software terms depend on the current Unity terms and applicable financial thresholds; verify before release. | The engine is MIT-licensed; distribution requires retaining relevant licence notices. | The official licensing page distinguishes non-commercial/free use from commercial licensing and export options; check the current terms for the intended release. |
| Main project-specific advantage | Aligns with the current provisional C# plan and provides a documented path to integrate Yarn Spinner. | Dedicated 2D feature set and permissive open-source licence. | A focused 2D workflow with integrated room, sprite and sequence tools. |
| Main project-specific concern | Potentially more engine overhead than necessary; licensing eligibility must be checked. | The exact dialogue integration and C# workflow must be verified rather than assumed. | GML and dialogue architecture may add migration or integration work relative to the current C# plan. |

**Official references:** [Unity 2D documentation](https://docs.unity.com/en-us/engine/6000.0/manual/unity2d); [Godot 2D documentation](https://docs.godotengine.org/en/4.5/tutorials/2d/index.html); [Godot licence](https://godotengine.org/license/); [GameMaker features](https://gamemaker.io/en/features); [GameMaker licensing and export options](https://gamemaker.io/en/get); [Unity Editor Software Terms](https://unity.com/legal/editor-terms-of-service/software).

### 3.2 Preliminary assessment

**Unity 6 is the provisional recommendation**, not because it is objectively superior to the alternatives for all 2D games, but because it matches the current project plan: C# is already the intended gameplay language, and Yarn Spinner documents an integration path for Unity. This reduces the number of unverified integration decisions in the initial prototype.

Godot remains a credible alternative, particularly if avoiding a proprietary engine and using a dedicated 2D workflow become higher priorities. GameMaker remains technically plausible for a 2D title, but its GML-based workflow would be a larger departure from the current C# plan.

This recommendation should be reopened if the Unity setup proves disproportionately complex, if required packages create compatibility problems, or if project constraints favour a different licensing model.

## 4. Decision B — Dialogue and narrative scripting

The game requires dialogue presentation, player choices, chapter progression, and a final choice that selects one of two distinct narrative branches.

| Criterion | Yarn Spinner | Ink | Custom C# dialogue system |
|---|---|---|---|
| Primary strength | Dialogue authoring and connecting narrative commands to in-game behaviour. | Branching interactive writing, with a scripting language designed for choices and recombining story flow. | Complete control over data structures, UI and game-specific behaviour. |
| Authoring and revision | Dialogue is kept in dedicated script files, which can be revised separately from most gameplay code. | Story flow is written in `.ink` files and can be played/tested through the Inky workflow. | Dialogue may be stored in code, data files or a custom format; the project must design and maintain that format. |
| Connection to gameplay | Unity integration provides a Dialogue Runner and command handlers to invoke game functionality. | Official Unity integration provides a C# runtime and Unity tooling. | Direct integration is possible, but all dialogue parsing, presentation, choice handling and testing tools must be implemented or assembled. |
| Complex branching | Supports choices and variables; the complexity should be tested against the planned narrative. | Particularly suitable for branching and recombining interactive narratives. | Can support any required structure, but complexity and testing effort are the team's responsibility. |
| Initial implementation effort | Low-to-moderate if the documented Unity workflow matches the project. | Low-to-moderate for story authoring, plus integration and state coordination. | Higher, because core dialogue features would be built for this project. |
| Main risk | Integration commands and persistent game state must be designed clearly; selecting Yarn does not automatically solve architecture. | The project must define how Ink story state, Unity gameplay state and scene progression stay consistent. | Scope can expand into building a dialogue engine rather than building the game. |

**Official references:** [Yarn Spinner: Dialogue Runner](https://docs.yarnspinner.dev/components/dialogue-runner); [Yarn Spinner: Commands and Functions](https://docs.yarnspinner.dev/yarn-spinner-for-unity/creating-commands-functions); [inkle/ink repository and Unity integration overview](https://github.com/inkle/ink).

### 4.1 Preliminary assessment

**Yarn Spinner is the provisional recommendation** because the current engine plan is Unity and the game's requirements include dialogue-driven interactions that can call gameplay behaviour. Its command integration is relevant to triggering interactions or requesting state changes without hard-coding all dialogue content into gameplay scripts.

Ink is a strong alternative if the writing develops into a more densely branching narrative with frequent recombination and story-state logic. A custom C# solution is possible, but it is difficult to justify for the first prototype unless the requirements prove too specific for the available dialogue tools. Building custom dialogue infrastructure would increase effort without directly demonstrating the project's main narrative objective.

The choice should be validated with a small dialogue scene before the full script is authored.

## 5. Decision C — Narrative state and branch management

Dialogue scripting and state management are related but different decisions. A dialogue tool can present choices, but the game still needs a clear rule for recording the selected branch and using it consistently across scenes.

| Approach | Advantages | Disadvantages | Assessment for *One More Day* |
|---|---|---|---|
| Keep all state inside the dialogue tool | Fast to begin; variables and choices remain near the story text. | Gameplay systems may become tightly coupled to the dialogue implementation; cross-scene use and debugging may be less clear if state grows. | Viable for a very small linear sequence, but potentially restrictive if branch state affects scenes and interactions. |
| Use a small central C# narrative-state manager, with Yarn Spinner or Ink for dialogue | Separates story text from application state; gives one place to record the current chapter, selected final branch and any essential flags; easier to inspect and test. | Requires an explicit interface between the dialogue tool and game code. | **Preferred provisional approach.** It fits the current C# plan and the need to preserve the Chapter III decision through the selected branch. |
| Use scene-specific or hard-coded branch flags | Can appear simple for a tiny demonstration. | State can become duplicated or inconsistent as scenes are added; changes become harder to trace and regression-test. | Not recommended except for a disposable experiment. |

### 5.1 Proposed minimum state

The initial implementation should store only what the requirements need:

- current chapter or narrative sequence;
- selected Chapter III branch (`engagement` or `withdrawal`), once chosen;
- any additional flags only when a documented scene or interaction requires them.

The selected branch should be set at the choice point and read by subsequent branch-specific content. Persistent save/load is not a prerequisite for the first vertical slice unless the project scope later makes it necessary. The architecture should not introduce a general-purpose quest or relationship system without evidence that the game needs one.

## 6. Supporting production-tool decision — Music software

Original music is part of the game concept. The selected workstation only needs to support the user's composition workflow and reliable export of audio assets suitable for integration into the game.

| Criterion | FL Studio | REAPER | LMMS |
|---|---|---|---|
| Main workflow | Pattern-based composition, arrangement, instruments, effects and mixing. | Broad audio/MIDI recording, editing, arranging, mixing and rendering workflow. | Free, open-source music production with synthesis, samples, instruments, effects and MIDI support. |
| Operating systems | Windows and macOS, according to the official feature page. | Windows, macOS and Linux. | Windows, macOS and Linux. |
| Export workflow | Official manual documents rendering to formats including WAV, MP3, OGG and FLAC. | Official documentation describes rendering to a wide range of audio formats and detailed render settings. | The manual documents export to WAV and OGG. |
| Main project-specific advantage | Fits the user's stated preference and can be used to compose and export original tracks. | Flexible recording/editing and strong rendering control; also available on Linux. | Free and open source, with a straightforward cost profile. |
| Main project-specific concern | Licence and edition terms should be checked for the installed version; the workflow may be more extensive than the game's audio needs. | More customisable than needed for simple soundtrack production; familiarity may be a factor. | The user may need to learn a different workflow; verify output quality and plug-in needs with a short test. |

**Official references:** [FL Studio features](https://www.image-line.com/fl-studio/features); [FL Studio export manual](https://www.image-line.com/fl-studio-learning/fl-studio-online-manual/html/fformats_save_export.htm); [REAPER features and supported platforms](https://www.reaper.fm/about.php); [LMMS](https://www.lmms.io/); [LMMS export manual](https://docs.lmms.io/user-manual/jp_2/4-production/4.5-exporting-a-song).

### 6.1 Preliminary assessment

**FL Studio is the proposed choice** because it matches the user's preference and provides an export workflow suitable for producing original music files. This is a workflow-fit decision rather than a claim that FL Studio is technically superior to REAPER or LMMS.

The required output for the game is a rendered audio asset, such as WAV, that can be imported and played in the engine. The editable DAW project and any third-party instruments or samples should be managed separately, with their licences checked where applicable. The initial integration test should confirm that the exported file plays at the intended scene and has no clipping or unexpected playback behaviour.

## 7. Summary of preliminary decisions

| Decision | Proposed option | Rationale | Confidence before validation |
|---|---|---|---|
| Game engine | Unity 6 | Aligns with the planned C# workflow and has a documented 2D pipeline. | Medium |
| Dialogue system | Yarn Spinner | Documented Unity integration and a command mechanism for invoking game behaviour. | Medium |
| Narrative state | Small central C# state manager, coordinated with the dialogue system | Avoids scattering branch state across scenes and separates narrative content from application state. | Medium |
| Music-production tool | FL Studio | Matches the user's preference and supports rendering audio assets for integration. | Medium-high for workflow preference; technical integration still to be tested |

These are provisional design decisions. They are not claims that the tools have already been installed, integrated or tested in the project.

## 8. Validation plan: minimal technical vertical slice

Before committing to the stack as final, validate the most important integration risks in a minimal test scene. The purpose is to discover whether the selected tools work together for this project, not to build a complete chapter or produce finished art.

| Test | Procedure | Acceptance criterion | Evidence to keep |
|---|---|---|---|
| V-01: 2D engine workflow | Create one small top-down test scene with a controllable player and one interactable object. | The scene runs and the interaction can be triggered reliably. | Engine version, short capture or screenshots, any setup issues. |
| V-02: Dialogue integration | Trigger one dialogue sequence and present at least one player choice. | Dialogue advances and the selected option is available to game code. | Dialogue source file and a brief test note. |
| V-03: Branch state | Make each final-choice option in separate test runs and route to distinct follow-up dialogue or scenes. | Each choice consistently selects the matching branch; the two branches differ in at least one predefined content item. | Test cases and observed outcomes. |
| V-04: Music integration | Export one short original track from the selected DAW and play it in the test scene. | The audio loads and plays as intended without clipping or an integration error. | Export settings, audio format and test result. |
| V-05: Reproducibility | Record the versions and steps needed to open and run the test project. | Another session can repeat the test from the documented setup without relying on undocumented local state. | Setup notes and repository commit. |

The test results should update this comparison. If a tool creates an integration obstacle, the decision should be reconsidered rather than retained merely because it was the initial preference.

## 9. Limitations

This is a requirements-based desk comparison using official documentation and product information. It is not a controlled benchmark, a usability study, or a comparison of finished prototypes. Features and licensing terms can change, so version-specific documentation and current terms should be rechecked when the tools are installed and before any public release.

The assessment prioritizes the requirements and constraints of *One More Day*. It should not be generalized into a claim that one engine, narrative tool or DAW is best for indie games as a whole.

## 10. References

1. Unity Technologies. *2D game development*. https://docs.unity.com/en-us/engine/6000.0/manual/unity2d
2. Godot Engine. *2D documentation (4.5)*. https://docs.godotengine.org/en/4.5/tutorials/2d/index.html
3. Godot Engine. *License*. https://godotengine.org/license/
4. GameMaker. *Features*. https://gamemaker.io/en/features
5. GameMaker. *Licensing and export options*. https://gamemaker.io/en/get
6. Unity Technologies. *Unity Editor Software Terms*. https://unity.com/legal/editor-terms-of-service/software
7. Yarn Spinner. *Dialogue Runners and Systems*. https://docs.yarnspinner.dev/components/dialogue-runner
8. Yarn Spinner. *Commands and Functions*. https://docs.yarnspinner.dev/yarn-spinner-for-unity/creating-commands-functions
9. inkle. *Ink: interactive narrative scripting language and Unity integration*. https://github.com/inkle/ink
10. Image-Line. *FL Studio features*. https://www.image-line.com/fl-studio/features
11. Image-Line. *Exporting audio and MIDI*. https://www.image-line.com/fl-studio-learning/fl-studio-online-manual/html/fformats_save_export.htm
12. Cockos. *REAPER: features and technical information*. https://www.reaper.fm/about.php
13. LMMS. *Official project site*. https://www.lmms.io/
14. LMMS. *Exporting a song*. https://docs.lmms.io/user-manual/jp_2/4-production/4.5-exporting-a-song
