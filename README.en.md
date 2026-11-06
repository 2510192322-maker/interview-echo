# Interview Echo · 面试回声

Replay the interview. Improve the next answer.

A Chinese-first interview review skill for recordings, audio files, and transcripts. It separates the interviewer's questions, the candidate's actual answers, and AI feedback, with blank spaces for a teacher or coach. A Tongyi Tingwu analysis link with playback and ASR text appears first; an evidence-based summary of strengths and improvements appears last.

[中文说明](README.md) · [Skill instructions](SKILL.md) · [Fictional example](examples/sample-review.md)

## What it produces

For each question:

1. The question, follow-ups, and a source-backed timestamp when available.
2. The candidate's actual answer, without silently rewriting mistakes.
3. Specific feedback, practical changes, and a clearly labeled suggested answer.
4. A blank teacher feedback area.

Each question uses the headings “My answer”, “AI answer (model-answer perspective)”, and a blank teacher feedback area. The final summary separates strengths from opportunities to improve. Missing audio, uncertain terms, incomplete recordings, and unclear speakers are explicitly marked. Suggested answers must not invent personal experience or achievements.

## Install

Place this repository in the Codex skills directory as `interview-echo`:

```bash
git clone https://github.com/2510192322-maker/interview-echo.git "${CODEX_HOME:-$HOME/.codex}/skills/interview-echo"
```

Inspect an existing destination before replacing it. Other assistants that support `SKILL.md` can use their own skill import workflow.

## Use

Attach an interview recording or transcript and ask:

```text
Use $interview-echo to review this interview.
Put the corresponding Tongyi Tingwu analysis link first. For each question,
include my actual answer, a model answer, and a blank teacher feedback area.
End with a summary of strengths and improvements.
```

The skill defaults to Chinese. Ask for another output language when needed.

## Requirements

This repository contains instructions, not a bundled speech recognition engine. Audio understanding or a transcription tool must be available in the host. Video-to-audio extraction also requires a suitable media tool, such as FFmpeg. A transcript alone is sufficient for a text review.

Markdown is the default output. Additional document formats depend on the host's tools. The opening link must lead to the matching Tongyi Tingwu analysis page with the recording and ASR transcript, not a raw file or an attachment. An audio-only source may use an analysis page with audio playback. Timestamps must match the selected version. If the analysis link is missing, produce a clearly labeled draft and request the missing link. Creating new analysis records requires user authorization; do not purchase transcription or expand sharing permissions without authorization. Reference screenshots define formatting only, not candidate facts.

No real interview recordings, transcripts, personal reviews, or account data are included. The example is entirely fictional.

## License

[MIT](LICENSE)
