# LAN743x Netdev CI Results

Public NIPA-shaped test results for the Microchip **LAN7430 EVB rev 2.3**,
tested against `net-next-hw` snapshots on a 2-hour cadence from the
Hauppauge, NY lab.

**Temporary hosting:** GitHub Pages. Moves to Microchip AWS once the
hosting choice is finalized. Registration with NIPA Remotes happens after
the move so the URL is stable for `netdev.bots.linux.dev`.

## Layout

- `index.html` — polished dashboard (pass/fail matrix, per-test clickable logs)
- `results.json` — NIPA manifest (30 most recent runs)
- `runs/<YYYY-MM>/<branch>.json` — per-run NIPA JSON
- `logs/<YYYY-MM>/<branch>/<test>/stdout.txt` — raw test output, one dir per test
- `archive/<YYYY-MM>.json` — older manifest entries (rotated out after 60 days)
- `device.json` — NIPA device descriptor

## How it's populated

Results are pushed by `Testrunner.py` (from the internal
`sw-linux-patch-tests` harness) via the `lib/nipa_publish.py` helpers.
Each finished test cycle triggers one commit. Schema:
<https://github.com/linux-netdev/nipa/wiki/Netdev-CI-system>.

## Contact

Yuiko Oshino <yuiko.oshino@microchip.com>, Microchip Technology Inc.

---

*Assisted-by: Claude <claude-opus-4-7>*
