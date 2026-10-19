# One More Day — Verification and Evaluation Plan

**Project:** One More Day, a 2D top-down narrative game
**Related document:** `docs/One More Day.docx` — *Requirements Specification and Narrative Structure*  
**Implementation status:** The plan describes how the prototype should be checked. It does not report completed tests or user-study results.

## 1. Purpose and Scope

This document defines how the One More Day prototype will be checked against its requirements and how a small exploratory evaluation will examine the intended narrative experience.

Two activities are distinguished:

- **Verification** checks whether the implemented features behave according to documented requirements. Examples include launching the build, advancing dialogue, recording the final choice, and playing the original music track.
- **Evaluation** explores whether players understand the story and experience the final choice as a meaningful narrative decision. It also records confusion and usability problems that may need design changes.

The plan covers the core prototype, not a complete commercial-scale game. It focuses on a playable 2D top-down environment, representative dialogue and interaction, the three-chapter narrative structure, the Chapter III choice between engagement and withdrawal, distinguishable branch content, and audio integration.

The plan does not attempt to measure clinical outcomes, diagnose player reactions, or demonstrate that one narrative approach is universally effective.

## 2. Evaluation Questions

The exploratory evaluation will address the questions already identified in the requirements specification:

1. Can players describe April as a person beyond her diagnosis?
2. Do players understand the difference between the engagement and withdrawal choices?
3. Can players identify how the choice changes the scenes, dialogue, or relationships they experience?
4. Do players interpret the choice as a personal response to the situation rather than a simple good-versus-bad decision?
5. Does the audiovisual presentation support the intended emotional tone?
6. Can first-time players understand the basic controls and complete the test scenario without substantial assistance?

These questions concern the current prototype and the experience of the people who test it. Findings will be reported as preliminary and will not be generalized to all players.

## 3. Evaluation Approach

The project will use three complementary forms of evidence.

| Activity | Purpose | Evidence recorded |
|---|---|---|
| Functional verification | Check that required features work | Test result, build/version, defects, and reproduction steps |
| Narrative and content review | Check that both branches contain the intended differences and that the framing does not require one choice to be morally superior | Branch comparison checklist and reviewer notes |
| Exploratory player evaluation | Observe comprehension, agency, and interaction usability | Task completion, observation notes, short post-test answers, and participant feedback |

Where possible, test cases will be run again after a relevant fix. A test is not considered passed merely because the feature appears in the source files; the expected behavior must be observed in a running build or verified through an explicitly documented review method.

## 4. Test Conditions and Baseline

### 4.1 Technical test conditions

For each test session, record:

- Build or commit identifier.
- Date of the test and tester code.
- Operating system and target resolution used.
- Input method and the documented control scheme.
- Test scenario and starting scene.
- Whether the test was run on a clean launch or after another scenario.
- Result, observed defects, and steps needed to reproduce any failure.

The target platform, target resolution, and final control scheme are still open design decisions in the requirements specification. They must be recorded here once selected; they should not be silently assumed in the final report.

### 4.2 Baseline

The **functional baseline** is the first documented run of each test case against a named prototype build. Later runs will be compared with this record to identify regressions and verify fixes.

For player evaluation, the baseline is the first-time, unassisted attempt at the defined scenario. Participants should receive only the instructions needed to start the test. Any help given during the scenario must be recorded. This baseline is descriptive rather than a comparison against another game or a representative population.

### 4.3 Test status values

Use the following values in the test log:

- **Pass:** The expected result was observed.
- **Fail:** The expected result was not observed, or a blocking defect prevented completion.
- **Blocked:** The test could not be run because a prerequisite or feature was unavailable.
- **Not run:** No result has been collected yet.

A blocked or unrun test must not be reported as passed.

## 5. Functional Verification Plan

The following cases are based on the tests and acceptance criteria in the requirements specification. They are planned tests; no results are implied by this table.

