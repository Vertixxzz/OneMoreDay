# One More Day — Requirements Specification and Narrative Structure

**Project type:** 2D top-down narrative indie game  
**Protagonist:** April, an art university student  
**Narrative structure:** Three chapters with a consequential choice in Chapter III  
**Game engine:** Unity 6 — provisional selection  
**Dialogue system:** Yarn Spinner — provisional selection  
**Original music:** Produced in FL Studio  
**Document status:** Draft for pre-defense  
**Version:** 0.3  
**Revision date:** 24 October 2026

> **Related document:** The detailed verification procedures, test cases, result fields, and player-evaluation method are maintained in [`evaluation-plan.md`](evaluation-plan.md). That file is the single source of truth for test-case IDs T-01–T-12; this specification maps requirements to those IDs without redefining the test cases.

## 1. Project Overview

One More Day is an original 2D top-down narrative game about April, a kind, sociable art university student whose ordinary life is disrupted by a cancer diagnosis.

The story begins by establishing April's everyday life, including her relationships with family and friends, her studies, and her personal identity beyond her illness. After the diagnosis, the narrative moves into a hospital environment, where April must confront uncertainty, changes in her relationships, and the emotional consequences of her condition.

In the third chapter, the player makes a consequential choice between two ways of spending April's remaining time:

- **Engagement:** April attempts to continue interacting with people and maintaining connections with her former life, despite the possibility of dying.
- **Withdrawal:** April chooses to disengage from other people and spends her remaining time largely isolated in bed.

The choice leads to different scenes, emotional experiences, and depictions of April's relationships with the people around her. Neither branch provides a guaranteed recovery or a conventional happy ending.

The central design objective is to make the player's choice meaningful through its emotional and narrative consequences rather than through a promise that the player can change the protagonist's medical outcome.

The precise ending scenes, dialogue, and character reactions remain to be developed.

## 2. Narrative Structure

### Chapter I — Before the Diagnosis

**Narrative purpose:** Establish April as a person with a life, relationships, interests, and plans of her own.

The first chapter introduces April's ordinary environment before the diagnosis. The player should have opportunities to encounter elements of her university life, interact with relevant characters, and learn about the relationships that matter to her.

**Intended narrative elements**

- Introduction to April and her everyday personality.
- Establishment of family and friendship relationships.
- Introduction to her art university environment.
- Opportunities to explore the setting and interact with selected characters or objects.
- Foreshadowing, if appropriate, without revealing the entire central conflict too early.

**Chapter completion criterion:** The player can identify April's basic personality, important relationships, and aspects of her life that become relevant after the diagnosis.

### Chapter II — The Diagnosis

**Narrative purpose:** Introduce the central conflict and show how April's life changes.

April is diagnosed with cancer, and the story moves into the hospital environment. The chapter explores her experience of uncertainty and the changing dynamics between her and the people who care about her.

The illness should not erase April's identity or reduce every character interaction to discussion of cancer. Her personality, relationships, and individual reactions remain central to the story.

**Intended narrative elements**

- Presentation of the diagnosis and its emotional impact.
- Transition into the hospital setting.
- Interactions with selected family members, friends, or other relevant characters.
- Changes in routine, environment, and opportunities for interaction.
- Development of the emotional conflict that motivates the final choice.

**Chapter completion criterion:** The player understands the central conflict and the emotional context of the decision presented in Chapter III.

### Chapter III — How to Spend the Remaining Time

**Narrative purpose:** Give the player agency over April's response to her situation without presenting the choice as a means of guaranteeing survival.

The player chooses between continued engagement with other people and withdrawal from social interaction.

#### Branch A — Engagement

April chooses to keep interacting with the world around her.

**Potential narrative consequences include:**

- Additional conversations with family and friends.
- Opportunities to maintain or revisit meaningful relationships.
- Scenes that show April attempting to preserve parts of her former identity and routine.
- Moments of connection, difficulty, vulnerability, or unresolved conflict.

This branch is not a guaranteed happy ending. Continued engagement does not reverse the diagnosis or promise recovery.

#### Branch B — Withdrawal

April chooses to disengage from other people and spend her remaining time largely in bed.

**Potential narrative consequences include:**

- Fewer interactions with other characters.
- Scenes emphasizing isolation, silence, and the passage of time.
- Different reactions from family and friends.
- Opportunities to explore what withdrawal means for April and the people around her.

