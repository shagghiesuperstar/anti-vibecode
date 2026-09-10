# anti-vibecode

Hermes Agent skill that turns [@kloss_xyz](https://x.com/kloss_xyz)'s 30-tell "your site looks vibecoded" list into a hard ship gate.

**More than five hits and everyone will know.**

Original post: [x.com/kloss_xyz/status/2097808934442844307](https://x.com/kloss_xyz/status/2097808934442844307)

This repo packages that list. Credit kloss for the tells. Scott ([shagghiesuperstar](https://github.com/shagghiesuperstar)) only wrapped them as a skill.

## Install (Hermes)

```bash
hermes skills install https://raw.githubusercontent.com/shagghiesuperstar/anti-vibecode/main/skills/anti-vibecode/SKILL.md
```

Tap (searchable from your hub sources):

```bash
hermes skills tap add shagghiesuperstar/anti-vibecode
hermes skills install anti-vibecode
```

## What it does

Before a landing page ships, the agent scores 30 tells (purple-to-blue, glowing orb, Inter/Geist-only, fake testimonials, $9/$29/$99, hero copy that never says what it does, …). If the count is over five, it is not done. It has to fix and re-score.

## Files

- `skills/anti-vibecode/SKILL.md` — the skill

## License

MIT. The 30-tell list remains attributed to [@kloss_xyz](https://x.com/kloss_xyz).
