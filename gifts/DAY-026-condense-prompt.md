# The condense prompt

YT-Condense is a bookmarklet. Click it while a YouTube video plays, and a small worker sends the video's transcript to Claude with the prompt below. What comes back is plain prose at about a fifth of the length, ready to paste into a text-to-speech reader.

The bookmarklet and its worker are a private build. The prompt works on its own in any chat, with no code.

## The prompt

This is the prompt the worker sends, word for word. Fill in the three bracketed lines.

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

## Four steps

1. Open the video's transcript. On YouTube's desktop site, open the description and choose Show transcript. A video with no captions has no transcript, so the prompt cannot help with it.
2. Copy the transcript. If you already watched part of the video, copy from the point where you stopped and put that point, in seconds, on the FROM TIMESTAMP line.
3. Paste the prompt into Claude or ChatGPT and fill in the three bracketed lines.
4. Paste the answer into any text-to-speech reader and listen.

## Make it yours

- For a longer listen, change ~20% to ~40%.
- For notes to read instead of a listen, delete the first two rules and ask for a bulleted list.

## Limits

- The worker refuses a transcript over 100,000 characters, which its README puts at about an hour of video. A chat has its own limit too, so for a longer video split the transcript and run the prompt on each part.
- A model can drop or bend a fact while it shortens. Before you act on something you heard, check that part of the video.
