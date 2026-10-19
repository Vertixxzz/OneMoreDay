# One More Day — Requirements Specification and Narrative Structure

**Project type:** 2D top-down narrative indie game  
**Protagonist:** April, an art university student  
**Narrative structure:** Three chapters with a consequential choice in Chapter III  
**Game engine:** Unity 6 — provisional selection  
**Dialogue system:** Yarn Spinner — provisional selection  
**Original music:** Produced in FL Studio  
**Document status:** Draft for pre-defense  
**Version:** 0.2

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

## Chapter I — Before the Diagnosis

**Narrative purpose:** Establish April as a person with a life, relationships, interests, and plans of her own.

The first chapter introduces April's ordinary environment before the diagnosis. The player should have opportunities to encounter elements of her university life, interact with relevant characters, and learn about the relationships that matter to her.

**Intended narrative elements**

- Introduction to April and her everyday personality.

- Establishment of family and friendship relationships.

- Introduction to her art university environment.

- Opportunities to explore the setting and interact with selected characters or objects.

- Foreshadowing, if appropriate, without revealing the entire central conflict too early.

**Chapter completion criterion:** The player can identify April's basic personality, important relationships, and aspects of her life that become relevant after the diagnosis.

## Chapter II — The Diagnosis

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

## Chapter III — How to Spend the Remaining Time

**Narrative purpose:** Give the player agency over April's response to her situation without presenting the choice as a means of guaranteeing survival.

The player chooses between continued engagement with other people and withdrawal from social interaction.

### Branch A — Engagement

April chooses to keep interacting with the world around her.

**Potential narrative consequences include:**

- Additional conversations with family and friends.

- Opportunities to maintain or revisit meaningful relationships.

- Scenes that show April attempting to preserve parts of her former identity and routine.

- Moments of connection, difficulty, vulnerability, or unresolved conflict.

This branch is not a guaranteed happy ending. Continued engagement does not reverse the diagnosis or promise recovery.

### Branch B — Withdrawal

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

**Priority definitions:**

- **Must:** Essential for the core prototype.

- **Should:** Important but potentially deferrable.

- **Could:** Optional enhancement.

| ID | Requirement | Priority | Acceptance criteria |
| --- | --- | --- | --- |
| FR-01 | The game shall launch into a playable state. | Must | The application launches in the target test environment and reaches the initial scene without a blocking error. |
| FR-02 | The game shall use a 2D top-down presentation. | Must | The prototype includes a top-down scene in which the player can navigate or interact as defined by the implemented controls. |
| FR-03 | The narrative shall be divided into three chapters. | Must | The prototype's narrative structure identifies Chapters I, II, and III, and the implemented sequence follows the documented order. |
| FR-04 | Chapter I shall introduce April's life before the diagnosis. | Must | The implemented opening presents April and at least one relevant aspect of her ordinary life or relationships. |
| FR-05 | Chapter II shall introduce the diagnosis and hospital setting. | Must | The implemented narrative communicates the central diagnosis and establishes the change in setting and circumstances. |
| FR-06 | The game shall support in-game dialogue or equivalent narrative presentation. | Must | A complete test dialogue sequence can be triggered, displayed, and advanced without becoming stuck. |
| FR-07 | The player shall be able to interact with relevant characters or objects. | Must | At least one documented interaction can be completed through the intended input method. |
| FR-08 | Chapter III shall present the consequential choice between engagement and withdrawal. | Must | The player can select either option, and the game records the selected branch. |
| FR-09 | The engagement branch shall present distinct narrative content. | Must | Selecting engagement leads to at least one scene or interaction that is not identical to the corresponding withdrawal-branch content. |
| FR-10 | The withdrawal branch shall present distinct narrative content. | Must | Selecting withdrawal leads to at least one scene or interaction that is not identical to the corresponding engagement-branch content. |
| FR-11 | The selected branch shall affect the depiction of April's relationships. | Must | The two branches contain at least one documented difference in character interactions, dialogue, or relationship presentation. |
| FR-12 | The game shall not promise that the final choice guarantees April's recovery. | Must | Neither branch displays or implies a guaranteed cure as a reward for choosing a particular option. |
| FR-13 | The game shall play original music integrated into Unity. | Must | At least one original track produced in FL Studio plays in the intended scene without an integration error. |
| FR-14 | Audio behavior shall respond appropriately to narrative or scene transitions. | Should | Music starts, stops, or transitions according to the documented behavior for the tested sequence. |
| FR-15 | The game shall provide enough feedback for the player to understand basic interactions. | Should | A first-time tester can identify the intended interaction method or the usability test identifies what must be improved. |
| FR-16 | The project shall provide a documented method for testing core requirements. | Must | Every Must requirement has a verification method and a recorded result. |

