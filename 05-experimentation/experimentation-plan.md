# Experimentation Plan (Module 5)

## Get your documents ready
- **From M3, your hypothesis sentence:** I believe that Spotlight Curated Rail for quality-focused streaming subscribers will result in more users finding content worth watching quickly and starting playback sooner, as measured by an increase in the percentage of sessions where a user starts watching content within 5 minutes of opening StreamLine, while protecting content completion rate and recommendation satisfaction
- **From M3, your primary success metric & guardrail metric:** % of sessions where a user starts watching content within 5 minutes of opening StreamLine. Content completion rate and recommendation satisfaction must not decrease while improving watch-start speed.
- **From M4, the feature you scoped in your PRD this is what you're testing:** A1 · Spotlight Curated Rail: A home-screen experience that immediately presents 5-10 editor-curated recommendations, allowing users to access trusted content without searching or filtering and start watching more quickly.

## Define your experiment parameters
- **Feature under test pull from your M4 PRD:** A1 · Spotlight Curated Rail. A home-screen rail displaying 5-10 editor-curated recommendations immediately upon app launch.
- **Persona pull your M2 persona:** Quality-focused streaming subscribers who want to find a great movie or show quickly but become frustrated when large catalogs make discovery overwhelming and time-consuming.
- **Expected outcome the behaviour change you expect, from your M3 hypothesis:** Users spend less time browsing, select content more quickly, and start watching within 5 minutes more frequently.
- **Primary success metric the one number that defines success, from M3:** % of sessions where a user starts watching content within 5 minutes of opening StreamLine.
- **Baseline rate today's rate of your primary metric, from your M3 data:** Use the value from your M3 analysis. It is not contained in the uploaded M2/M4 documents.
- **Guardrail metric & boundary what must not break, and how far it can move before you investigate:** Content completion rate and recommendation satisfaction. Recommended boundary: investigate if either declines by more than 2 percentage points. The metrics come from M3; the boundary is a new decision required in Module 5.
- **Minimum Detectable Effect (MDE) the smallest improvement worth shipping, your floor:** Recommended: +5 percentage points improvement in watch-start rate. This is a reasonable threshold for a feature specifically designed to solve the primary user problem.
- **Sample size per arm use the calculator in the builder, baseline + MDE:** Calculate in the Experiment Brief Builder using your M3 baseline rate plus the chosen MDE.
- **Traffic split & test duration 50/50 standard · cover ≥ 2 weekly cycles:** 50/50 split. Run for 2 weeks minimum to cover at least two weekly usage cycles.
- **Significance threshold p < 0.05 is standard, explain any deviation:** p < 0.05 (standard).

## Define your control and variant
- **Control (A) the current experience, reference your M2 moment of misery and M3 funnel/workflow data:** The current StreamLine experience requires users to browse a large catalog of recommendations and categories to find something to watch. Users commonly spend 15-20 minutes scrolling through thousands of titles without confidence in their choice, often leaving StreamLine to consult Google, review sites, friends, or competing services before making a decision.

Current experience (Control A):

Standard home screen recommendation rows
Large content catalog available for browsing
Users discover content through existing recommendation categories
No Spotlight Curated Rail
No curated set of editor-selected recommendations presented immediately on app launch
- **Variant (B) your single change, copy the relevant screens & functional requirements from your M4 PRD:** Variant (B) - Spotlight Curated Rail

Single change being tested: A1 · Spotlight Curated Rail.

Screens (copied from PRD):

Home Screen (Entry Point) – Spotlight Curated Rail with 5-10 recommendations.
Title Details Screen (Feature Core) – Content details and Watch Now action.
Now Playing Screen (Success/Confirmation) – Confirmation that content has been selected and playback has started.

Functional requirements (copied from PRD):

Spotlight Curated Rail must appear immediately on app launch.
Spotlight must display between 5 and 10 curated titles.
All displayed titles must come from a predefined curated dataset.
Users must be able to access Spotlight without using search or filters.
Selecting a recommendation must open a title details page.
Users must be able to start playback from the title details page.
The system must track watch starts originating from Spotlight.
The system must record time-to-first-watch for metric evaluation.
- **Isolation check, what has NOT changed? list everything identical between arms (app version, recommendation engine, notifications, onboarding). If something changed inadvertently, your test is compromised.:** The following remain identical in both Control (A) and Variant (B):

Same StreamLine application version
Same content catalog
Same title details page
Same playback experience
Same Now Playing experience
Same recommendation engine (no AI or personalization changes)
Same onboarding experience
Same notifications
Same pricing and subscription model
Same search functionality
Same analytics framework
Same user accounts and permissions
Same content availability and licensing

Only one thing changes: the addition of the Spotlight Curated Rail on the home screen presenting 5-10 curated recommendations immediately upon app launch.

This satisfies the experiment requirement that only a single variable changes, allowing any difference in watch-start rate to be attributed to Spotlight.

## Formalize your hypothesis & shipping criteria
- **Your hypothesis (filled in):** I believe that Spotlight Curated Rail for quality-focused streaming subscribers who want to find a great movie or show quickly will result in users spending less time browsing and starting playback more quickly, as measured by a 5 percentage point improvement in the percentage of sessions where a user starts watching content within 5 minutes of opening StreamLine within a 2-week test period. We will protect content completion rate and recommendation satisfaction throughout the test.
- **Your shipping criteria (filled in):** We will SHIP if the percentage of sessions where a user starts watching content within 5 minutes of opening StreamLine improves by ≥ 5 percentage points at p < 0.05 and content completion rate and recommendation satisfaction do not decline by more than 2 percentage points after a 2-week test period.

We will ITERATE if the direction is positive but the lift is below the 5-percentage-point MDE.

We will KILL if the primary metric shows no improvement or moves negatively.

The read date is fixed at the end of the 2-week test period. No results will be reviewed before this date.
- **Hardest parameter to define, and did it change your hypothesis? quick debrief:** Minimum Detectable Effect (MDE) was the hardest parameter to define.

Why?

The feature is intended to solve the primary user problem: spending 15-20 minutes browsing without choosing content.
A very small MDE would require a much larger experiment and might not justify the investment.
A very large MDE could cause you to reject a meaningful improvement.

Did it change the hypothesis?

No.

The hypothesis stayed the same: Spotlight should help users find something worth watching faster. The MDE only defines what level of improvement is large enough to justify shipping, not whether the underlying belief changes.
