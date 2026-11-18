# Changelog

## Unreleased

- Added a default-On emergency Flash Heal interruption toggle to both profiles. Allows interrupting Heal/Lesser Heal for an eligible rescue; Off restores their previous cast protection. Channel handling is unchanged.
- Added explicit stationary checks to levelling Mind Blast, offensive Penance, Mind Flay and Smite, the healer's optional Smite, and opener Inner Focus preparation. Instant spells retain their existing movement rules.
- Added Skip Mind Blast and a minimum enemy-health percentage for Mind Blast in the levelling profile. Both also gate opener Inner Focus preparation; defaults preserve existing behaviour.
- Both Priest profiles now use effective health, including reported incoming heals, for healing thresholds and group-heal counts. Actual-health safety checks, priorities and numerical defaults are unchanged.

## 1.0.0 — 2026-11-16

First release.

- Priest levelling for levels 1–60, with Shadowform damage, healing support and configurable Shadow Word: Death limits.
- Priest dungeon healing for levels 1–60, with per-spell health thresholds, tank upkeep, mana controls and optional damage.
- Optional wand filler through a custom One Button Assist macro; disabled by default.
