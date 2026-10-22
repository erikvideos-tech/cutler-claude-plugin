# Cutler for Claude Code: edit video with Claude

**Cutler turns Claude into a video editor.** This repository is the Claude Code plugin that connects Claude Code to [Cutler](https://cutler.miracontents.com), a Mac app that gives Claude eyes, hands and a timeline: it analyses your footage, syncs your cameras and mics by sound, cuts with a reason for every clip, renders previews, and exports a verified Final Cut Pro project on your original media.

> The plugin is a small launcher. The editing engine ships inside **Cutler.app**, which you need on the same Mac (macOS 14 or later, Apple Silicon). Cutler is a one-time purchase: see [pricing](https://cutler.miracontents.com/pricing).

![Cutler's cut page: the conversation, the preview, the plan and every row with its reason](https://cutler.miracontents.com/assets/og-cut-page.jpg)

## What Claude can do with Cutler

- **See the footage.** Transcription runs on your Mac. Every clip gets a description and quality flags (soft focus, blinks, motion blur, dark takes). Claude can look at contact sheets and storyboards.
- **Sync cameras and separate audio.** Sources line up by waveform, with no timecode needed. Multicam opens as native multicam in Final Cut Pro.
- **Cut with reasons.** Claude writes a cut table checked against the media: every row has its source, timecodes and why it is there.
- **Finish.** Music, logos, stills and show graphics by name; dialogue levelling, loudness targets and music ducking under dialogue at export.
- **Check its work.** A rendered preview plays on your Mac before anything is handed over.
- **Deliver.** A Final Cut Pro project (FCPXML validated against Apple's DTD) with roles and keywords, every clip pointing at your original media. Nothing re-encoded, nothing generated.

## Tools

| Tool | What it does |
|---|---|
| `cutler_read` | Free, read-only: the project, the footage digest, a clip's timed phrases and picture notes, a saved cut, jobs, the brief, a free cost estimate, the attached show. |
| `cutler_look` | Pictures made on your Mac: a storyboard of a cut (one frame per row) or contact sheets for describing footage. |
| `cutler_edit` | Brief, cut check and save, vision plan and descriptions, add media, free analysis (transcribe on the Mac, vision in the chat), show profiles, and status/questions to the editor. |
| `cutler_deliver` | Render and play a preview, or export the cut to Final Cut Pro with levelling, loudness and ducking options. |
| `cutler_spend` | Paid analysis with the vision model you chose in Cutler, only under a budget the editor names. |
| `cutler_panel` | Shows Cutler's live panel in the chat: progress and a player for rendered previews. |

## Install

1. Install [Cutler](https://cutler.miracontents.com) on your Mac. If you choose Claude Code in Cutler's setup, Cutler connects itself and you can skip the next step.
2. To add the plugin by hand, run these two lines in your terminal:

```bash
claude plugin marketplace add erikvideos-tech/cutler-claude-plugin
claude plugin install cutler@mira-contents
```

Or, inside a Claude Code session:

```text
/plugin marketplace add erikvideos-tech/cutler-claude-plugin
/plugin install cutler@mira-contents
```

If Cutler.app is not in `/Applications`, set `CUTLER_APP` to its location.

## How a session goes

1. Point Claude at a folder from a real job: raw camera cards, separate audio, unsynced multicam.
2. Tell it what the video is for. The conversation is the brief.
3. Read the proposal: a reason on every row. Ask for changes in plain language.
4. Open the result in Final Cut Pro, or ask for a rendered preview.

## Privacy

Transcription always runs on your Mac. When Claude looks at shots, it sees still frames through your own Claude account. Your video files stay where they are; Cutler never copies them into a project. Details: [privacy](https://cutler.miracontents.com/privacy).

## Also works with

The Claude app (no terminal; Cutler's panel shows the work) and ChatGPT (beta, inside Cutler's window with your own ChatGPT account). Premiere Pro and DaVinci Resolve XML export are in beta.

## Links

- Website: https://cutler.miracontents.com
- Edit video with Claude Code: https://cutler.miracontents.com/claude-code-video-editing
- Questions: https://cutler.miracontents.com/faq
- Support: support@miracontents.com

Made by [Erik Lindgren](https://erikcuts.com), an editor with more than twenty years of documentary, corporate and television work. Mira Contents, Cascais, Portugal.

The files in this repository are MIT licensed. Cutler.app is proprietary; see its [terms](https://cutler.miracontents.com/terms).