## 5. Non-Functional Requirements

| ID | Requirement | Priority | Acceptance criteria |
| --- | --- | --- | --- |
| NFR-01 | The prototype shall be stable enough for a demonstration. | Must | The predefined demonstration scenario can be completed without a crash or blocking defect. |
| NFR-02 | The project shall use maintainable code and identifiable game components. | Should | Core interaction, dialogue handling, chapter progression, and audio behavior can be located and modified without relying on one monolithic script. |
| NFR-03 | Narrative text shall be readable. | Must | Text is not clipped or obscured at the selected target resolution during the test scenario. |
| NFR-04 | Player controls shall be understandable. | Must | Controls are documented or communicated in-game and support completion of the test scenario. |
| NFR-05 | Audio shall play without unintended clipping or disruptive behavior. | Must | The tested track plays at an appropriate level without unintended playback or transition defects. |
| NFR-06 | The project shall be reproducible from version-controlled source files. | Should | The repository documents the engine version and dependencies and provides instructions for opening the project. |
| NFR-07 | The project shall remain feasible for independent development. | Must | The scope and implementation priorities are documented, and optional features do not block the core narrative experience. |
| NFR-08 | The narrative shall avoid presenting the two choices as a simple moral test. | Should | Review of the implemented scenes finds no requirement that one branch must be rewarded as morally superior. Any potentially judgmental framing is explicitly considered during narrative review. |
| NFR-09 | The project shall support evaluation of narrative and usability outcomes. | Must | The evaluation plan defines test scenarios, metrics, recording procedures, and limitations. |

## 6. Narrative State and Branch Management

The implementation must preserve the player's Chapter III decision throughout the selected branch.

**Minimum narrative state**

- Current chapter.

- Current narrative sequence or scene.

- Selected Chapter III branch.

- Any additional state variables required by the implemented dialogue or interactions.

**Branch behavior**

1. The player progresses through the shared narrative structure.

1. The game presents the final choice at the documented point in Chapter III.

1. The selected option is stored in the narrative state.

1. The game loads the corresponding branch content.

1. Branch-specific scenes and dialogue are presented.

1. The branch reaches its intended ending sequence.

If saving and loading are implemented, the selected branch must remain consistent after loading a saved game. Persistent saves are not mandatory for the initial vertical slice unless they are required by the final design.

## 7. Technology Requirements and Constraints

The following technology choices are provisional and must be validated against the implementation.

| Component | Proposed technology | Purpose |
| --- | --- | --- |
| Game engine | Unity 6 | 2D scenes, input, interactions, and application builds |
| Dialogue system | Yarn Spinner | Organizing dialogue and implementing narrative choices |
| Programming language | C# | Gameplay logic, interaction handling, and state management |
| Music production | FL Studio | Creating and exporting original music |
| Version control | Git with GitHub or another Git hosting service | Tracking development and preserving project history |

The final selection of the dialogue system should account for the need to trigger scenes, preserve the selected branch, and coordinate narrative state with gameplay logic.

## 8. Verification and Evaluation Plan

Verification and evaluation serve different purposes.

**Verification** checks whether the implemented features satisfy their specified requirements.

**Evaluation** examines whether the resulting experience communicates the intended narrative and provides meaningful player agency.

**Technical verification**

