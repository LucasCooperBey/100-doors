# Door 16: CorpusSync: search what you already know

- **Date:** October 28, 2026
- **Built:** June 20, 2026
- **Room:** 2
- **Code:** [LucasCooperBey/corpussync](https://github.com/LucasCooperBey/corpussync)

## What it is

Plain nearest-neighbor search always returns a match, even when nothing in your notes is about the question.

CorpusSync ingests local Markdown notes, documents, and YouTube captions into a local Qdrant store, searches by both meaning and exact word behind a relevance gate (0.65 cosine floor or full lexical match), and answers from a local Ollama model with numbered sources. When nothing clears the gate, `ask` refuses instead of guessing.

## Try it today

Clone [LucasCooperBey/corpussync](https://github.com/LucasCooperBey/corpussync), install in a virtual environment, pull `nomic-embed-text` in Ollama, and ingest a folder of notes:

```bash
pip install -e .
ollama pull nomic-embed-text
corpussync ingest ./notes --corpus notes
corpussync search "your question"
```
