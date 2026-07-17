BULLSEYE — Interactive Prototypes
"Aim. Learn. Invest."  ·  Product Design Intern Assignment
Gamified stock-market learning platform for Indian teenagers.
===============================================================

HOW TO OPEN
-----------
1. Unzip this archive to any folder (keep all files together in the
   same folder — they link to each other by filename).
2. Double-click  index.html  to open the hub in any modern browser
   (Chrome, Edge, Safari, Firefox). No install or server required.

WHAT'S INSIDE
-------------
  index.html      →  Landing hub. Links to both prototypes.
  flow.html       →  Onboarding flow prototype (6 key screens:
                      language → hook → first trade → instant win →
                      lesson → quiz → Bull III rank-up).
  dashboard.html  →  Live daily-dashboard prototype (BI portfolio
                      chart, rank, quests, watchlist, squad league,
                      achievements).

HOW THEY INTERLINK
------------------
  • On the flow's final rank-up screen, tap "🏠 Go to my Dashboard →".
    It plays a short "landing in the app" animation, then opens
    dashboard.html — mirroring how a real user arrives after onboarding.
  • In the dashboard sidebar (ACCOUNT section), tap
    "↺ Replay onboarding" to jump back to flow.html.
  So together they read as one continuous product experience.

HOW TO USE EACH PROTOTYPE
-------------------------
  Flow:       pick a language (localizes copy), tap a "vibe" stock,
              claim the win, read the concept card, answer the quiz
              (right AND wrong both animate — no punishment), watch
              the rank-up, then hand off to the dashboard.
  Dashboard:  hover the portfolio chart for a live tooltip, switch
              1D/1W/1M/1Y, toggle EN / हिं / বাং (localizes the header),
              complete daily quests then Claim, click watchlist rows,
              sidebar tabs, the Continue CTA and avatar.
  Both are fully keyboard-navigable (Tab + Enter/Space).

TECH
----
  • Self-contained HTML/CSS/vanilla JS — no build step, no dependencies.
  • Aesthetic: macOS-style glassmorphism, JetBrains Mono, heavy
    micro-animation, BI-style data-viz simplified for teens.
  • The JetBrains Mono webfont loads from Google Fonts when online;
    offline, a monospace fallback stack is used automatically
    (fully functional either way).
  • A production-ready React + Tailwind + Framer Motion version of the
    dashboard is included in the Notion write-up (Section 5).

GEN-Z NAME
----------
  BULLSEYE — "Bull" (a rising market) + "nailing it / hitting your
  target." The target icon doubles as your rank/goal indicator.
