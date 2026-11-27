# Door 16: CorpusSync: search what you already know

- **Date:** October 28, 2026
- **Built:** June 20, 2026
- **Room:** 2
- **Code:** [LucasCooperBey/corpussync](https://github.com/LucasCooperBey/corpussync)

## What it is

You already have the answers somewhere in your notes, documents and your channel's captions. CorpusSync makes them searchable on your own machine, for free.

It cuts your files into overlapping windows and stores two vectors for each one in Qdrant: one from a local Ollama embed model that matches by meaning, and one that matches exact words, so names, codes and error strings still turn up.

- A relevance gate drops results that are not about your question, so you don't get the nearest neighbor of nothing.
- `corpussync ask` answers from a local chat model using only the numbered sources it found, and refuses without calling the model when nothing clears the gate.
- `./sync.sh` pulls YouTube captions with yt-dlp and no API key.
- Only yt-dlp's requests to YouTube leave your machine, unless you point Ollama or Qdrant at another one.

## Try it today

Clone [LucasCooperBey/corpussync](https://github.com/LucasCooperBey/corpussync), install it in a venv, and search a folder of your own notes:

```bash
pip install -e ".[pdf,docx]"
ollama pull nomic-embed-text
corpussync init
corpussync ingest ./notes --corpus notes
corpussync search "your question" --corpus notes
```

It needs Python 3.9 or newer and Ollama running locally.