| Test | Procedure | Expected result |
| --- | --- | --- |
| T-01: Launch | Start the application and enter the first scene. | The game reaches a playable state. |
| T-02: Navigation | Move through the implemented top-down environment. | Movement or navigation behaves according to the documented controls. |
| T-03: Dialogue | Trigger and advance a narrative sequence. | Text displays and progresses correctly. |
| T-04: Chapter progression | Complete the available sequence and progress through the implemented chapter flow. | The next intended narrative sequence is reached. |
| T-05: Branch selection | Select engagement in one run and withdrawal in another. | Each selection activates the correct branch. |
| T-06: Branch distinction | Compare the two runs using a predefined content checklist. | At least one scene or relationship interaction differs between the branches. |
| T-07: Audio integration | Play the intended sequence with the original track enabled. | The track plays correctly and follows the documented scene behavior. |
| T-08: Regression | Repeat the core scenario after relevant changes. | Previously passing core functionality continues to work. |

**Narrative evaluation**

**The evaluation should explore the following questions:**

- Can players describe who April is beyond her diagnosis?

- Do players understand the difference between the two final choices?

- Can players identify how the choice changes the scenes or relationships they experience?

- Do players interpret the choice as a personal response to the situation rather than as a simple good-versus-bad decision?

- Does the audiovisual presentation support the intended emotional tone?

**Initial metrics**

| Metric | Measurement |
| --- | --- |
| Scenario completion rate | Percentage of testers completing the defined scenario |
| Branch activation accuracy | Whether each selected option leads to its intended branch |
| Branch content difference | Checklist of unique scenes, interactions, and dialogue |
| Narrative comprehension | Responses to short questions about April, the conflict, and the choice |
| Perceived agency | Post-test questions about whether the choice meaningfully changed the experience |
| Usability friction | Observed confusion, failed interactions, and requests for assistance |
| Blocking defects | Count of defects preventing completion |

The evaluation should use a small, documented group of testers appropriate to the project's resources. Findings must be reported as preliminary if the sample is small. The results should not be generalized to all players or used to claim that one particular narrative approach is universally effective.

## 9. Traceability Matrix

| Requirement group | Evidence | Verification |
| --- | --- | --- |
| FR-01–FR-03 | Build, scenes, chapter structure | Launch and progression tests |
| FR-04–FR-07 | Opening scenes, hospital sequence, interactions, dialogue | Narrative walkthrough and interaction tests |
| FR-08–FR-12 | Branch state and branch-specific content | Two-run branch comparison |
| FR-13–FR-14 | Original audio assets and playback logic | Audio integration test |
| FR-15 | Interaction cues and controls | First-time tester observation |
| FR-16 and NFR-01–NFR-09 | Source code, documentation, evaluation records | Project review and test report |

## 10. Remaining Design Decisions

**The following details remain open and should be resolved during narrative design:**

1. The specific events and interactions that establish April's life in Chapter I.

1. How the diagnosis is communicated and how much medical detail is included.

1. Which characters appear in Chapter II and the final branches.

1. The exact scenes that distinguish engagement from withdrawal.

1. Whether the endings explicitly depict April's death or leave the outcome uncertain.

1. Whether the player can explore optional rooms, objects, or memories.

1. Whether dialogue choices exist before the final decision and whether they affect later scenes.

1. The target platform, resolution, and accessibility options.

These are open decisions, not missing evidence of implementation. They should be resolved as the story and prototype develop.

## 11. Definition of a Successful Pre-Defense Prototype

**The pre-defense prototype will be considered successful when it demonstrates:**

- A coherent three-chapter narrative structure.

- A playable 2D top-down environment.

- A representative interaction and dialogue sequence.

- The consequential choice between engagement and withdrawal.

- Two demonstrably different narrative experiences after the choice.

- At least one original music track integrated into the game.

- Documented tests and a preliminary evaluation plan.

- A repository and project documentation that make the current state and remaining work clear.

The prototype does not need to contain the complete final game. Its purpose is to demonstrate that the core narrative concept is feasible, that the choice can be implemented and evaluated, and that the practical project is aligned with the diploma's research objectives.