This branch must not automatically frame April as selfish, weak, or morally wrong. Its purpose is to depict a different response to a difficult situation, not to punish the player for making the choice.

**Shared narrative principle**

Both branches concern the same underlying uncertainty and the possibility that April may die. The branches differ in the experiences presented, the interactions available, and the way relationships are depicted.

The game does not promise that either decision will produce a better medical outcome. Its narrative agency comes from allowing the player to influence how April spends her remaining time.

**Chapter completion criterion:** The selected branch presents a distinct set of scenes and relationship experiences, and the player can recognize the consequences of the decision without being told that one option is objectively correct.

## 3. Project Scope

**In scope**

- A playable 2D top-down narrative prototype.
- Three sequential narrative chapters.
- Exploration of relevant environments.
- Interaction with selected characters and objects.
- Dialogue and narrative event presentation.
- A consequential choice in Chapter III.
- Two distinct narrative branches with different scenes and relationship experiences.
- Original music produced in FL Studio and integrated into Unity.
- Version-controlled project files and technical documentation.
- A testable vertical slice demonstrating the core experience.

**Out of scope for the initial prototype**

- A complete commercial-scale game.
- Online multiplayer or network-dependent features.
- A complex combat system unless subsequently justified by the design.
- A medical simulation or detailed representation of cancer treatment.
- A guaranteed survival outcome or a conventional happy ending unlocked by the player's choice.
- Extensive branching throughout all three chapters before the core narrative structure is validated.

## 4. Functional Requirements

**Priority definitions**

- **Must:** Essential for the core prototype.
- **Should:** Important but potentially deferrable.
- **Could:** Optional enhancement.

| ID | Requirement | Priority | Acceptance criteria |
|---|---|---|---|
| FR-01 | The game shall launch into a playable state. | Must | The application launches in the target test environment and reaches the initial scene without a blocking error. |
| FR-02 | The game shall use a 2D top-down presentation. | Must | The prototype includes a top-down scene in which the player can navigate or interact using the implemented controls. |
| FR-03 | The narrative shall be divided into three chapters. | Must | The documented narrative structure identifies Chapters I, II, and III, and the implemented sequence follows that order. |
| FR-04 | Chapter I shall introduce April's life before the diagnosis. | Must | The opening presents April and at least one relevant aspect of her ordinary life or relationships. During narrative review, the opening is checked against the Chapter I completion criterion. |
| FR-05 | Chapter II shall introduce the diagnosis and hospital setting. | Must | The implemented narrative communicates the central diagnosis and establishes the resulting change in setting and circumstances. The sequence is reviewed against the Chapter II completion criterion. |
| FR-06 | The game shall support in-game dialogue or equivalent narrative presentation. | Must | A complete test dialogue sequence can be triggered, displayed, and advanced without becoming stuck. |
| FR-07 | The player shall be able to interact with relevant characters or objects. | Must | At least one documented interaction can be completed using the intended input method. |
| FR-08 | Chapter III shall present the consequential choice between engagement and withdrawal. | Must | The player can select either option, and the game records the selected branch. |
| FR-09 | The engagement branch shall present distinct narrative content. | Must | Selecting engagement leads to at least one scene or interaction that differs from the corresponding withdrawal-branch content. |
| FR-10 | The withdrawal branch shall present distinct narrative content. | Must | Selecting withdrawal leads to at least one scene or interaction that differs from the corresponding engagement-branch content. |
| FR-11 | The selected branch shall affect the depiction of April's relationships. | Must | The branches contain at least one documented difference in character interaction, dialogue, or relationship presentation. |
| FR-12 | The game shall not promise that the final choice guarantees April's recovery. | Must | Neither branch displays or implies that a cure is guaranteed as a reward for selecting that option. |
| FR-13 | The game shall play original music integrated into Unity. | Must | At least one original track produced in FL Studio plays in its intended scene without an integration error. |
| FR-14 | Audio behavior shall respond appropriately to narrative or scene transitions. | Should | Music starts, stops, or transitions according to the documented behavior for the tested sequence. |
| FR-15 | The game shall provide enough feedback for the player to understand basic interactions. | Should | A first-time tester can identify the intended interaction method, or the usability evaluation records the confusion and the improvement needed. |
| FR-16 | The project shall provide a documented method for verifying core requirements. | Must | Each Must requirement is linked to a verification method. For every test that is executed, the evaluation record includes its outcome and available context/evidence; unexecuted tests are marked as not tested rather than assumed to have passed. |

