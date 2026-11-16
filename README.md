# Forever Priest rotations

Custom Priest rotations for **WoW Forever, levels 1–60**.

| Rotation | Purpose |
| --- | --- |
| Priest Levelling (`priest-levelling.yaml`) | Solo levelling with conditional Shadowform damage and healing support. |
| Priest Dungeon Heal (`priest-levelling-dungeon-heal.yaml`) | Dungeon healing with per-spell health thresholds and optional damage. |

## Setup

1. Use an existing Forever setup with its shared rotation data.
2. Copy the desired YAML files into `<application folder>/forever/custom/` or `<application folder>/forever/`.
3. Select the profile in the rotation selector and review its settings and bindings before combat.

These profiles are for Forever, not retail. Spell rank selection is automatic.

## Custom settings

The tables list this release's defaults and adjustment ranges. Saved settings can
retain older values. Health percentages refer to the intended recipient unless
the setting says otherwise. Raising a healing threshold makes that heal eligible
earlier; lowering it waits for more injury. Eligibility does not guarantee a cast:
earlier priorities, movement, spell availability, range and bindings still matter.
The defaults are starting points, not promises of optimal mana use.

### Priest Levelling

Leave Shadowform manually when healing is needed. Devouring Plague and Mind Flay
require active Shadowform. Routine direct heals run before Renew and damage.

| Setting | Default (range) | What it controls |
| --- | --- | --- |
| Wand | Off | Requires a custom One Button Assist wand macro and binding. Enables wand filler and suppresses offensive Penance and Smite. Pain, Mind Blast, Death, Plague and Mind Flay remain eligible; Mind Flay can take the filler slot before the wand. |
| Emergency health percent | 35% (10–50%) | Below this, prioritise available self/party rescue spells. Most damage requires your health at or above it; Death also has its own minimum. |
| Direct heal health percent | 50% (20–80%) | In combat, try available self Flash Heal, Heal or Lesser Heal below this health. Also controls the moving self-shield threshold. |
| Party member heal health percent | 50% (20–80%) | In combat, try direct heals, then missing Renew, on other party members below this health. Emergency assistance uses the emergency threshold instead. |
| Renew health percent | 70% (30–90%) | Apply missing Renew to yourself below this health in combat, outside Shadowform. |
| Out-of-combat heal health percent | 70% (0–95%) | Below this, try stationary Heal/Lesser Heal outside combat and Shadowform. Also sets the minimum health for automatically restoring Shadowform, including in combat. |
| Shield in combat | On | Maintain your missing shield in combat whenever Weakened Soul permits, regardless of health. Turning it Off leaves emergency and low-health moving shields enabled. |
| Emergency Psychic Scream | Off | Allow fear below your emergency health threshold with at least two combat enemies within 8 yards. Enable only when fleeing enemies will be safe. |
| Automatic Holy Nova | Off | Allow Nova in the moving-action list with at least two combat enemies within 10 yards, outside Shadowform and above the emergency health floor. This list is called while moving. Enable only when nearby enemies are safe to hit. |

**Shadow Word: Death** has its own settings section:

| Setting | Default (range) | What it controls |
| --- | --- | --- |
| Enemy health limit (HP) | 300 HP (0–5000) | Allow Death at or below this remaining enemy HP. Set to 0 to disable this condition. |
| Use below 20% (Early Demise) | Off | Independently allow Death below 20% enemy health, even above the absolute limit or when that limit is 0. Enable deliberately for Early Demise builds; this does not detect the talent. |
| Minimum player health percent | 40% (31–100%) | Both Death modes require your health at or above this and the emergency threshold, and strictly above 30%. |

Death is the first damage priority, after the earlier healing actions. To disable
automatic Death, set the enemy HP limit to 0 **and** leave the under-20% toggle Off.
A failed kill costs 30% of maximum health; these checks do not predict incoming
damage, so they cannot guarantee survival.

### Priest Dungeon Heal

Select your tank, verify member/self bindings and start with optional damage and
general party Renew Off. The selected tank is tried before role-based tank
fallbacks; selecting one does not exclude other detected tanks.

**Healing controls:**

