# A1 · Spotlight Curated Rail, Simplified PRD (StreamLine)

**Author:** Me · **Status:** Draft · **Target:** High-Fidelity Prototype · **Persona:** Quality-focused streaming subscribers

## 1. The Big Picture
- **Vision:** Help quality-focused streaming subscribers find something worth watching within 5 minutes by presenting a small set of trusted, curated recommendations that eliminate choice overload.
- **Press release:** StreamLine is launching Spotlight Curated Rail, a new way to discover great content without endless scrolling. Instead of forcing users to browse thousands of titles, Spotlight immediately presents a small collection of editor-curated recommendations designed to help users make a confident viewing decision quickly.

For subscribers who regularly spend 15-20 minutes browsing only to abandon the app or search elsewhere for recommendations, Spotlight reduces decision fatigue and guides users directly to high-quality content. The result is less time searching, more time watching, and a faster path to entertainment.
- **Success metric:** % of sessions where a user starts watching content within 5 minutes of opening StreamLine.
- **Guardrail:** Content completion rate and recommendation satisfaction must not decrease while improving watch-start speed.

## 2. The Details
### User stories
- As a quality-focused streaming subscriber, I want to see trusted recommendations immediately when I open StreamLine so that I can avoid spending 15–20 minutes browsing.
- As a subscriber with limited free time, I want a small curated set of titles so that I can choose something quickly and start watching sooner.
- As a subscriber looking for a great movie or show, I want editor-curated recommendations so that I feel confident in my viewing choice.
### Screens to build
- Home Screen (Entry Point) – Spotlight Curated Rail with 5–10 recommendations.
- Title Details Screen (Feature Core) – Content details and Watch Now action.
- Now Playing Screen (Success/Confirmation) – Confirmation that content has been selected and playback has started.
### Functional requirements
- Spotlight Curated Rail must appear immediately on app launch.
- Spotlight must display between 5 and 10 curated titles.
- All displayed titles must come from a predefined curated dataset.
- Users must be able to access Spotlight without using search or filters.
- Selecting a recommendation must open a title details page.
- Users must be able to start playback from the title details page.
- The system must track watch starts originating from Spotlight.
- The system must record time-to-first-watch for metric evaluation.
### Smart behaviors (Situation → Outcome)
- If the user opens StreamLine → then Spotlight is displayed immediately.
- If the user selects a title card → then the Title Details screen opens.
- If the user clicks Watch Now → then the Now Playing screen is displayed.
- If fewer than 5 curated titles are available → then display all available curated titles.
- If analytics tracking fails → then continue the user flow without interruption.
### Technical constraints
- No external APIs.
- No backend database.
- No authentication or user accounts.
- No machine learning or recommendation engine.
- Use a static mock dataset only.
- React frontend only.
- State management via useState only.
- No personalization logic.

## 3. The Logistics
### Features out
- AI recommendation engine
- Advanced filtering and search
- Watch Party functionality
- Offline downloads
- Curator profiles
- Push notifications
- Email digests
- User-generated playlists
- Social features
- Personalized recommendations
### Edge cases & safety guard
- If the user exits without selecting a title, the app returns to the Home screen without errors.
- If the user opens a title but does not click Watch Now, no watch-start event is recorded.
- If analytics tracking fails, the viewing flow continues uninterrupted.
- If fewer than 5 curated titles are available, display all available titles.
- Safety Guard: The prototype must only display content from the predefined curated dataset. It must never generate fictional movies, fake ratings, or claim recommendations are personalized when personalization does not exist.
### Decision log
- Chose editorial curation over personalization to validate whether trusted recommendations alone reduce choice overload before investing in recommendation infrastructure.
- Limited Spotlight to 5–10 titles to reduce cognitive load and keep the sprint focused on improving content selection speed rather than expanding catalog browsing.
### Evals
- Time-to-Watch: Increase the percentage of sessions that start watching within 5 minutes.
- Discovery Efficiency: Reduce average browsing time before a title is selected.
- Content Safety & Accuracy: 100% of displayed recommendations must come from the approved curated dataset. No generated or fabricated content allowed.

## MoSCoW scope
- **Must:** Spotlight Curated Rail visible on the home screen; 5–10 curated recommendations displayed immediately; Recommendations sourced from a predefined curated list; User can open title details from any recommendation; User can start watching from the title details page; Track watch starts within 5 minutes of app launch
- **Should:** Weekly refresh of curated recommendations; Themed rails (e.g., "Editor's Picks", "Tonight's Picks"); Click-through tracking on Spotlight titles
- **Could:** Personalized curation; User feedback ("Not Interested"); Multiple curated rails; Popularity or rating indicators
- **Won't (now):** AI recommendation engine; Advanced filters; Social watch parties; Offline downloads; Curator profiles; Email or push notifications; User-generated playlists

---
**Builder hook:** Build a working prototype based on this PRD. Use the User Story as the core flow, Functional Requirements as build constraints, and prioritize speed and clarity over visual complexity.
