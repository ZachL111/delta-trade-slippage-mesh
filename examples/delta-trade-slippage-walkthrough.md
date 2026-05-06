# Delta Trade Slippage Mesh Walkthrough

This note is the quickest way to read the extra review model in `delta-trade-slippage-mesh`.

| Case | Focus | Score | Lane |
| --- | --- | ---: | --- |
| baseline | spread pressure | 123 | watch |
| stress | fill risk | 106 | watch |
| edge | portfolio drift | 129 | watch |
| recovery | quote width | 176 | ship |
| stale | spread pressure | 126 | watch |

Start with `recovery` and `stress`. They create the widest contrast in this repository's fixture set, which makes them better review anchors than the middle cases.

`recovery` is the optimistic case; use it to make sure the scoring path still rewards strong signal.
