# Changelog

**English** · [Español](CHANGELOG.es.md)

All notable changes to StreamFetch are documented here.
Format based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/)
and versions follow [Semantic Versioning](https://semver.org/).

## [1.0.0] · 2026-11-04

First release. Built on top of [VideoFetch](https://github.com/juangalisteo/videofetch) v1.2.0.

### Added
- Downloads streamed videos (`.m3u8` HLS, `.mpd` DASH, direct `.mp4`) from any website.
- **02 · Origin page** (*Referer*): filled in automatically from the link (e.g. `tella.tv`)
  or typed by hand; it is remembered.
- **Expired link** warning: reads the date inside signed links (CloudFront `Policy` / `Expires`).
- **"How do I get the link?"** button with the steps (F12 → Network → `m3u8` → Copy URL).
- Clear messages for DRM, access denied (403), not found (404) and invalid links.
- If the video is called "manifest", "master"…, the file is named `StreamFetch <date>`.
- Parallel fragment downloads and retries for long videos.
- Same as VideoFetch: MP4 H.264 + AAC ready for editors, MP3, 720p / 1080p / Best,
  **SRT** button (stream subtitles or AI-made with Whisper), ES / EN and console mode
  (`--referer`, `--name`, `--srt`, `--lang en`).
- App colour: **green** (`#22C55E`).
