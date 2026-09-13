# English — Modified #5 (LCR ≈ 3.14159)

Fifth modified English phonetic encoding in the EOA-43 deterministic symbolic representation.

## LCR

Approximately **3.141593223577**.

This value agrees with pi to five decimal places under ordinary rounding. It differs from pi by about 5.70 x 10^-7.

This is an empirical observation, not a proof that the limit equals pi. The sequence has not been classified as a pi-generating sequence. The proximity is a measured property of this particular encoding.

## Source

B. BuDargham, *The EOA Program, Supplementary Note: Toward pi by Phonetic Encoding*, 2026.

The supplementary note reports three observations from this encoding:

1. The ratio of consecutive terms reaches 3.14159 by term 24.
2. By term 50, the ratio is approximately 3.141593223577.
3. At n = 499, 128 decimal positions remained stable across a window of 8 consecutive ratios.

These are numerical diagnostics, not proofs of the limiting value.

## Contents

| File | Purpose |
| :--- | :--- |
| `README.md` | This file. Encoding details, LCR, source. |
| `mapping.json` | Letter to group assignment for this encoding. |
| `terms/` | Sequence files, one per distinct group. |

## Groupings Are Encoding Dependent

**Important:** The 26 letters do not group the same way in every encoding. The set of letters that share a sequence changes when the phonetic mapping changes.

For example:

- In the primary encoding, the group BDPTVZ contains b, d, p, t, v, z.
- In the modified-5 encoding, the groupings are different:
  - **B = F = M = S** share one sequence.
  - **L = N** share one sequence.
  - **T = V** share one sequence.
  - **I = R** share one sequence.

Because of this, the number of distinct groups is not fixed at 16. It varies by encoding.

**In this encoding (modified-5), there are 20 distinct sequence groups.**

Always read `mapping.json` in the encoding folder for the authoritative grouping. Do not assume grouping carries over from one encoding to another.

## Terms Folder

Each file in `terms/` contains the pre-convergence sequence for one distinct group in this encoding.

| File | Letters sharing this sequence |
| :--- | :--- |
| `terms/sequence_bfms.json` | b, f, m, s |
| `terms/sequence_ln.json` | l, n |
| `terms/sequence_tv.json` | t, v |
| `terms/sequence_ir.json` | i, r |
| `terms/sequence_a.json` | a |
| `terms/sequence_c.json` | c |
| ... | ... |

Files are named for the letters in the group. Singletons have their own file. The full list is in `mapping.json`.

## File Format

Each `terms/*.json` file follows this structure:

```json
{
  "language": "english",
  "encoding": "modified-5",
  "lcr": 3.141593223577,
  "group": "bfms",
  "letters": ["b", "f", "m", "s"],
  "terms": [1, 3, 8, 26, 86, 276, 869, 2719]
}
```

- `terms` contains the sequence starting from the seed at index 0.
- Terms are integers, listed in order.
- Extended runs (500 or more terms) are available under access terms described in EOA Part I, Section 2.

## How to Generate a Word Vector

The full method is described in EOA Part I. In short:

1. Load the letter sequences for all letters in a word.
2. Apply position and index weighting.
3. Sum the weighted sequences.

For anagrams such as *own*, *won*, and *now*, the weighting produces distinct vectors despite identical letter content. See the `EOA_comparison.html` tool for a working implementation.

## Relation to Other Encodings

The same letter t under other English encodings produces different sequences and different LCRs:

| Encoding | LCR |
| :--- | :--- |
| primary | 3.306 |
| modified-1 | 3.037 |
| modified-2 | 3.173 |
| modified-3 | 2.689 |
| modified-4 | 3.209 |
| **modified-5** | **3.141593223577** |

A single phonetic change in the mapping shifted the LCR from about 3.2099 to 3.141593223577. The paper reports this as an observation, not a method.

## OEIS

The letter t sequence for this encoding is drafted on OEIS as [A399854](https://oeis.org/A399854).

## Disclosure

Only the outputs are published here. The deterministic operator that generates these sequences is not disclosed. It is available to qualified researchers under the terms described in EOA Part I, Section 2.

## Citation

BuDargham, B. (2026). EOA Sequences: English Modified #5. GitHub.
https://github.com/bahaa-budargham/eoa-sequences/tree/main/english/modified-5-LCR-3.14159

## Related Work

- EOA Program, Part 0: The Engineering of Alphabets as an Open Frontier
- EOA Program, Part I: EOA-43, A Rank-Collapsed Deterministic Symbolic Representation
- EOA Program, Supplementary Note: Toward pi by Phonetic Encoding

## Contact

bdarghamneurolabs@gmail.com
