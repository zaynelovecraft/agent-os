---
name: youtube-to-os
description: Analyze a YouTube video from URL, extract actionable frameworks, and update OS context, skills, or plans.
---

# YouTube -> OS

## Step 1 — Fetch transcript

1. `youtube-transcript-api` (Python): `YouTubeTranscriptApi().fetch(video_id)`
2. Fallback to `yt-dlp --write-auto-sub --skip-download`

## Step 2 — Analyze

Produce a high-signal breakdown:
- **Thesis** — main argument in 2-3 sentences
- **Frameworks** — named models or repeatable patterns
- **Actionable** — what to implement right now vs. skip
- **Gaps** — what our current setup is missing compared to the video

## Step 3 — Output artifacts

Offer to turn the takeaway into:
- A new skill in `.cursor/skills/<name>/SKILL.md`
- A research log in `research/logs/YYYY-MM-DD-slug.md`
- Concrete checkboxes in `todo.md`
