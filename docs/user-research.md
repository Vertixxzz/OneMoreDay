# User Research: Evidence of Relevance

**Project:** *One More Day*  
**Diploma topic:** *Independent Game Development as a Catalyst for the Evolution of the Video Game Industry*  
**Document status:** Preliminary findings from three asynchronous text-based discussions  
**Data period:** 22–23 October 2026  

## 1. Purpose

The purpose of this preliminary research was to gather perspectives on independent game development, player preferences, and the factors that shape the reception of indie games. The evidence is used to inform the scope and initial requirements of *One More Day* and to support the diploma research question concerning the role of independent development in the wider video game industry.

These discussions provide exploratory qualitative evidence. They do not establish that the views are representative of all players or developers, and they do not independently prove industry-wide causal claims.

## 2. Method and Participants

Information was collected through asynchronous text-based semi-structured discussions. Interview questions varied according to the participant's perspective, so not every participant answered an identical set of questions.

The supplied transcript contains three respondent records. Handles are replaced in this report with participant codes:

- **P01 — Game-development experience and player perspective.** Reported teaching game development for approximately one year, having personal projects, and working on a graduation project. Also described playing indie games, including narrative-driven titles.
- **P02 — Player interested in narrative-focused indie games.** Described playing indie titles regularly and discussed visual identity, atmosphere, narrative, music, and how they decide whether to try an unfamiliar game.
- **P03 — Player interested in the video game industry.** Reported following releases of interest and discussed indie innovation, development tools, distribution, and discoverability.

The sample is small and non-representative. The supplied transcript does not document the recruitment procedure or consent status; these details should be recorded separately before identifiable messages or quotations are used in academic submission. This report uses participant codes and paraphrases responses rather than reproducing personal handles.

## 3. Findings

### Finding 1 — Respondents associate indie development with creative experimentation

P01 described indie developers as more willing to explore experimental mechanics and storytelling, mentioning games such as *Noita*, *Enter the Gungeon*, *Risk of Rain*, *Balatro*, *OMORI*, and *Deltarune*. P02 highlighted unusual combinations of mechanics, visual style, and storytelling in titles such as *Outer Wilds*, *Signalis*, and *Disillusion ST*. P03 associated indie games with new genres, art styles, and ideas that can later appear in larger productions.

**Interpretation:** The responses support examining experimentation as one perceived contribution of independent development. They are participants' assessments, not independent proof that a particular game caused an industry-wide change.

### Finding 2 — Atmosphere and artistic identity can be important to player interest

P01 recommended focusing on writing, atmosphere, and mood for a small narrative-driven game. P02 emphasised visual presentation and atmosphere, also noting the role of music and distinctive storytelling in memorable experiences. P02's response further suggested that visual presentation, trailers, store-page material, and reviews may influence whether an unfamiliar game receives attention.

**Interpretation:** For *One More Day*, narrative, visual presentation, and original music should be considered as elements of one coherent experience. The interviews do not establish that every player prioritises atmosphere or music equally.

### Finding 3 — Finishing a game and controlling its scope are significant development concerns

P01 identified completing a game as a major challenge. The respondent noted that implementation, expanding mechanics, additional details, and polishing can make a project substantially more demanding than it initially appears. P01 also recommended avoiding an oversized scope and maintaining adequate rest.

**Interpretation:** This provides direct practitioner-perspective support for keeping the initial playable scope manageable and prioritising a coherent core experience over optional systems.

### Finding 4 — Discoverability and marketing are perceived as major indie challenges

P01 emphasised marketing and wishlists. P02 referred to reviews, mechanics, trailers, store-page presentation, and the uniqueness of a game's concept as factors in deciding whether to try an unfamiliar title. P03 also identified discoverability and competition among a large number of releases as challenges.

**Interpretation:** The findings support including discoverability and distribution constraints in the diploma's broader analysis of independent game development. They do not validate a marketing strategy for *One More Day*, which has not been marketed or tested.

### Finding 5 — Creative ambition still needs reliable implementation

P02 identified game-breaking bugs as a reason to reject a game. P01's recommendations combined creative focus with scope control, while P03 discussed both opportunities created by accessible tools and the difficulty of standing out in a crowded market.

**Interpretation:** A small project should aim for a distinctive core idea without neglecting basic stability and interaction clarity.

### Finding 6 — Accessible tools can lower some barriers, but they do not guarantee success

P01 mentioned lightweight engines, graphics tools, and music software as options for developers with limited hardware resources. P03 referred to engines such as Unity and Godot and distribution platforms such as Steam as resources that make development and release more accessible, while also noting intense competition.

