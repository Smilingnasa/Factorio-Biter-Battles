# Captains Skill Draft

This is the current Biter Battles scenario with Captains Skill Draft added as an alternative to the existing Captain mode. Both modes remain available in the Special games panel. Skill Draft uses the established Captain lobby and picking UI slots while keeping its own draft state and rating model.

## Start a live draft

1. Start the scenario and open the admin Special games panel.
2. Apply the Captains Skill Draft row; captain names are not entered in the selector.
3. Players choose `Join draft` in the lobby and may volunteer for the open North or South captain slot.
4. Players set effort from 0–100% in the lobby. Effort 0% is a 50% skill-cost discount; no larger discount is possible.
5. Once both captain slots are filled, the lobby operator starts the draft.
6. The captains pick from the visible list. The team with the lower current skill-based win probability receives the next pick.
7. After the draft, every player confirms a primary role and may select a secondary role.

## Bot playtest

An admin can run `/cpt-skill-test-start` from the in-game console. This selects 30 random players from the published seed leaderboard, uses their real seeded values, runs the entire draft and role-confirmation flow, and opens the results window. The bot playtest does not start a live map match.

The bot playtest is intentionally available only through the command, not as a live Special games selector option.

## Seed data

The bundled seed is generated offline from the Jimmy and cojito trusted-player sheets. It contains the published top 100 and the role columns used by the scenario. The seed builder and update instructions are kept separately in the `skill-seed-builder` bundle.

Unseeded players use the safe defaults: 50% win rate, 1.00 average unweighted role score, the corresponding default weighted role score, and default skill. No idle-match guardrail is applied to the seed.
