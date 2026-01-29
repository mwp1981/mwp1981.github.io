# ZingTo Image Scoring - AI Image Rating User Guide

## 📥 Download & Installation
Get the official ZingTo Image Scoring app by searching for "Zingto" on the Microsoft Store. This standalone desktop AI image scoring software requires no additional setup—launch and use immediately after installation.

<p style="text-align: center; margin: 1.5rem 0;">
  <img src="/assets/images/picscoredesc.png" alt="picscoredesc" width="700" style="height: auto; border: 1px solid #eee; border-radius: 6px;">
</p>
<p style="color: #6a737d; font-size: 0.9rem; text-align: center; margin-top: -1rem; margin-bottom: 1.5rem;">ui main window</p>

## 📋 Overview of ZingTo Image Scoring
ZingTo Image Scoring is a **local-first, standalone desktop application** for professional AI image scoring, video frame capture, and photo-to-video creation. As an offline AI image rating tool, it prioritizes privacy and performance with these core advantages:
- 100% local data processing: All images, data, and AI scoring operations stay on your device—no cloud sync, no privacy leaks.
- Offline-first design: Complete AI image rating functionality without an internet connection.
- Lightweight & optimized: Smooth batch image analysis performance even on low-end computers with minimal resource usage.

## 🎯 AI Image Quality Scoring Module
Powered by a specialized AI model trained on a vast image dataset, ZingTo Image Scoring delivers fast and accurate AI image quality assessments with over 90% precision—ideal for batch image analysis of large photography collections.

### Performance
On a legacy system (Intel Core i5, 8GB RAM, no dedicated GPU), the software processes up to 150 images per minute for AI scoring and rating.

### Core AI Scoring Capabilities
- Professional 0-10 scoring system for objective image quality evaluation (AI Image Rating).
- Auto-categorization into 4 quality levels: Excellent, Good, Fair, Poor.
- Flexible result export for batch image analysis:
  - Default: Excel format (with thumbnails).
  - CSV format (without thumbnails): Modify the configuration file as follows:
    1. Open `_internal/baseParamCfg.ini`.
    2. Find `export_score_with_thumbnail` and set its value to 0.

## 🖼️ Image List & Right-Click Menu (Batch Operation Support)
The AI image scoring tool features a user-friendly image list for efficient batch image analysis, with these customizable options:
- Default display limit: Up to 500 scored images in the list (configurable for larger batch processing).
- Right-click anywhere in the image list to open a context menu with the following options:
  - Sort by Name: Orders items alphabetically (A-Z) by filename.
  - Sort by Score (Ascending): Arranges from lowest to highest AI image score.
  - Sort by Score (Descending): Arranges from highest to lowest AI image score.
  - Save Selected As: Saves copies of checked images to a custom local location.

## 🎥 Frame Capture Module (For Video-to-Image Analysis)
Extract multiple frames from video files for AI image scoring or archiving, with dual processing engines for flexibility—100% offline, no internet required.

### Video Source Support
Supported formats: MP4, AVI, MOV, MKV, FLV, WEBM.

### Dual Processing Engines
- FFmpeg Mode: Recommended for videos with complex encoding, B-frames, or high profiles (requires separate FFmpeg installation).
- OpenCV Mode: Built-in solution—no additional software needed for basic frame capture.

### Flexible Capture Options
- Standard Mode: Capture frames at customizable intervals (minimum 1 second) for subsequent AI image scoring.
- High-Frequency Mode: Extract frames every 0.05 seconds for detailed analysis.
- Precise time-range selection (start/end controls).
- Customizable output naming (batch prefixes) and adjustable image quality/dimensions.

### Image Management & Preview
- Thumbnail view with checkboxes for batch AI scoring operations.
- Real-time preview with detailed image metadata.
- Right-click context menu for quick file operations.
- Configurable list limit (default: 500 images).

## 🎵 MelodyFrame - Photo to Video Module
Transform photo collections into professional music videos with auto-transitions, background music, and lyric synchronization—an exclusive feature of ZingTo Image Scoring beyond core AI image rating.

### Smart Photo Management
- Import via folder selection or individual file picker (supports batch selection for video creation).
- Thumbnail grid view with multi-select support: reorder (up/down/top/bottom), sort (random/name).

### Professional Video Templates
- Cinematic: Gradual camera movements + smooth cross-fades.
- Emotional: Soft fades and dissolves for storytelling.
- Dynamic: Energetic zooms and transitions for upbeat content.
- Minimal: Clean effects with subtle animations.

### Quality Options
- Adjustable image display duration (3-15 seconds).
- Customizable transition times (1-5 seconds).
- Image scaling (30%-150% of original size).
- 24 FPS output for smooth playback.

### Audio Integration
- Support for MP3, WAV, AAC, M4A, FLAC formats + audio duration display.
- Auto-detection of matching LRC lyric files (when audio and lyric files share the same name).

## ⚖️ Legal Notices & Third-Party Software
### FFmpeg
This software uses FFmpeg-compatible functionality for extended video processing in the Frame Capture module. Note: ZingTo Image Scoring does NOT bundle or distribute FFmpeg.

#### About FFmpeg
FFmpeg is an open-source multimedia framework for handling video, audio, and other media files. It is licensed under the GNU Lesser General Public License (LGPL) and/or GNU General Public License (GPL).

#### User Responsibilities for FFmpeg Mode
1. Download `ffmpeg.exe` from the official source: [https://ffmpeg.org/](https://ffmpeg.org/).
2. Configure the software to point to your local `ffmpeg.exe` file.
3. Comply with all applicable FFmpeg license terms.

Disclaimer: We assume no liability for issues arising from your download, configuration, or use of FFmpeg. For FFmpeg license questions, contact the FFmpeg project directly.