| Test ID | Area / related requirement | Procedure | Expected result and acceptance condition | Evidence |
|---|---|---|---|---|
| T-01 | Launch — FR-01, NFR-01 | Start the prototype from the intended test environment and enter the initial scene. | The game reaches a playable state without a blocking error or crash. | Build identifier, result, and defect notes. |
| T-02 | Navigation — FR-02, NFR-04 | Use the documented controls to navigate the top-down scene. | Movement or navigation behaves as specified, and the controls are understandable from the supplied instructions or in-game cues. | Observation notes and any input-related defects. |
| T-03 | Dialogue — FR-06 | Trigger a representative dialogue sequence and advance through it. | Dialogue appears legibly, progresses through the intended sequence, and does not become stuck. | Scene/sequence identifier and screenshots or notes for defects. |
| T-04 | Chapter progression — FR-03–FR-05 | Follow the implemented narrative path through the available chapter sequence. | The available content follows the documented order and communicates the intended narrative function of the implemented chapter or scene. | Walkthrough checklist and content notes. |
| T-05 | Branch selection — FR-08 | Run the final-choice scenario twice: select engagement in one run and withdrawal in the other. | Each choice is recorded and activates its corresponding branch. | Selected option and resulting branch for each run. |
| T-06 | Branch distinction — FR-09–FR-11 | Compare both runs against a predefined checklist of scenes, interactions, dialogue, and relationship depiction. | Each branch contains at least one documented, observable difference; the difference is not limited to the button label or branch name. | Completed branch comparison checklist. |
| T-07 | Narrative framing — FR-12, NFR-08 | Review both branches and their ending sequences against the requirements. | Neither branch implies that choosing it guarantees recovery, and the narrative does not require one branch to be framed as morally superior. Potentially judgmental wording is recorded for review. | Content review notes and specific lines/scenes flagged. |
| T-08 | Audio integration — FR-13, NFR-05 | Play the intended scene with an original track enabled. | At least one original track plays in the intended scene without missing playback, unintended clipping, or disruptive playback behavior. | Track/scene identifiers and audio defect notes. |
| T-09 | Audio transitions — FR-14 | Exercise the documented scene or narrative transition for which audio behavior is specified. | Music starts, stops, or transitions according to the documented behavior. If this behavior is not implemented yet, record the test as Blocked or Not run. | Transition tested, expected behavior, and result. |
| T-10 | Interaction feedback — FR-07, FR-15 | Ask a first-time tester to perform a documented interaction without coaching. | The tester can identify and perform the intended interaction, or the observation produces a specific issue to address. The test is not passed solely because the tester succeeds after unrecorded assistance. | Task result, assistance given, and confusion observed. |
| T-11 | Stability and regression — NFR-01, FR-16 | Repeat the core demonstration scenario after a relevant change. | No new blocking defect prevents the scenario from being completed; previously passing tests remain passing or any regression is recorded. | Before/after build identifiers and test log. |
| T-12 | Reproducibility — NFR-06 | Review the repository and follow the documented instructions to identify the required engine version and dependencies. When the project is available, attempt to open it in a clean environment if feasible. | The version and dependencies are documented. Any clean-environment opening attempt is recorded separately from a documentation-only review. | Repository checklist and environment notes. |

### 5.1 Coverage of requirements

Every **Must** requirement in the requirements specification must have a verification method and a recorded result before the final project report. The current mapping is:

| Requirement group | Planned evidence |
|---|---|
| FR-01–FR-03 | Launch test, playable scene, and narrative sequence review |
| FR-04–FR-07 | Opening-scene walkthrough, hospital/diagnosis scene review, interaction and dialogue tests |
| FR-08–FR-12 | Two-run branch selection test, branch content comparison, and narrative framing review |
| FR-13–FR-14 | Original audio asset identification and playback/transition tests |
| FR-15 | First-time interaction observation |
| FR-16 and NFR-01–NFR-09 | Complete test log, stability/regression checks, repository review, and exploratory evaluation records |

Some non-functional requirements, such as maintainability and feasibility for independent development, require a documented project review rather than a single runtime test. The review method and evidence should be recorded explicitly.

## 6. Exploratory Player Evaluation

### 6.1 Participants and scope

The evaluation will use a small, convenience-based group of testers appropriate to the project's resources. A provisional target is **3–5 participants** for an initial exploratory round; the final number and any recruitment constraints should be documented before testing. This is a practical usability sample, not a statistically representative sample of the intended audience.

