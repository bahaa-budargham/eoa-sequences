
# English Encodings

Pre-convergence sequences for the English alphabet under the EOA-43 deterministic symbolic representation.

Six English phonetic encodings are documented here. Each encoding produces a different limiting constant ratio (LCR). Within a single encoding, the 26 letters collapse into 16 distinct sequence groups.

## Encodings

| Folder | LCR | Notes |
| :--- | :--- | :--- |
| [`primary-LCR-3.306/`](./primary-LCR-3.306/) | 3.306 | Baseline English phonetic encoding |
| [`modified-1-LCR-3.037/`](./modified-1-LCR-3.037/) | 3.037 | First modification |
| [`modified-2-LCR-3.173/`](./modified-2-LCR-3.173/) | 3.173 | Second modification |
| [`modified-3-LCR-2.689/`](./modified-3-LCR-2.689/) | 2.689 | Third modification |
| [`modified-4-LCR-3.209/`](./modified-4-LCR-3.209/) | 3.209 | Fourth modification |
| [`modified-5-LCR-3.14159/`](./modified-5-LCR-3.14159/) | 3.141593223577 | Fifth modification, the pi run |

## About the LCR

The LCR is the value that the ratio of consecutive terms approaches as the sequence grows. It is encoding dependent. Changing the phonetic mapping of the alphabet changes the LCR. The values above span from 2.689 to 3.306, a spread of about 1.2x.

The `modified-5` encoding produced a value of approximately 3.141593223577, which agrees with pi to five decimal places. This is an empirical observation, not a proof that the limit equals pi. See the supplementary note "Toward pi by Phonetic Encoding" (2026).

## Contents of Each Encoding Folder

| File | Purpose |
| :--- | :--- |
| `README.md` | Encoding details, LCR, source |
| `mapping.json` | Letter to group assignment |
| `terms/` | Sequence files, one per distinct group |

## Why 16 Groups, Not 26 Letters

Within one encoding, several letters produce an identical sequence. For example, under the English primary encoding, the letters b, d, p, t, v and z share one sequence, the letters f, l, m, n and s share another, and the letters i and r share a third. The remaining 13 letters are singletons.

That gives 16 distinct groups per encoding.

Group membership is not guaranteed to be the same across encodings. Always read `mapping.json` inside the specific encoding folder.

## Cross Encoding Comparison

| Encoding | LCR | Difference from pi |
| :--- | :--- | :--- |
| modified-1 | 3.037 | — |
| modified-2 | 3.173 | — |
| modified-3 | 2.689 | — |
| modified-4 | 3.209 | — |
| modified-5 | 3.141593223577 | approx. 5.70e-7 |

## Disclosure

Only the outputs are published here. The deterministic operator that generates these sequences is not disclosed. It is available to qualified researchers under the terms described in EOA Part I, Section 2.

## Related Work

- EOA Program, Part 0: The Engineering of Alphabets as an Open Frontier
- EOA Program, Part I: EOA-43, A Rank-Collapsed Deterministic Symbolic Representation
- EOA Program, Supplementary Note: Toward pi by Phonetic Encoding

## Contact

bdarghamneurolabs@gmail.com
