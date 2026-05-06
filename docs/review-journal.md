# Review Journal

The review surface for `delta-trade-slippage-mesh` is deliberately narrow: one fixture, one scoring rule, and one local check.

The local checks classify each case as `ship`, `watch`, or `hold`. That gives the project a small review vocabulary that matches its trading systems focus without claiming live deployment or external usage.

## Cases

- `baseline`: `spread pressure`, score 123, lane `watch`
- `stress`: `fill risk`, score 106, lane `watch`
- `edge`: `portfolio drift`, score 129, lane `watch`
- `recovery`: `quote width`, score 176, lane `ship`
- `stale`: `spread pressure`, score 126, lane `watch`

## Note

The repository should be understandable without pretending it is larger than it is.
