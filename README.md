# Verify Before You Trust It, Even Yourself

A Cross-Vendor Quantum Hardware Case Study

**Lokesh Pullakandam¹, Jack Woehr²**

¹ Independent Researcher (B.A. Computing and Informatics, Rowan University,
December 2025). Corresponding author: lokeshpullakandam123@gmail.com
² Seiden Group; IBM Champion 2021–2026; Secretary, OpenQASM Technical
Steering Committee

## Status

Intermediate result — see the paper's own Discussion and Conclusion for
explicit scope and open questions. Independently verification-checked
against the underlying repos and live job data.

## Abstract

We built a verification tool whose only job is to check that a quantum
circuit which actually runs on real hardware is the circuit that was
intended, before trusting anything it reports. Pointed at our own work,
it immediately found five real bugs, including one that had already
silently produced a wrong number we had previously trusted, and one case
where it correctly found nothing wrong at all. Only once those bugs were
fixed did we trust an actual physics comparison: the same graded
entangling circuit, run twice each on real IBM and real IonQ hardware,
with the final matched repeat pair submitted 26 seconds apart. IonQ's
five-qubit ring circuit showed a genuine 51% swing in amplification
between its two runs; IBM's held steady within 0.4% between its own two
runs. We also report a smaller, negative-but-useful finding: an exact
classical calculation shows a circuit's abstract entanglement, on its
own, does not predict how much its result degrades on real hardware — the
number of physical two-qubit gates it needs does. We present this work as
an intermediate result: a real, checkable methodology and two real
findings, with several explicitly-scoped follow-up experiments still
open.

## Files

- `Verify_Before_You_Trust_It_Even_Yourself.pdf` — the paper.
- `paper.md` — the paper's Markdown source.

## Data

The circuits, job IDs, and raw results behind this paper's physics
comparison are a separate, dedicated public release:
[ionq-ibm-cross-vendor-data](https://github.com/Lokesh-2025/ionq-ibm-cross-vendor-data),
archived on Zenodo at DOI
[10.5281/zenodo.23543567](https://doi.org/10.5281/zenodo.23543567).

## Related

- [quantum-verifier](https://github.com/Lokesh-2025/quantum-verifier) — the verification tool this paper is about.
- [quantum-hardware-mcp](https://github.com/Lokesh-2025/quantum-hardware-mcp) — the MCP server / snapshot pipeline.
- [singmasters-conjecture](https://github.com/Lokesh-2025/singmasters-conjecture) — the earlier Singmaster's Conjecture work referenced in the Introduction.
