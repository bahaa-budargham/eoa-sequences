## Terms Folder

Each file in `terms/` contains only the first **34 terms** of the pre-convergence sequence for one distinct group in this encoding.

The complete sequence and its rational generating function are available under agreed collaboration. See the Disclosure section for details.

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

Each `terms/*.json` file follows this structure. Only the first 34 terms are included.

```json
{
  "language": "english",
  "encoding": "modified-5",
  "lcr": 3.141593223577,
  "group": "tv",
  "letters": ["t", "v"],
  "terms": [1, 3, 8, 26, 86, 276, 869, 2719, ... 34 terms total ...],
  "collaboration": "Complete sequence and rational generating function available under agreed collaboration."
}