**Interpretation:** This supports examining accessible production tools and distribution platforms in the literature review and technology comparison. It is not, by itself, evidence that one particular engine or tool is the best choice for *One More Day*.

## 4. Evidence-to-Requirements Mapping

The table distinguishes what participants actually reported from the design implications inferred for the project.

| Interview evidence | Implication for *One More Day* | Related requirement or project decision | Evidence status |
|---|---|---|---|
| P01 stressed the difficulty of completing projects and advised keeping the scope manageable. | Prioritise a small, demonstrable core experience before adding optional features. | **NFR-07** — feasibility for independent development; project scope and implementation priorities. | Directly reported concern; design implication derived from it. |
| P02 said game-breaking bugs can prevent them from enjoying or continuing a game. | The core demonstration scenario should be stable and free of blocking defects. | **NFR-01** — prototype stability; **FR-01** — launch into a playable state. | Directly reported player preference; not a test result for this game. |
| P01 recommended attention to writing, atmosphere, and mood; P02 valued visual identity, atmosphere, music, and narrative. | Design and review dialogue, visual presentation, and music as parts of a coherent narrative experience. | **FR-06** — dialogue/narrative presentation; **FR-13** — original music; **NFR-05** — appropriate audio behaviour. | Directly reported preferences; relevance to this particular game remains to be evaluated. |
| P01 and P02 described narrative-driven indie games as appealing and named examples that made a strong impression. | Retain narrative-focused indie-game players as the preliminary intended audience, subject to further validation. | Project proposal — target users; **FR-04–FR-06** — establishing April and presenting the narrative. | Preliminary audience support from a small sample, not representative validation. |
| P01, P02, and P03 discussed experimentation and distinctive design in indie games. | The practical project should have a clear creative identity rather than add features solely to increase scope. | Research objectives and project concept; **NFR-07** — feasible scope. | Respondents' perceptions; the originality or industry impact of a design must be assessed separately. |
| P01 and P03 raised marketing/discoverability, while P02 mentioned reviews and presentation when choosing unfamiliar games. | Include discoverability and distribution as industry-level factors in the diploma discussion. | Diploma research on independent development, distribution, and industry constraints. | Qualitative interview evidence; no market size or causal effect was measured. |
| No supplied response evaluated the *One More Day* concept or its engagement-versus-withdrawal choice directly. | Do not claim that the concept, the final choice, or its emotional framing has been validated by these interviews. Test the concept with potential players in a follow-up discussion or prototype evaluation. | **FR-08–FR-12** — choice and branch requirements; **NFR-08** — avoiding a simple moral test. | **Unvalidated design assumption / next validation step.** |

## 5. Reported Findings Versus Assumptions

### Findings directly supported by the transcript

- The three respondent records contain positive views about the potential for creative experimentation in indie games.
- Scope control and completing projects were raised as development concerns by the participant with game-development experience.
- Atmosphere, visual identity, narrative, music, reviews, trailers, and presentation were raised as factors that may influence individual players' experiences or choices.
- Discoverability and marketing were raised as challenges for small developers.
- At least one player explicitly identified game-breaking bugs as a major negative factor.

These are findings about what the respondents said. Statements about industry history, market conditions, or the effects of a game on later titles remain participant opinions unless supported separately by literature or other evidence.

### Assumptions and questions that remain open

- Whether the intended audience will find *One More Day*'s specific premise compelling.
- Whether players will understand the Chapter III choice and perceive the two branches as meaningfully different.
- Whether the narrative will avoid being interpreted as presenting engagement as morally superior to withdrawal.
- Which visual style, length, controls, or accessibility options best suit the intended audience.
- Whether the selected technology stack will prove to be the most efficient once a vertical slice is implemented.

These assumptions should be assessed through concept feedback and later prototype testing. The current interview set does not answer them directly.

## 6. Limitations

The study includes only three respondent records, uses different interview guides, and relies on self-reported opinions. The participants were not shown a concept description or prototype of *One More Day* in the supplied transcript. The responses are therefore useful for preliminary relevance and requirement discussions, but they cannot demonstrate usability, acceptance of the game's specific narrative choice, or a causal influence of indie games on the wider industry.

A follow-up discussion with potential players should present the game's short concept description and ask neutral questions about clarity, expectations, and the interpretation of the final choice. Later, a playable prototype should be evaluated using the existing verification and evaluation plan.

## 7. Conclusion

The preliminary discussions suggest that respondents value creative experimentation in indie games while recognising practical constraints such as project completion, discoverability, and technical quality. For *One More Day*, the most actionable implications are to keep the prototype scope realistic, create a coherent narrative and audiovisual identity, and prioritise a stable core experience. The project's specific narrative choices remain design hypotheses until they are discussed with potential players and evaluated using a prototype.
