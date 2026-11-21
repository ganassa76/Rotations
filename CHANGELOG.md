# Changelog

## 1.2.0 — 2026-11-21

### Dungeon healing

- Missing tank Renew takes priority over routine Heal and Lesser Heal.
- **Holy Binding talented** defaults on. When both you and an ally need Flash Heal, the rotation can heal both with an ally-targeted cast. During an emergency it prefers the ally only if their effective health percentage is at or below yours. Turn this setting off if you lack the talent.
- Prayer of Healing and Flash Heal remain available below the mana-conservation floor when affordable. Prayer checks the priest first as its centre and can use Inner Focus.
- Automatic Holy Nova defaults on for priests who know it. While moving, it precedes Renew when enough nearby members are injured. At low mana, urgent group Nova, moving tank Shield and Renew on a substantially injured tank remain available.

### Shadow dungeon DPS

- Shadow Word: Death takes first damage priority at **300 remaining enemy HP or less** by default. The optional Early Demise setting also allows it below 20% enemy health. Both require the priest to be above 50% health and meet the configured personal minimum.
- Otherwise, an available Mind Blast opens after engagement when the cast can finish. Mind Blast stays eligible at high threat, with Fade available for threat relief.
- Missing DoTs no longer depend on an estimate of enemy lifetime. Mouseover Pain no longer requires 30% mana. Vampiric Embrace follows the higher-priority damage spells.

### Solo levelling

- Routine self and party healing tries Heal, then Lesser Heal, then Flash Heal. Emergency Flash Heal keeps its priority.
- Mind Flay uses the normal spell range check, removing the fixed 20-yard cutoff.

## 1.1.0 — 2026-11-19

- Added a level 60 Shadow dungeon DPS profile and a 13/0/38 talent build for five-player groups. Mouseover Pain defaults on, Silence defaults to manual, and Shadow Word: Death uses the priest's own health with a default cutoff above 50%.
- Dungeon healing now uses Penance up to 40 yards on allies. Emergency Inner Focus considers incoming heals and range. Prayer of Healing targets the priest, counts nearby injured members and can use an active Inner Focus below the mana floor.
- Documented the agreed 21/30/0 starter dungeon-healing build, current priority limitations and five in-game checks.
- Mouseover Pain in the levelling profile now requires combat, preventing automatic out-of-combat hover pulls. Current-target Pain is unchanged.
- Added a default-On emergency Flash Heal interruption toggle to the levelling and dungeon-healing profiles. Turn it off to protect existing Heal and Lesser Heal casts from emergency Flash Heal.
- Added explicit stationary checks to levelling Mind Blast, offensive Penance, Mind Flay and Smite, the healer's optional Smite, and opener Inner Focus preparation. Instant spells retain their existing movement rules.
- Added Skip Mind Blast and a minimum enemy-health percentage for Mind Blast in the levelling profile. Both also gate opener Inner Focus preparation; defaults preserve existing behaviour.
- Levelling and dungeon-healing health thresholds and group-heal counts now account for reported incoming healing.

## 1.0.0 — 2026-11-16

First release.

- Priest levelling for levels 1–60, with Shadowform damage, healing support and configurable Shadow Word: Death limits.
- Priest dungeon healing for levels 1–60, with per-spell health thresholds, tank upkeep, mana controls and optional damage.
- Optional wand filler through a custom One Button Assist macro; disabled by default.
