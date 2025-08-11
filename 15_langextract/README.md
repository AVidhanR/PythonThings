# langextract

langextract is a lightweight toolkit for detecting, segmenting, and extracting human language content from mixed or noisy textual sources. It focuses on turning heterogeneous inputs (logs, scraped pages, transcripts, blended multilingual blocks) into clean, analyzable language segments with associated metadata that downstream pipelines can consume.

## Key Features

- Robust language identification across short, fragmented, or code‑mixed text.
- Multi-language segmentation that preserves original ordering and offsets.
- Noise filtering (removal or flagging of markup, boilerplate, templates, and artifacts).
- Adaptive token normalization while retaining reversible mappings to the raw text.
- Pluggable scoring and confidence measures for each detected segment.
- Lightweight abstraction for adding custom heuristics or model backends.
- Structured metadata output (language, confidence, span indices, quality flags).
- Batch and streaming oriented internal design for scalability.
- Extensible pipeline stages for enrichment (e.g., script detection, directionality).
- Designed to interoperate cleanly with downstream NLP tasks (translation, clustering, search).

## Common Use Cases

- Preprocessing multilingual corpora before indexing or embedding.
- Cleaning and segmenting scraped web pages or forum dumps.
- Identifying and isolating minority-language snippets within dominant-language documents.
- Preparing mixed-language customer support tickets for routing and analytics.
- Filtering out boilerplate or template fragments from content archives.
- Separating human-readable text from generated logs or telemetry noise.
- Enriching data lakes with language and script metadata for governance.
- Improving relevance in multilingual search or recommendation systems.
- Powering selective translation workflows (translating only specific language spans).
- Supporting compliance reviews by flagging unexpected language usage.

## Goals

langextract emphasizes accuracy on short spans, transparent confidence reporting, and ease of extension without imposing a heavy runtime footprint.

## Non-Goals

It is not a general-purpose NLP suite; it avoids embedding full parsing, semantic modeling, or translation, instead providing clean, language-aware text slices for specialized downstream tools.

## Summary

By focusing on precise multilingual segmentation and metadata fidelity, langextract streamlines the early stages of multilingual text processing pipelines, reducing noise and ambiguity before deeper analysis or model ingestion.

---

## Steps to get started into the `langextract` 

```sh
# zero
# cd into the 15_langextract/ directory!

# first
python -m venv .venv

# second
source .venv/bin/activate
# .venv/Scripts/activate - for windows

# third
pip install poetry

# fourth
poetry install

# to run the file
python main.py
```