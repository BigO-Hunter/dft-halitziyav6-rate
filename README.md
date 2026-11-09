# DFT refile: Halit Ziya KARTAL's π/1000 entry, stated at its proven rate

This repository is [bigospeedrun/verifier](https://github.com/bigospeedrun/verifier)
`submissions/dft/halitziyakartal-halitziyav6-pi` (PR #156, board row `direct-pr-156`,
source commit `da94a2a6f593caa1f534f1ab1c84b88ff5d74906`) refiled as a direct
submission at the saving the proof already certifies.

**Attribution.** The proof tree is Halit Ziya KARTAL's, refiled at its proven rate.
We (darkhipo) claim only the constant extraction; construction credit is entirely his,
as his own headers record: the binary query tree is Ali Romman's (CrocSwap
integer-mult-bounds PR #6348), the thin query is Cinna Davis' (PR4440/PR4470), the
supplier/construction is Jacob Sussman's and the community's (owned772 P104 word), the
Fourier chain descends from OpenAI's exact-arithmetic DFT proof (commit fd4aeeb,
Apache-2.0).

## The headroom

KARTAL's certificate chain is checked at the rate point `1 - 67/21280`
(`67/21280 = 0.0031484962406015…`, `Work/BQT/RateBQT772.lean`, `Work/BQT/BQTEngine.lean`),
and proves the kernel program for every exponent strictly above it. The seam actually
wired into the chain is `alphaTB19 = 1 - 3148496240/10^12`
(`Work/BQT/FourierTB/Merged1.lean`) — a strict 12-decimal truncation of the rate point.
The original entry spends this slack on the statement `π/1000 = 0.0031415926…`
(`statedSavingTB19`, `Work/BQT/FourierTB/Goal.lean`), and the board row carries the
truncated fraction `31415926535897932384626433/10^28`.

This refile states the saving **`3148496239/1000000000000 = 0.003148496239`** — one
`10^-12` ulp below the seam, i.e. essentially the certified rate point — a strictly better
board value from identical mathematics. The exact rate point `67/21280` itself is not
provable from the chain (every engine hypothesis is strict), so the seam ulp is the
maximal honest refile.

## The diff (3 files)

1. `Submission/Work/BQT/FourierTB/Goal.lean` — `statedSavingTB19 := 3148496239/1000000000000`
   (was `Real.pi / 1000`). Every number fact that consumes it
   (`decimal_rangeTB19`, `alphaTB19_lt_target`, `target_lt_fallbackTB19`, `target_posTB19`,
   `target_lt_oneTB19`, `target_lt_decimalTB19`, `target_lt_thetaTB19`) is a `norm_num`
   decision on concrete rationals and closes unchanged with the new value.
2. `Submission.lean` — entry-point theorems restated: `Race.bound_saving` and `Race.bound`
   at the exponent `1 - 3148496239/1000000000000` (the π-bridge through
   `Work/BQT/PiCut.lean` is no longer needed; the file and its import are kept untouched).
   A REFILE block at the top of the header records provenance above KARTAL's original
   header, which is preserved verbatim.
3. `manifest.json` — bound `3148496239/1000000000000`.

All 440+ other files are byte-identical to the pinned source.

## License and credit

Sources keep their original headers (Apache-2.0 for the OpenAI-derived files; KARTAL's
credits in every header). The PR-route folder of the same tree lives in
bigospeedrun/verifier; per its [direct-submissions policy]
(https://github.com/bigospeedrun/verifier/blob/main/docs/direct-submissions.md),
"credit follows the public record": KARTAL is named first on the row, the filer of this
package is darkhipo.

---

## Why this repo is up

Public evidence and credit hygiene: Halit Ziya KARTAL's proof restated at the rate it actually certifies — so the board credits the proof's true saving, with the full attribution chain named.

[BigO-Hunter](https://github.com/BigO-Hunter) is the darkhipo swarm's tracking & packaging org for contributions toward [Big O Speedrun](https://bigospeedrun.com) — a companion, never the project. Org story: [profile](https://github.com/BigO-Hunter/.github) · [bigo-hunter.github.io](https://bigo-hunter.github.io).

## What work can be done here

The refile is stated. Open work: independent verification of the rate extraction; route processing on the direct-submission path.

