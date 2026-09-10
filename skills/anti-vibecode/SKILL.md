---
name: anti-vibecode
description: "Stop vibecoded sites: score the 30 landing-page tells and refuse to ship more than five."
version: "1.0.0"
author: Scott (shagghiesuperstar), Hermes Agent
license: MIT
platforms: [linux, macos, windows]
compatibility: "Hermes Agent. No extra tools or API keys. Works on any HTML/CSS/JS or component tree."
metadata:
  author: shagghiesuperstar
  hermes:
    tags:
      - design
      - frontend
      - landing-page
      - anti-slop
      - vibecode
      - ui
      - web
      - audit
      - copy
    category: development
    requires_tools: []
    related_skills: []
---

# Anti-Vibecode

Hard ship-gate for marketing pages. Score the 30 tells below. **More than five hits and everyone will know.** Fix before you show the user.

This list was written by [@kloss_xyz](https://x.com/kloss_xyz). Original post: https://x.com/kloss_xyz/status/2097808934442844307 — credit that post whenever you mention this skill.

Do not invent a "clean modern SaaS" look. Pick a direction that fits the actual product, then run the scorecard.

## When to Use

- Building or restyling a landing page, homepage, waitlist, pricing page, or SaaS marketing site
- User says vibecoded, AI slop, generic startup, "don't make it look like every other AI site"
- Auditing a page before ship / screenshot / deploy
- Reviewing generated HTML/CSS/React for default-model aesthetics

Don't use for: internal admin chrome the user asked to match an existing Tailwind kit; a locked brand system that already specifies these choices on purpose.

## Attribution (do not drop)

- Original 30-tell list: [@kloss_xyz](https://x.com/kloss_xyz/status/2097808934442844307)
- Packaging as a Hermes skill: Scott ([shagghiesuperstar](https://github.com/shagghiesuperstar/anti-vibecode))

If you cite this skill, cite kloss first.

## Procedure

1. **Name the job in one sentence** — what the product does, for whom. If you cannot, you are not ready to write a hero.
2. **Pick three locked choices before markup:** display + body type pairing (not Inter/Geist-only), one accent from the product (not purple-to-blue), one layout that serves the job (not a bento of equal cards).
3. **Build or read the page.**
4. **Score all 30 tells.** Each is 0 or 1. No half points. A tell counts if a stranger would notice it in a 3-second scan.
5. **Ship rule:** `hits <= 5` → pass. `hits > 5` → fail. Do not present a failing page as done. List the hits, apply the replacements, re-score.
6. **Audit-only mode:** if the user asked for a review, return the scorecard and stop. Do not edit unless they say so.

Completion criterion: a 30-row scorecard with a total, and either `PASS (<=5)` or a fixed page that re-scores `PASS`.

## The 30 tells

Score 1 if present.

1. Purple, or purple fading into blue
2. Glowing orb behind the hero
3. Dot-grid background
4. Gradient on the headline text
5. Sparkle icon on anything AI
6. Glass card floating over a gradient
7. Icon in a tinted rounded square
8. An average bento grid
9. A clearly fake product screenshot
10. The only font is Inter or Geist
11. Standard Tailwind colors out of the box
12. Fake testimonials by fake avatars
13. "Trusted by" logos you did not close
14. A stats row of 10,000+ users and 99.9% uptime when traffic is tiny
15. "Powered by AI" badge in the nav
16. A waitlist form that goes nowhere
17. "It's not X, it's Y"
18. Em dashes everywhere
19. "Fast. Simple. Powerful." descriptors
20. Feature names that are two nouns (e.g. Seamless Workflow)
21. Three feature cards, identical text length
22. "Get started" sitting next to "Learn more"
23. Three pricing tiers with "Most popular" in the middle
24. $9 / $29 / $99 pricing structure
25. FAQ answering questions nobody asked
26. Mid hover and scroll animations
27. Hero copy that never says what it actually does
28. No loading or empty state — just blank
29. A blog link with no blog
30. A default favicon

None of these is individually forbidden. **More than five is the fail.**

## Replacements (use when a tell hits)

Visual (1–8, 10–11, 26): one real type pairing with character; paper and ink from the product (photo, packaging, logo), not a purple glow; flat or lightly textured ground; no orb, no dot grid, no glass-on-gradient, no sparkle-on-AI. Motion only if it explains state.

Proof (9, 12–16, 25, 29): real screenshot or none; real names or no testimonials; logos only with permission; stats only if true; waitlist only if it stores a real email; FAQ only from real questions; blog link only if posts exist.

Copy (17–22, 27): say the job in the hero in plain words. Feature names are verbs or outcomes. Card lengths may be uneven. One primary CTA that names the action. No "it's not X". No triad of empty adjectives.

Chrome (15, 23–24, 28, 30): no "powered by AI" chip; price what you actually charge; loading and empty states exist; a real favicon.

Honesty rule: if you do not have a metric, testimonial, logo, or screenshot, omit the section. Invented proof is a hit on 9, 12, 13, or 14.

## Pitfalls

- Restyling purple to indigo is still tell 1.
- Geist *and* Inter together still fail tell 10 if nothing else is used.
- A "handmade" bento with equal tiles is still tell 8.
- Replacing em dashes with spaced hyphens but keeping "Fast. Simple. Powerful." still fails 19.
- Passing 5 visual tells and failing 8 copy tells is still a fail — the cap is total hits, not category.
- Do not add tells that are not on this list and then claim the kloss score. Extra taste notes go in a separate paragraph, unlabeled as kloss.

## Verification

Return this block (fill every row):

```
anti-vibecode score  (source: kloss_xyz/2097808934442844307)
hits: <n> / 30    verdict: PASS (<=5) | FAIL (>5)
1-10:  ...
11-20: ...
21-30: ...
fixes applied: <ids or none>
```

PASS only if `hits <= 5` on the page you are handing back, not the page you started from.

## Install

```
hermes skills install https://raw.githubusercontent.com/shagghiesuperstar/anti-vibecode/main/skills/anti-vibecode/SKILL.md
```
