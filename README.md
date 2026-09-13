# EOA Sequences

Public pre-convergence sequences for the Engineering of Alphabets (EOA) program.

The EOA program studies a deterministic recursive operator that maps spoken letter names into numerical sequences. Each sequence converges to a language and encoding specific limiting constant ratio (LCR). Within a single encoding, the 26 letters of an alphabet collapse into 16 distinct sequence groups.

This repository collects those sequences in a structured, citable form.

## Structure

Sequences are organized by language, then by encoding variant.

```
eoa-sequences/
├── README.md
├── english/
│   ├── README.md
│   ├── primary-LCR-3.306/
│   ├── modified-1-LCR-3.037/
│   ├── modified-2-LCR-3.173/
│   ├── modified-3-LCR-2.689/
│   ├── modified-4-LCR-3.209/
│   └── modified-5-LCR-3.14159/
├── arabic/
│   ├── README.md
│   └── primary/
├── hebrew/
│   ├── README.md
│   └── primary/
└── greek/
    ├── README.md
    └── primary/
```

## English Encodings

| Folder | LCR | Notes |
| :--- | :--- | :--- |
| `primary-LCR-3.306` | 3.306 | Baseline English phonetic encoding |
| `modified-1-LCR-3.037` | 3.037 | First modification |
| `modified-2-LCR-3.173` | 3.173 | Second modification |
| `modified-3-LCR-2.689` | 2.689 | Third modification |
| `modified-4-LCR-3.209` | 3.209 | Fourth modification |
| `modified-5-LCR-3.14159` | 3.141593223577 | Fifth modification, the π run |

The `modified-5` encoding is documented in the supplementary note "Toward π by Phonetic Encoding." Its LCR agrees with π to five decimal places. It is an empirical observation, not a proof that the limit equals π.

## Other Languages

| Language | Encodings |
| :--- | :--- |
| Arabic | primary |
| Hebrew | primary |
| Greek | primary |

## Contents of Each Encoding Folder

| File | Purpose |
| :--- | :--- |
| `README.md` | Encoding details, LCR, source paper, date |
| `mapping.json` | Letter to group assignment for this encoding |
| `terms/` | 16 text files, one per distinct sequence group |

## Why 16 Files, Not 26

Within a single encoding, several letters produce an identical sequence. For example, under the English primary encoding, the letters b, d, p, t, v and z share one sequence, the letters f, l, m, n and s share another, and the letters i and r share a third. The remaining 13 letters are singletons.

That gives 16 distinct groups per encoding.

Group membership can change between encodings. Always read `mapping.json` inside the specific encoding folder for the authoritative grouping.

## Terms File Format

Each file inside `terms/` contains the pre-convergence sequence for that group, one term per line, in order. Files are plain text so they can be read by any tool.

Example, `terms/group-BDPTVZ.txt` under the English primary encoding:

```
1
3
8
26
77
242
766
2420
...
```

## Example mapping.json

```json
{
  "language": "english",
  "encoding": "modified-5",
  "lcr": 3.141593223577,
  "source": "Toward π by Phonetic Encoding (2026)",
  "groups": {
    "group-BDPTVZ": ["b", "d", "p", "t", "v", "z"],
    "group-FLMNS": ["f", "l", "m", "n", "s"],
    "group-IR": ["i", "r"],
    "singletons": ["a", "c", "e", "g", "h", "j", "k", "o", "q", "u", "w", "x", "y"]
  }
}
```

## Disclosure

Only the outputs are published here. The deterministic operator that generates these sequences is not disclosed. It is available to qualified researchers under the terms described in EOA Part I, Section 2.

Some encodings in this repository are released as public exceptions. The remaining 43-term sequences and extended runs stay under the access terms described in EOA Part I, Section 2.

## Citation

BuDargham, B. (2026). EOA Sequences. GitHub.
https://github.com/bahaa-budargham/eoa-sequences

## Related Work

- EOA Program, Part 0: The Engineering of Alphabets as an Open Frontier
- EOA Program, Part I: EOA-43, A Rank-Collapsed Deterministic Symbolic Representation
- EOA Program, Supplementary Note: Toward π by Phonetic Encoding

## Contact

bdarghamneurolabs@gmail.com
