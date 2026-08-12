# Roadmap, PRD & Prototype (Module 4)

## Your strategic anchors
- **Persona (M2), who are you solving for?:** Quality-focused streaming subscribers who want to find a great movie or show quickly, but become frustrated when a large catalog makes discovery feel overwhelming and time-consuming.
- **Primary success metric (M3), your leading indicator:** % of sessions where a user starts watching content within 5 minutes of opening StreamLine.
- **Moment of misery (M2), the specific friction blocking the goal:** After a long day, users spend 15-20 minutes browsing thousands of titles, still have less confidence about what to watch than when they started, and leave StreamLine to search Google, review sites, friends, or competitors for recommendations.
- **Guardrail metric (M3), what must not drop or break:** Content completion rate and recommendation satisfaction. Improvements in quick-start rate must not reduce viewing quality or user trust in recommendations.

## Scan the backlog & set a human baseline
- **My instinctive “quick wins” before touching the AI (2 to 3 feature IDs + why):** A1 · Spotlight Curated Rail
 Users are overwhelmed by choice and want trusted guidance. A curated rail immediately reduces browsing time and helps users find something worth watching faster.

A2 · "Why You'll Love This" Label
 Users lack confidence in recommendations. A simple explanation builds trust and helps them make a decision instead of continuing to scroll.

A3 · Hidden Gem Badge
 Low implementation effort with high visibility. It surfaces quality content that users might otherwise miss and supports faster discovery.

Why these three?
 All directly address the core moment of misery: users spend 15-20 minutes browsing, fail to choose something, and leave the platform without watching.

## Audit, override & decide
- **Where did you override the AI? (feature + old vs. new score + why):** A9 · Advanced Filter Engine

AI: Value 3 → My score: Value 2
Why: My M2 research shows users are overwhelmed by choice, not lacking filters. Users wanted someone to help them decide, not more ways to search. Additional filters increase complexity without addressing the core frustration.

A8 · Watch Party (Spotlight)

AI: Value 2 → My score: Value 1
Why: No interview or product health evidence suggests social viewing is blocking content discovery. The primary problem is failure to choose content, not inability to watch with friends.

A10 · Offline Download

AI: Value 3 → My score: Value 2
Why: Offline viewing improves consumption after a title has been selected. My research identified discovery failure as the dominant problem, so this feature has limited impact on the primary metric.

A3 · Hidden Gem Badge

AI: Value 3 → My score: Value 4
Why: M3 product health data showed users wanted help finding quality content and hidden gems. This is a low-effort feature that directly supports faster decision-making and discovery.
- **Did the AI over-value a Sales/Eng request your M2 interviews don’t support?:** Yes.

A8 · Watch Party (Sales request)
A9 · Advanced Filter Engine (Engineering request)
A10 · Offline Download (Sales request)

My M2 interviews consistently highlighted choice overload, recommendation distrust, and spending 15-20 minutes browsing without selecting anything. None of the interview evidence suggests social viewing, offline downloads, or advanced filtering are primary user needs.
- **Did it underweight something your M3 cohort/funnel data strongly supports?:** Yes.

A3 · Hidden Gem Badge

The M3 synthesis specifically highlights users wanting help finding quality content, hidden gems, and trusted recommendations rather than additional catalog volume. Because the feature directly surfaces overlooked content and is inexpensive to build, I increased its value score.

## Generate your interactive roadmap
- **My “Now” lane (this sprint), the 2 to 3 quick wins I’ll build first:** A1 · Spotlight Curated Rail
 Directly reduces choice overload by giving users trusted recommendations instead of forcing them to browse thousands of titles. This is the most direct response to the documented discovery problem.

A2 · “Why You'll Love This” Label
 Increases confidence in recommendations and reduces decision paralysis by explaining why a title is relevant.

A3 · Hidden Gem Badge
 Surfaces quality content that users might otherwise miss, making discovery faster and easier with minimal implementation effort.
- **What I cut, and the “no” I’m protecting the scope from:** A8 · Watch Party (Spotlight)
 Cut because the research does not show social viewing as a major user problem. Users struggle to choose content, not watch together.

A9 · Advanced Filter Engine
 Cut because users want guidance, not more filtering options. Additional filters increase complexity without addressing the core frustration.

A10 · Offline Download
 Cut because it improves viewing after content selection, while the primary problem is selecting content in the first place.

The "no" I'm protecting the scope from:
 I'm saying no to features that improve consumption, social engagement, or power-user workflows before solving the core discovery problem. With a team of two engineers and one designer, every sprint investment must help users find something worth watching within five minutes.
- **Prototype/roadmap screenshot link (paste into your deliverables):** Added seprately.
