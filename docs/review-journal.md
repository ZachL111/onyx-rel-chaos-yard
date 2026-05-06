# Review Journal

The review surface for `onyx-rel-chaos-yard` is deliberately narrow: one fixture, one scoring rule, and one local check.

The local checks classify each case as `ship`, `watch`, or `hold`. That gives the project a small review vocabulary that matches its reliability focus without claiming live deployment or external usage.

## Cases

- `baseline`: `budget pressure`, score 204, lane `ship`
- `stress`: `failure width`, score 215, lane `ship`
- `edge`: `recovery gap`, score 159, lane `ship`
- `recovery`: `runbook drift`, score 185, lane `ship`
- `stale`: `budget pressure`, score 208, lane `ship`

## Note

A future change should add new cases before it changes the scoring rule.
