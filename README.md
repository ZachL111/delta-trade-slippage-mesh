# delta-trade-slippage-mesh

`delta-trade-slippage-mesh` explores trading systems with a small Zig codebase and local fixtures. The technical goal is to design a Zig verification harness for slippage systems, covering stream reduction, windowed input fixtures, and failure-oriented tests.

## Why It Exists

This is intentionally local and self-contained so it can be inspected without credentials, services, or seeded history.

## Delta Trade Slippage Mesh Review Notes

For a quick review, compare `quote width` with `fill risk` before reading the middle cases.

## Features

- `fixtures/domain_review.csv` adds cases for spread pressure and fill risk.
- `metadata/domain-review.json` records the same cases in structured form.
- `config/review-profile.json` captures the read order and the two review questions.
- `examples/delta-trade-slippage-walkthrough.md` walks through the case spread.
- The Zig code includes a review path for `quote width` and `fill risk`.
- `docs/field-notes.md` explains the strongest and weakest cases.

## Architecture Notes

The core code exposes a scoring path and the added review layer uses `signal`, `slack`, `drag`, and `confidence`. The domain terms are `spread pressure`, `fill risk`, `portfolio drift`, and `quote width`.

The Zig code keeps the review rule close to the tests.

## Usage

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File scripts/verify.ps1
```

## Tests

The verifier is intentionally local. It should fail if the fixture score math, lane assignment, or language-specific test drifts.

## Limitations And Roadmap

The repository is intentionally scoped to local checks. I would expand it by adding adversarial fixtures before adding features.
