# YT-Condense: turn a long YouTube video into a shorter listen

The tool is public: **https://github.com/LucasCooperBey/yt-condense**

Give it a YouTube link and it gives back the video as plain spoken prose at about a fifth of the length, ready to read or to play through any text-to-speech reader. It works with or without captions. When a video has captions it uses them; when it has none, it downloads the audio and transcribes it on your own machine first.

## Run it

You need [uv](https://docs.astral.sh/uv/), a free Python runner.

```sh
curl -LsSf https://astral.sh/uv/install.sh | sh
git clone https://github.com/LucasCooperBey/yt-condense.git
cd yt-condense
uv run yt_condense.py "https://www.youtube.com/watch?v=VIDEO_ID" --provider none
```

The first run installs what it needs. With `--provider none` no model is called and you need no account: the tool writes `out/VIDEO_ID/paste-into-chat.txt`, which you paste into Claude, ChatGPT or any chat model. The reply is the shorter version.

To skip the paste, drop `--provider none`. If you use Claude Code, the tool runs `claude -p` on your own plan with no key; otherwise export an `ANTHROPIC_API_KEY` or run [Ollama](https://ollama.com) locally. The result lands in `out/VIDEO_ID/condensed.txt`. On a Mac, add `--speak` to also get an audio file.

Useful flags: `--from 12:30` starts where you stopped watching, `--length 40` gives a longer listen, `--transcribe` transcribes the audio even when captions exist, and `--whisper-model tiny` makes transcription faster on a slow machine.

## The prompt inside it

This is the prompt the tool sends, word for word. It also works on its own if you paste a transcript into any chat.

```text
Transform this YouTube transcript into a condensed audio summary.

RULES:
- Flowing conversational prose (NO bullets, NO lists, NO markdown)
- Short sentences suitable for text-to-speech
- Remove ALL filler: "um", "like", "you know", "basically", "so"
- Remove ALL meta-content: intros, outros, "subscribe", sponsors, "in this video"
- Remove ALL repetition: if a point was made, don't restate it
- Keep ONLY: novel insights, specific facts, actionable advice, concrete examples
- Target ~20% of original length
- Start IMMEDIATELY with content (no preamble)

VIDEO: [the video's title or link]
FROM TIMESTAMP: [where to start; 0 for the whole video] seconds

TRANSCRIPT:
[paste the transcript here]
```

## Limits

- A model can drop or bend a fact while it shortens. Before you act on something you heard, check that part of the video.
- Transcribing a video with no captions takes a few minutes on a laptop, and the first time it downloads the speech model (about 460 MB for the default, 75 MB for `tiny`).
- Private, removed, age-gated and region-locked videos cannot be read; the tool says which.
