# Optimizing Inference Cost for Arabic–English Mathematical Reasoning in LLMs

Code for the paper *"Optimizing Inference Cost for Arabic–English Mathematical Reasoning in LLMs"* (ArabicNLP 2026, co-located with EMNLP 2026).

## Repository Structure

Each notebook corresponds to one dataset's final experimental results, as reported in the paper:

| Notebook | Result |
|---|---|
| `test2.ipynb` | K-sweep validation (Table 1, Figure 2) |
| `test33.ipynb` | Arabic GSM8K final results (Table 2) |
| `test34.ipynb` | English GSM8K final results (Table 3) |
| `test35.ipynb` | SVAMP final results (Table 4) |
| `test37.ipynb` | ArMATH final results (Table 5, Table 6) |

## Methods Implemented

Each notebook evaluates the following prompting methods in a black-box API setting (via the NVIDIA API, `openai/gpt-oss-20b`):

- Direct Answer
- Chain-of-Thought (CoT)
- FAA-lite (First Answer Anchoring)
- Confidence-Triggered Escalation (CTE)
- Self-Consistency (K=2)
- Verification (K=2)
- Arabic-specific variants (Format-Controlled CoT, Numeral-Normalized CoT, Bilingual-Glossary CoT) — Arabic datasets only

## Requirements

```
pip install openai pandas numpy tqdm matplotlib scipy datasets
```

An NVIDIA API key is required, set via the `NVIDIA_API_KEY` environment variable.

## Citation

If you use this code, please cite our paper (details to be updated upon publication in the ArabicNLP 2026 proceedings).