Participant results should be identified using neutral codes (for example, P01 and P02). Do not collect names or personal medical histories unless there is a specific, approved reason to do so; such information is not required for this evaluation.

### 6.2 Session procedure

1. Explain that the session evaluates the prototype, not the participant, and that participation is voluntary.
2. Tell the participant that the story includes a cancer diagnosis, hospitalization, and emotionally difficult choices. Allow them to decline or stop without explanation.
3. Give the minimum instructions needed to launch the build and understand the available controls.
4. Ask the participant to complete the defined scenario. Observe without coaching where possible; record all assistance provided.
5. If both narrative branches are implemented, arrange for the participant to experience both in a documented order or use a consistent order across participants. Record the order, because sequence can affect the response.
6. Ask the short post-test questions below. Do not suggest a “correct” interpretation.
7. Invite optional comments about confusing interactions, narrative clarity, and the audiovisual presentation.
8. Record the build identifier, duration if measured, task results, observations, and any deviations from the procedure.

If the available prototype cannot yet be completed end-to-end, evaluate only the available scenario and state the limitation. Do not imply that participants tested unavailable chapters or branches.

### 6.3 Post-test questions

Use open-ended questions first to avoid leading participants:

1. “How would you describe April as a person? What did you learn about her life or relationships?”
2. “What did you understand the two choices in Chapter III to mean?”
3. “What changed after the choice you experienced?”
4. “Did the choice feel meaningful to you? What made it feel that way, or not?”
5. “Did the story seem to present one option as the morally correct choice? What gave you that impression?”
6. “How did the visuals, dialogue, and music affect your understanding or experience of the scene?”
7. “Was anything confusing or difficult to interact with?”

Participants may skip any question. Their response is evidence of their interpretation, not proof of a universal effect.

## 7. Metrics and Provisional Success Criteria

The requirements specification names the metrics below. Where the original specification does not set a numeric threshold, the proposed criteria in this table are **working thresholds for the initial prototype** and should be confirmed before formal testing. They must not be described as measured results.

| Metric | Operational definition | Provisional success criterion for the initial round | Recording method |
|---|---|---|---|
| Scenario completion rate | Number of participants who complete the defined scenario without moderator intervention divided by participants who attempted it. | Report the exact count and percentage. A target of at least 4 out of 5, or all participants for a smaller group, may be used as an initial usability goal; investigate every failure rather than treating the threshold as proof of quality. | Task log. |
| Branch activation accuracy | Whether the selected option activates the intended branch in each test run. | Both options activate the correct branch in repeated verification runs. For participant sessions, record every observed mismatch. | Branch-selection log. |
| Branch content difference | Count and description of pre-identified branch differences in scenes, dialogue, interactions, or relationship depiction. | At least one meaningful, documented difference per branch, as required by FR-09–FR-11. | Branch checklist. |
| Narrative comprehension | Whether answers demonstrate an understanding of April's identity beyond diagnosis, the situation, and the difference between choices. | Use a simple coding rubric: “demonstrated,” “partly demonstrated,” or “not demonstrated,” with a brief excerpt or paraphrase supporting each code. Do not reduce nuanced answers to a single unsupported score. | Post-test response sheet. |
| Perceived agency | Participant explanation of whether and how the choice changed the experienced story. | Report the distribution of responses and supporting explanations. Treat disagreement or lack of perceived impact as a design finding, not a participant failure. | Post-test response sheet. |
| Usability friction | Count and description of hesitation, failed interactions, confusion, or requests for assistance. | Every observed issue that blocks progress is logged. Repeated non-blocking issues are listed for prioritization; there is no assumed zero-issue threshold for an early prototype. | Observation log. |
| Blocking defects | Number of defects that prevent the defined scenario from being completed. | Zero known blocking defects in the final demonstration run. Any unresolved blocking defect must be disclosed. | Defect log and regression tests. |
| Audio behavior | Whether the intended track plays and follows the specified scene behavior without a disruptive defect. | The audio integration test passes for the selected demonstration scenario. | Test log and reviewer notes. |
| Narrative framing | Whether the participant or reviewer interprets the choice as a simple good-versus-bad test, with the specific narrative cues recorded. | No requirement that one branch be treated as morally superior. Any apparent moralizing cue is documented and reviewed; a participant's interpretation alone does not automatically establish authorial intent. | Content review and participant responses. |