## 5. Non-Functional Requirements

| ID | Requirement | Priority | Acceptance criteria |
|---|---|---|---|
| NFR-01 | The prototype shall be stable enough for a demonstration. | Must | The predefined demonstration scenario can be completed without a crash or blocking defect. |
| NFR-02 | The project shall use maintainable code and identifiable game components. | Should | Core interaction, dialogue handling, chapter progression, and audio behavior can be located and modified without relying on one monolithic script. |
| NFR-03 | Narrative text shall be readable. | Must | Text is not clipped or obscured at the selected target resolution and remains readable throughout the test scenario. |
| NFR-04 | Player controls shall be understandable. | Must | Controls are documented or communicated in-game and support completion of the test scenario. |
| NFR-05 | Audio shall play without unintended clipping or disruptive behavior. | Must | The tested track plays at an appropriate level without unintended playback, clipping, or transition defects. |
| NFR-06 | The project shall be reproducible from version-controlled source files. | Should | The repository documents the engine version and dependencies and provides instructions for opening the project. |
| NFR-07 | The project shall remain feasible for independent development. | Must | Scope and implementation priorities are documented, and optional features do not block the core narrative experience. |
| NFR-08 | The narrative shall avoid presenting the two choices as a simple moral test. | Must | Narrative review finds that neither branch is required to be rewarded as morally superior. Potentially judgmental framing is explicitly considered during review, particularly in the withdrawal branch. |
| NFR-09 | The project shall support evaluation of narrative and usability outcomes. | Must | The evaluation plan defines test scenarios, metrics, recording procedures, and limitations. Where player evaluation is conducted, results and sample limitations are documented. |

## 6. Narrative State and Branch Management

The implementation must preserve the player's Chapter III decision throughout the selected branch.

**Minimum narrative state**

- Current chapter.
- Current narrative sequence or scene.
- Selected Chapter III branch.
- Any additional state variables required by the implemented dialogue or interactions.

**Branch behavior**

1. The player progresses through the shared narrative structure.
2. The game presents the final choice at the documented point in Chapter III.
3. The selected option is stored in the narrative state.
4. The game loads the corresponding branch content.
5. Branch-specific scenes and dialogue are presented.
6. The branch reaches its intended ending sequence.

If saving and loading are implemented, the selected branch must remain consistent after loading a saved game. Persistent saves are not mandatory for the initial vertical slice unless required by the final design.

## 7. Technology Requirements and Constraints

The following technology choices are provisional and must be validated against the implementation.

| Component | Proposed technology | Purpose |
|---|---|---|
| Game engine | Unity 6 | 2D scenes, input, interactions, and application builds |
| Dialogue system | Yarn Spinner | Organizing dialogue and implementing narrative choices |
| Programming language | C# | Gameplay logic, interaction handling, and state management |
| Music production | FL Studio | Creating and exporting original music |
| Version control | Git with GitHub or another Git hosting service | Tracking development and preserving project history |

The final selection of the dialogue system should account for the need to trigger scenes, preserve the selected branch, and coordinate narrative state with gameplay logic.

## 8. Verification and Evaluation

Verification and evaluation serve different purposes.

**Verification** checks whether the implemented features satisfy their specified requirements. **Evaluation** examines whether the resulting experience communicates the intended narrative and provides meaningful player agency.

The detailed test procedures, test-case register, result fields, and evidence-recording instructions are maintained in [`evaluation-plan.md`](evaluation-plan.md). Test-case IDs T-01–T-12 are defined there and are not duplicated in this document. The requirements traceability matrix in Section 9 identifies the relevant test IDs or review method for each requirement.

For each executed test, the evaluation record should identify the test ID, date, build or commit, test environment and input method where relevant, outcome, and available evidence or defect notes. A test that has not yet been executed must be recorded as not tested; a planned test is not evidence that a requirement has passed.

Narrative evaluation should explore whether players can describe April beyond her diagnosis, understand the difference between the two final choices, recognize how the choice affects the experience, and interpret the decision as a personal response rather than a simple good-versus-bad test. It should also examine whether the audiovisual presentation supports the intended emotional tone.

