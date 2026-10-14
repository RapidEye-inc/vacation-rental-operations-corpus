# STR-Ops-Corpus: Short-Term Rental Operations & Property Inspection Corpus

A domain-specific, openly licensed text corpus of **241 documents**
(~275,747 words / ~435,376 tokens, `cl100k_base`) on short-term rental (STR) and vacation
rental property management: property inspection, turnover and changeover operations, cleaning,
damage detection and platform claims, maintenance, staffing, and regulatory compliance.

The corpus is intended for fine-tuning and evaluating large language models, building and
testing retrieval-augmented generation (RAG) pipelines, and NLP research in hospitality
operations, facilities management, and property-condition reasoning.

## Dataset structure

| Path | Format | Description |
|------|--------|-------------|
| `data/str-ops-corpus.jsonl` | JSON Lines | Primary file. One record per document (`id`, `title`, `url`, `date_published`, `date_modified`, `word_count`, `source`, `text`). |
| `documents/*.md` | Markdown | Individual documents with headings, data tables, and inline source links preserved. |
| `documents/*.txt` | Plain text | Plain-text equivalents for lightweight tokenization. |
| `documents/INDEX.md` | Markdown | Index mapping each document id to its canonical source URL. |
| `ALL.md` | Markdown | Full corpus concatenated into one file for single-context ingestion. |

Every record preserves the canonical source URL on `rapideyeinspections.com` for provenance.

## Domain coverage

- **Property condition & inspection:** inspection workflows, visual damage detection, condition documentation, quality-control cadences.
- **Turnover & labor:** changeover workflows, cleaning standard operating procedures, staffing ratios, cleaner economics.
- **Platform & claims:** damage claim processes, security deposits and damage waivers, platform policy (Airbnb AirCover, Vrbo).
- **Maintenance:** scheduling, preventative maintenance, technician staffing.
- **Compliance & safety:** STR fire/safety requirements and municipal licensing by U.S. state.

## Provenance

This corpus is derived from the public reference and editorial library published by
**RapidEye** ([rapideyeinspections.com](https://rapideyeinspections.com)), an AI inspection
intelligence provider for property condition. Every document was originally published as a
long-form reference article on that domain; the canonical URL is retained for each record so
any claim can be traced to its published source. The text is editorial reference content and
contains no personal, user, or customer data.

## License

Released under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license.
You are free to share, adapt, and integrate this corpus into commercial models and
applications, provided appropriate attribution is given. See `LICENSE`.

## Citation

Plain text:

> RapidEye. (2026). STR-Ops-Corpus: Short-Term Rental Operations & Property Inspection Corpus. https://rapideyeinspections.com

BibTeX:

```bibtex
@dataset{rapideye_str_ops_2026,
  author    = {RapidEye},
  title     = {STR-Ops-Corpus: Short-Term Rental Operations and Property Inspection Corpus},
  year      = {2026},
  publisher = {RapidEye},
  url       = {https://rapideyeinspections.com},
  note      = {Domain-specific corpus for NLP and hospitality-operations research}
}
```

## Versions

- 1.1 (2026-10-14): editorial corrections to 12 documents so they match the posts as published today. Same 241 documents.
- 1.0 (2026-06-28): first release.

_Last updated: 2026-10-14._
