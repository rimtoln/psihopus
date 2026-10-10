# How Psihopus works

One HTML file: layout, styles and the floor simulation. No build step.

## Pipeline

Every mint is a bubble from the vent.

1. Spawn every 0.28–0.44 s at the vent.
2. Rise to the sniff line (`y = 440`).
3. **Sniff.** `cleanRate = 0.18`.
   - Dirty: tagged `DEV %` / `BUNDLES` / `TOP10` / `LATE` / `SHILL` and skipped.
   - Clean + free arm: that arm reaches (0.55 s) and carries (0.6 s) to its seat.
   - Clean + no free arm: tagged `NO FREE ARM` and drifts off.
4. **Hold** 6–13 s on the seat card: MC sparkline, curve %, size in SOL.
5. **Close** one of three ways:
   - `TP` — take profit into KOTH, coins burst, gold stamp.
   - `INK` — dev wallet closing on sonar, ink jet from the siphon, violet stamp.
   - `RUG` — dumped, red flash, limp arm.

Odds: TP 68% · INK 22% · RUG 10%.

## Seats

Eight cards, four on each side. States: `empty` → `reach` → `hold` → `exit` → `empty`.

While holding, sonar contacts orbit the seat. The red `dev` contact closes in before an ink or a rug. Organic and sniper wallets stay on the ring.

## Octopus

Body, siphon, eight Bézier arms with suckers. Skin color follows mood:

| Mood | When |
|---|---|
| CALM | idle |
| GRABBING | an arm is reaching |
| HYPED | average open seat is up >35% |
| PAYDAY | a TP just printed |
| INKING | an ink escape just fired |
| SCARED | a rug just hit |

Eyes track the last grab or close. Blink is independent.

## Panels

- **SONAR** — 8 sectors, sweep, contact counts, nearest dev in seconds.
- **VENT FUNNEL** — 60 s bars: vented / clean / grabbed / closed, skip reasons.
- **ARM HEATMAP** — 22 cells per arm, win % on the right, best arm called out.
- **CATCH LOG** — newest row at top, mix bar TP / INK / RUG, average hold.
- **TIDE** — equity since deploy.
- **INK SAC** — fill level, escapes ready (`floor(ink/30)`).

## Numbers in the header

Arms busy, session PnL, ink %, SOL price, UTC clock, depth in meters. All-time PnL on the tide panel is the wallet `7XKP···9QF2` running total.