| Setting | Default (range) | What it controls |
| --- | --- | --- |
| Tank target | Select up to one member | Choose who receives the selected-tank shield, Renew and Mending upkeep attempts. Role-based tank fallbacks remain active. |
| Mouseover healing | Off | Allow direct heals on a living friendly unit frame under the mouse, within 40 yards (36 for Penance). Emergency healing runs first; mouseover uses the normal per-spell thresholds. |
| Routine party Renew | Off | Enable general stationary party Renew and later moving top-ups. Does not disable tank Renew or the earlier moving rescue Renew. |
| Emergency support health percent | 35% (10–60%) | Group-lowest threshold for attempted emergency Shadowform cancellation and optional Inner Focus. Does not replace individual rescue thresholds. |
| Desperate Prayer health percent | 35% (0–100%) | Your health threshold for self-rescue with Desperate Prayer. |
| Emergency Power Word Shield health percent | 35% (0–100%) | Rescue shield threshold, respecting existing shields and Weakened Soul. |
| Emergency Flash Heal health percent | 35% (0–100%) | High-priority Flash Heal threshold. |
| Emergency Heal health percent | 35% (0–100%) | High-priority Heal threshold. |
| Emergency Lesser Heal health percent | 35% (0–100%) | High-priority Lesser Heal fallback threshold. |
| Divine Grace health percent | 35% (0–50%) | Rescue threshold for another member; also strictly requires their health below 50%. Never targets yourself. |
| Emergency Penance health percent | 35% (0–100%) | High-priority stationary Penance threshold. |
| Penance health percent | 60% (0–100%) | Routine stationary Penance threshold, also used for mouseover. |
| Flash Heal health percent | 40% (20–90%) | Routine stationary Flash Heal threshold, including mouseover. Requires the mana-conservation floor. |
| Greater Heal health percent | 55% (0–100%) | Routine stationary Greater Heal threshold, also used for mouseover. |
| Heal health percent | 75% (40–95%) | Routine stationary Heal threshold, also used for mouseover. |
| Lesser Heal health percent | 75% (0–100%) | Routine stationary Lesser Heal fallback threshold, also used for mouseover. |
| Renew health percent | 90% (50–100%) | Missing Renew threshold for tank maintenance and optional stationary party Renew. |
| Tank shield health percent | 90% (50–100%) | Tank upkeep shield threshold. Requires combat, the mana floor and no shield/Weakened Soul. |
| Prayer of Healing health percent | 70% (40–95%) | Count members below this health toward the group-heal trigger. Requires enough injured members, the mana floor and standing still. |
| Holy Nova injured-member health percent | 70% (0–100%) | Count injured members within 10 yards for Nova. Also requires its toggle, combat, the mana floor and the group-heal count. |
| Prayer of Mending maximum health percent | 100% (0–100%) | Tank upkeep allows Mending at or below this health, only when no member has an active Mending buff. Requires combat and the mana floor. |
| Moving priority Renew health percent | 60% (0–100%) | Early moving rescue: apply missing Renew below this health, independently of routine party Renew and the mana floor. |
| Moving top-up Renew health percent | 80% (0–100%) | Later moving Renew top-ups below this health; requires routine party Renew and the mana floor. Can run between pulls. |
| Group heal injured members | 3 (2–5) | Required injured-member count for both Prayer of Healing and automatic Holy Nova. |

Healing thresholds use **below**, except Mending's **at or below**. Where a
strict-below threshold allows 0, that disables its trigger, not every other use
of the same spell. Mending's health limit is not an Off toggle.
Emergency and routine settings are separate because emergency actions run earlier
and may interrupt casts. Existing channel protection can still delay healing.

Routine direct-heal order is Penance, Flash Heal, Greater Heal, Heal, then Lesser
Heal. Lowering Flash Heal's routine threshold can reduce its use; increasing the
mana floor does not suppress the other direct heals. Tank upkeep runs after these
heals, so a tank needing direct healing can delay Renew or Mending upkeep.

**Mana, damage, buffs and utility:**

| Setting | Default (range) | What it controls |
| --- | --- | --- |
| Conserve below mana percent | 30% (0–50%) | Below this, withhold routine Flash Heal, group heals, tank upkeep, general party Renew, moving top-ups and combat maintenance buffs. Emergency healing, earlier moving rescue Renew and other direct heals remain eligible. Out-of-combat maintenance buffs are not restricted by this floor. |
| Mana-spending damage | Off | Allow Pain and Smite in combat when both damage health/mana conditions pass. Wand is independent. |
| DPS minimum group health percent | 90% (0–100%) | Every member must be at or above this for paid damage or a new wand-start action. This does not stop an already active wand attack when group health drops. |
| DPS minimum mana percent | 60% (50–100%) | Minimum mana for Pain/Smite. Does not restrict wand filler. |
| Wand | Off | Requires a custom One Button Assist wand macro and binding. Enables healthy-group wand filler and suppresses Smite, including when paid damage is On. Pain remains eligible when paid damage is enabled. |
| Automatic emergency Inner Focus | On | Allow available Inner Focus in combat, outside Shadowform, below the emergency support threshold. |
| Automatic Fade when holding threat | On | Allow Fade in combat when target threat is at least 3 or maximum nameplate threat is at least 2. |
| Maintain party buffs | On | Maintain missing Fortitude and Divine Spirit on members; also Shadow Protection when enabled. Can run in combat when the mana floor permits. Self-maintenance attempts remain when this is Off. |
| Maintain Shadow Protection | Off | Enable missing Shadow Protection on yourself and, when party buffs are enabled, other members. |
| Automatic Holy Nova | Off | Enable the Nova group-heal conditions above. Keep Off unless nearby enemies are safe to hit. |

### Shared controls and bindings

These tables cover the profiles' own settings. Additional shared settings cover
targeting, combat, consumables and resurrection. In the levelling profile,
**Auto Target (Ranged)** enables replacement targeting for the selected situations
(no target, dead target or distant target); clear those choices if you want manual
enemy targeting. **Auto Combat: Off** prevents out-of-combat hover pulls in that
profile; it is not a master switch for every buff or healing action.

Spells need working bindings for the intended recipient. The healer uses general
member cycling, while levelling party assistance uses party cycling; neither
profile creates missing bindings. Mouseover healing/resurrection needs the
matching mouseover bindings. Leave Wand Off unless you have configured the custom
One Button Assist macro. A missing-keybind message is a setup issue to investigate,
not something a higher health threshold fixes.

## Release status

First release: **1.0.0**. Release notes are in `CHANGELOG.md`.

Static validation does not certify in-game behaviour. Verify self/member healing
bindings, emergency response during channels and Prayer of Healing recipient
coverage before relying on these profiles in difficult content.
