# onyx-rel-chaos-yard

`onyx-rel-chaos-yard` keeps a focused Solidity implementation around reliability. The project goal is to develop a Solidity command-oriented project for chaos scenarios with fixture event logs, golden state snapshots, and offline replay mode.

## Reason For The Project

I want this repository to be useful as a quick reading exercise: fixtures first, implementation second, verifier last.

## Onyx Rel Chaos Yard Review Notes

Start with `failure width` and `recovery gap`. Those cases create the widest score spread in this repo, so they are the best quick check when the model changes.

## What It Does

- `fixtures/domain_review.csv` adds cases for budget pressure and failure width.
- `metadata/domain-review.json` records the same cases in structured form.
- `config/review-profile.json` captures the read order and the two review questions.
- `examples/onyx-rel-chaos-walkthrough.md` walks through the case spread.
- The Solidity code includes a review path for `failure width` and `recovery gap`.
- `docs/field-notes.md` explains the strongest and weakest cases.

## How It Is Put Together

The fixture data drives the tests. The code stays thin, while `metadata/domain-review.json` and `config/review-profile.json` explain what each case is meant to protect.

The Solidity checks add a pure review lens and Foundry coverage.

## Run It

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File scripts/verify.ps1
```

## Check It

The verifier is intentionally local. It should fail if the fixture score math, lane assignment, or language-specific test drifts.

## Boundaries

The fixture set is small enough to audit by hand. The next useful expansion is malformed input coverage, not extra surface area.