For a small sample, prioritize descriptive counts, examples, and recurring observations. Do not claim statistical significance or representativeness.

## 8. Data Recording Templates

### 8.1 Test execution log

| Test ID | Build / commit | Date | Result (Pass / Fail / Blocked / Not run) | Evidence or defect | Retest result |
|---|---|---|---|---|---|
| T-01 | TBD | TBD | Not run | TBD | TBD |

Duplicate the row for each test execution. Replace placeholders only when the run actually occurs.

### 8.2 Participant session log

| Participant code | Build | Scenario completed? | Assistance given | Main observations | Follow-up issue |
|---|---|---|---|---|---|
| P01 | TBD | Not run | TBD | TBD | TBD |

Keep identifiable information out of this table. Store quotations or detailed notes only when appropriate and with the participant's permission.

### 8.3 Branch comparison checklist

| Feature | Engagement branch | Withdrawal branch | Observable difference? | Notes |
|---|---|---|---|---|
| Scene / setting | TBD | TBD | Not assessed | TBD |
| Dialogue | TBD | TBD | Not assessed | TBD |
| Character interaction | TBD | TBD | Not assessed | TBD |
| Depiction of relationships | TBD | TBD | Not assessed | TBD |
| Ending sequence / tone | TBD | TBD | Not assessed | TBD |

Fill this checklist using implemented content, not intended future scenes. If a feature has not been implemented, mark it as not available rather than assuming a difference exists.

## 9. Participant Care and Data Handling

Because the story includes cancer, hospitalization, and emotionally difficult decisions:

- Tell participants about the relevant themes before the session.
- Make clear that they can stop or skip questions without giving a reason.
- Do not ask participants to disclose personal experiences with cancer or bereavement.
- Avoid presenting either fictional choice as medical advice or as a judgment of real patients.
- Record only the information needed to evaluate the prototype and use participant codes in the analysis.
- Report potentially distressing feedback respectfully and in context.

The purpose is to assess the prototype and the clarity of its narrative, not to make clinical or psychological claims.

## 10. Limitations and Threats to Validity

- **Small convenience sample:** A few testers can reveal usability problems and interpretations but cannot represent all players.
- **Prototype incompleteness:** Missing scenes, placeholders, or unfinished audio can affect feedback. Note what each participant actually experienced.
- **Moderator influence:** Hints or explanations may change how players interpret the story. Record assistance and ask open-ended questions first.
- **Order effects:** Experiencing one branch first may influence the response to the other. Record branch order and keep it consistent where practical.
- **Interpretation is contextual:** Different responses do not necessarily mean one interpretation is objectively correct. Report the evidence without overstating causality.
- **No comparative control condition:** Unless a later study explicitly defines a comparison, this evaluation does not establish that One More Day is more effective than another game or narrative approach.

## 11. Reporting Results and Exit Criteria

After testing, add a dated results section to this document or link a separate report. Include the build/commit tested, tests run, passed/failed/blocked counts, defects, participant count, tasks actually completed, summary of responses, changes made, and unresolved limitations.

The initial prototype evaluation is complete enough for reporting when:

1. Every Must requirement has a documented verification method and a result, or is clearly marked as not implemented/blocked with an explanation.
2. The core demonstration scenario has been run and any blocking defects are disclosed.
3. Both final-choice branches have been compared using the checklist if both are implemented.
4. The exploratory sessions and their limitations are documented if sessions have taken place.
5. No planned metric is presented as a result before evidence is collected.
6. The report distinguishes observed findings, design decisions, and future work.

The pre-defense prototype does not need to be the complete final game. It should demonstrate the feasibility of the core narrative concept and a credible plan for verifying and evaluating it.

## 12. Status

**Current status:** Methodology drafted; no technical test results or player-evaluation results are recorded in this document yet.

**Open items before execution:**

- Confirm the target platform and resolution.
- Finalize the demonstration scenario and implemented content available for testing.
- Confirm the initial participant target and session procedure.
- Prepare the test log and branch comparison checklist for the actual build.
- Record the build/commit identifier and all outcomes when testing begins.
