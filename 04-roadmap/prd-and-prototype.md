# PRD & Prototype Sprint (Module 4)

## Pick & scope with MoSCoW
- **The “Now” feature I’m scoping (name + one-line core description):** A1 · Spotlight Curated Rail
 A curated row of trusted movie and TV recommendations that helps overwhelmed users find something worth watching within 5 minutes instead of endlessly browsing.
- **My finalized Must-Haves (after overriding the AI):** These directly address the moment of misery and are required for Sprint 1.

Dedicated Spotlight rail on the home screen

Visible above or near standard content rows.
Users can discover curated recommendations immediately.

Small, curated set of recommendations (5-10 titles)

Prevents overwhelming users with another large catalog.
Focuses attention on a manageable set of choices.

Editorially curated collection

Recommendations are intentionally selected rather than random.
Creates the trusted guidance users are seeking.

Ability to open a title detail page from the rail

Users must be able to evaluate and start watching content.

Instrumentation for the primary metric

Track whether users start watching within 5 minutes of app launch.
Required to measure success.
- **What I demoted from Must → Should/Won’t, and why:** SHOULD HAVE

Valuable if capacity remains after the core experience ships.

Refresh curated rail daily or weekly

Prevents the experience from feeling stale.

Simple category themes

Examples: “Tonight’s Picks”, “Award Winners”, “Hidden Gems”.
Adds relevance without requiring personalization.

Basic engagement tracking

Click-through rate.
Title starts from Spotlight rail.
COULD HAVE

V2 enhancements and polish.

Personalized curation based on viewing history.
Multiple Spotlight rails.
Dynamic ranking based on engagement.
Curator profiles.
User feedback ("More like this" / "Not interested").
A/B testing framework.
Social proof elements (ratings, popularity indicators).
WON'T HAVE (NOW)

Explicit exclusions to protect the sprint.

Advanced personalization engine.
Machine-learning recommendation rebuild.
Social watch parties.
Advanced filtering and search enhancements.
Offline downloads.
Curator profile system.
Email digests and notifications.
User-generated playlists.
Cross-device synchronization improvements.
Any feature unrelated to helping users choose content faster.

## Generate your Simplified PRD
- **One thing my PRD makes explicit that a vague brief would have missed:** The product is not trying to improve recommendations in general. It is specifically testing whether a small, trusted curated set of 5-10 titles can reduce choice overload and increase the percentage of users who start watching within 5 minutes. That scope boundary prevents the team from drifting into personalization, filters, social features, or recommendation-engine work before validating the core hypothesis.

## Prompt-to-prototype sprint
- **Where did the prototype reveal a gap in my PRD logic? (what I had to update):** The prototype exposed that the PRD never defined what makes a recommendation "trusted." While the PRD required editorially curated content, it did not specify how the UI should communicate trust to users. During prototyping, the Spotlight rail looked like another content row. I updated the PRD to include a visible label such as "Editor's Picks" or "Tonight's Picks" so users immediately understand why these recommendations are different and can make decisions faster.
- **My shareable prototype URL (Lovable: Share → Share Preview · Bolt: Publish → Web):** https://spotlight-curated-rail.lovable.app