The initial player-evaluation plan targets a small, documented convenience sample appropriate to the project's resources. Findings must be reported as preliminary when the sample is small. They must not be generalized to all players or used to claim that one narrative approach is universally effective. Participant procedure, prompts, metrics, care considerations, and limitations are specified in `evaluation-plan.md`.

## 9. Requirements Traceability Matrix

The test IDs in this matrix refer to the canonical test register in [`evaluation-plan.md`](evaluation-plan.md). Review methods without a test ID are identified explicitly.

| Requirement | Evidence | Verification method / canonical test ID |
|---|---|---|
| FR-01 | Runnable build and initial scene | Launch test, T-01 |
| FR-02 | Top-down scene and implemented controls | Navigation test, T-02 |
| FR-03 | Chapter structure and implemented sequence | Chapter progression test, T-04; inspect narrative flow |
| FR-04 | Opening scene and ordinary-life/relationship content | Narrative framing, T-07; review against Chapter I completion criterion |
| FR-05 | Diagnosis sequence and hospital setting | Chapter progression, T-04; narrative framing, T-07 |
| FR-06 | Dialogue sequence | Dialogue test, T-03 |
| FR-07 | Character/object interaction | Navigation, T-02; interaction feedback, T-10 |
| FR-08 | Recorded branch state | Branch selection, T-05 |
| FR-09 | Engagement-branch scene or interaction | Branch distinction, T-06 |
| FR-10 | Withdrawal-branch scene or interaction | Branch distinction, T-06 |
| FR-11 | Differences in relationship presentation | Branch distinction, T-06; inspect the branch content checklist |
| FR-12 | Dialogue, scenes, and branch framing | Narrative framing, T-07 |
| FR-13 | Original audio asset and in-game playback | Audio integration, T-08 |
| FR-14 | Documented audio behavior at transitions | Audio transitions, T-09 |
| FR-15 | Interaction cues and control communication | Interaction feedback, T-10 |
| FR-16 | Verification methods and records | Review the test register and records in `evaluation-plan.md`; report unexecuted tests as not tested |
| NFR-01 | Demonstration build | Stability/regression, T-11 |
| NFR-02 | Project structure and core components | Code and project-structure inspection; no dedicated test ID |
| NFR-03 | Narrative UI at target resolution | Dialogue, T-03; visual inspection at the selected target resolution |
| NFR-04 | Control instructions and successful interaction | Navigation, T-02; interaction feedback, T-10 |
| NFR-05 | Audio playback and transitions | Audio integration, T-08; audio transitions, T-09 |
| NFR-06 | Repository files, dependency/version details, and opening instructions | Reproducibility, T-12 |
| NFR-07 | Scope, priorities, and documented exclusions | Scope and project-priority review; no dedicated test ID |
| NFR-08 | Branch scenes and narrative framing | Narrative framing, T-07; explicit narrative review of both branches |
| NFR-09 | Evaluation procedures, metrics, and records | Review `evaluation-plan.md` and any resulting evaluation records; no dedicated test ID |

## 10. Remaining Design Decisions

The following details remain open and should be resolved during narrative design:

1. The specific events and interactions that establish April's life in Chapter I.
2. How the diagnosis is communicated and how much medical detail is included.
3. Which characters appear in Chapter II and the final branches.
4. The exact scenes that distinguish engagement from withdrawal.
5. Whether the endings explicitly depict April's death or leave the outcome uncertain.
6. Whether the player can explore optional rooms, objects, or memories.
7. Whether dialogue choices exist before the final decision and whether they affect later scenes.
8. The target platform, resolution, and accessibility options.

These are open design decisions, not missing evidence of implementation. They should be resolved as the story and prototype develop. The target platform and resolution must be defined before final environment-specific verification is performed.

## 11. Definition of a Successful Pre-Defense Prototype

The pre-defense prototype will be considered successful when it demonstrates:

- A coherent three-chapter narrative structure.
- A playable 2D top-down environment.
- A representative interaction and dialogue sequence.
- The consequential choice between engagement and withdrawal.
- Two demonstrably different narrative experiences after the choice.
- At least one original music track integrated into the game.
- A documented evaluation plan and clearly recorded outcomes for tests that have been performed, with untested items identified as such.
- A repository and project documentation that make the current state and remaining work clear.

The prototype does not need to contain the complete final game. Its purpose is to demonstrate that the core narrative concept is feasible, that the choice can be implemented and evaluated, and that the practical project is aligned with the diploma's research objectives.

