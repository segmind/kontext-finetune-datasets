# kontext-finetune-datasets
Datasets for kontext finetuning

 - [Bigger Head](./bigger-head)
 - [Hat overlay](./hat-overlay)


HF datasets
- https://huggingface.co/datasets/kontext-community/relighting
- https://huggingface.co/datasets/peteromallet/InScene-Dataset
- https://huggingface.co/datasets/obvious-research/flux-kontext-ipa-dataset
- https://huggingface.co/datasets/showlab/OmniConsistency


## Preparing a dataset for Flux Kontext training

- **Pair your images**: For each edit, keep a matching "before" image and "after" image.
- **Use a consistent name pattern**:
  - Start image: `INDEX_start.EXT`
  - End image: `INDEX_end.EXT`
  - Where `INDEX` is a shared two-digit ID (e.g., `01`, `02`, …) and `EXT` is one of: `jpg`, `jpeg`, `png`.
- **Optional prompt file**: Add `INDEX.txt` with a short instruction describing the edit for that pair.
- **Keep files together**: Place each pair (and optional prompt) in the same folder.
- **Tip**: Zero‑pad `INDEX` to two digits (e.g., `01`) to keep files naturally sorted.

Example layout:

```text
my-dataset/
  01_start.jpg
  01_end.jpg
  01.txt
  02_start.png
  02_end.png
```

See sample datasets in `./bigger-head` and `./hat-overlay` for reference.