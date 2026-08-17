# A/B Experiment Brief, StreamLine (B2C)

## Parameters
| Parameter | Decision |
|---|---|
| Feature under test | A1 · Spotlight Curated Rail. Home-screen rail displaying 5-10 editor-curated recommendations immediately upon app launch. |
| Persona | Quality-focused streaming subscribers who want to find a great movie or show quickly, but become frustrated when a large catalog makes discovery overwhelming and time-consuming. |
| Expected outcome | Users spend less time browsing, choose content more quickly, and start watching within 5 minutes more often. |
| Primary success metric | % of sessions where a user starts watching content within 5 minutes of opening StreamLine. |
| Baseline rate | Use your M3 value (example: 30%). The uploaded documents do not contain the actual baseline. |
| Guardrail metric | Content completion rate and recommendation satisfaction. |
| Guardrail boundary | Investigate if either metric declines by more than 2 percentage points. |
| Second guardrail | Average session length does not decrease by more than 5%. This protects against users starting content quickly but abandoning shortly after. |
| Minimum Detectable Effect | +5 percentage points improvement in watch-start rate. |
| Sample size per arm | 1,377 |
| Traffic split | 50% Control / 50% Variant |
| Test duration | 14 days (covers two weekly usage cycles) |
| Significance threshold | p < 0.05 |

## Control vs. Variant
- **Control (A):** Users open StreamLine and browse through existing recommendation rows and categories. They often spend 15-20 minutes scrolling through thousands of titles without confidence in their choice and may leave StreamLine to seek recommendations from Google, review sites, friends, or competing services before deciding what to watch.

Current experience:

Standard home screen recommendation rows
Large catalog browsing experience
Existing recommendation categories
No Spotlight Curated Rail
No editor-curated recommendations presented immediately on launch
- **Variant (B):** A1 · Spotlight Curated Rail

Screens from the PRD:

Home Screen (Entry Point) – Spotlight Curated Rail with 5-10 recommendations.
Title Details Screen (Feature Core) – Content details and Watch Now action.
Now Playing Screen (Success/Confirmation) – Confirmation that content has been selected and playback has started.

Functional Requirements from the PRD:

Spotlight Curated Rail must appear immediately on app launch.
Spotlight must display between 5 and 10 curated titles.
All displayed titles must come from a predefined curated dataset.
Users must be able to access Spotlight without using search or filters.
Selecting a recommendation must open a title details page.
Users must be able to start playback from the title details page.
The system must track watch starts originating from Spotlight.
The system must record time-to-first-watch for metric evaluation.
- **Held constant (isolation check):** The following are identical between Control and Variant:

Same StreamLine app version
Same content catalog
Same title detail page
Same playback experience
Same recommendation engine
Same onboarding flow
Same notifications
Same pricing and subscription model
Same search functionality
Same analytics framework
Same user accounts
Same content availability

Only one thing changes: the addition of the Spotlight Curated Rail displaying 5-10 editor-curated recommendations immediately after app launch.

This creates a clean A/B test because any improvement in the watch-start metric can be attributed to the Spotlight feature itself.

## Hypothesis
> I believe that A1 · Spotlight Curated Rail. Home-screen rail displaying 5-10 editor-curated recommendations immediately upon app launch. for Quality-focused streaming subscribers who want to find a great movie or show quickly, but become frustrated when a large catalog makes discovery overwhelming and time-consuming. will result in Users spend less time browsing, choose content more quickly, and start watching within 5 minutes more often., as measured by a +5 percentage points improvement in watch-start rate. change in % of sessions where a user starts watching content within 5 minutes of opening StreamLine. within 14 days (covers two weekly usage cycles). We will protect Content completion rate and recommendation satisfaction. throughout the test.

## Shipping criteria
> We will **ship** if % of sessions where a user starts watching content within 5 minutes of opening StreamLine. improves by ≥ +5 percentage points improvement in watch-start rate. at p < 0.05 and Content completion rate and recommendation satisfaction. does not reach Investigate if either metric declines by more than 2 percentage points. after 14 days (covers two weekly usage cycles).
> We will **iterate** if direction is positive but lift is below the MDE.
> We will **kill** if the primary metric shows no improvement or moves negatively.
> The read date is fixed at the end of 14 days (covers two weekly usage cycles), no results reviewed before this date.
