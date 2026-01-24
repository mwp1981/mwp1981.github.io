ZingTo Image Scoring - User Guide

📥 Download

Get the official app by searching for Zingto on the Microsoft Store.

## Related Keywords
AI Image Scoring, AI Image Rating, Standalone Desktop Image Scoring Application, Desktop AI Image Rating Software, Batch Image Analysis with AI, AI Photo Culling Tool for Desktop, Offline AI Image Rating

📋 Overview

A standalone desktop application for image scoring, frame capture, and photo-to-video creation. Key features:

- 100% local data processing: All images, data, and operations stay on your device—no cloud sync, no privacy leaks.

- Offline-first design: Complete functionality without an internet connection.

- Lightweight & optimized: Smooth performance even on low-end computers with minimal resource usage.

🎯 Image Quality Module

Powered by an AI model trained on a vast image dataset, delivering fast and accurate quality assessments with over 90% precision.

Performance

On a legacy system (Intel Core i5, 8GB RAM, no dedicated GPU), it processes up to 150 images per minute.

Core Capabilities

- Professional 0-10 scoring system for objective image quality evaluation.

- Auto-categorization into 4 quality levels: Excellent, Good, Fair, Poor.

- Flexible result export:

- Default: Excel format (with thumbnails).

- CSV format (without thumbnails): Modify the configuration file as follows:
        

  1. Open _internal/baseParamCfg.ini.

  2. Find export_score_with_thumbnail and set its value to 0.

🖼️ Image List & Right-Click Menu

- Default display limit: Up to 500 scored images in the list (configurable).

- Right-click anywhere in the image list to open a context menu with the following options:

- Sort by Name: Orders items alphabetically (A-Z) by filename.

- Sort by Score (Ascending): Arranges from lowest to highest score.

- Sort by Score (Descending): Arranges from highest to lowest score.

- Save Selected As: Saves copies of checked images to a custom local location.

🎥 Frame Capture Module

Extract multiple frames from video files for scoring or archiving, with dual processing engines for flexibility.

Video Source Support

- Supported formats: MP4, AVI, MOV, MKV, FLV, WEBM.

- 100% offline processing—no internet required.

Dual Processing Engines

- FFmpeg Mode: Recommended for videos with complex encoding, B-frames, or high profiles (requires separate FFmpeg installation).

- OpenCV Mode: Built-in solution—no additional software needed.

Flexible Capture Options

- Standard Mode: Capture frames at customizable intervals (minimum 1 second).

- High-Frequency Mode: Extract frames every 0.05 seconds for detailed analysis.

- Precise time-range selection (start/end controls).

- Customizable output naming (batch prefixes) and adjustable image quality/dimensions.

Image Management & Preview

- Thumbnail view with checkboxes for batch operations.

- Real-time preview with detailed image metadata.

- Right-click context menu for quick file operations.

- Configurable list limit (default: 500 images).

🎵 MelodyFrame - Photo to Video Module

Transform photo collections into professional music videos with auto-transitions, background music, and lyric synchronization.

Smart Photo Management

- Import via folder selection or individual file picker.

- Thumbnail grid view with multi-select support: reorder (up/down/top/bottom), sort (random/name).

Professional Video Templates

- Cinematic: Gradual camera movements + smooth cross-fades.

- Emotional: Soft fades and dissolves for storytelling.

- Dynamic: Energetic zooms and transitions for upbeat content.

- Minimal: Clean effects with subtle animations.

Quality Options

- Adjustable image display duration (3-15 seconds).

- Customizable transition times (1-5 seconds).

- Image scaling (30%-150% of original size).

- 24 FPS output for smooth playback.

Audio Integration

- Support for MP3, WAV, AAC, M4A, FLAC formats + audio duration display.

- Auto-detection of matching LRC lyric files (when audio and lyric files share the same name).

⚖️ Legal Notices & Third-Party Software

FFmpeg

This software uses FFmpeg-compatible functionality for extended video processing in the Frame Capture module. Note: ZingTo Image Scoring does NOT bundle or distribute FFmpeg.

About FFmpeg

FFmpeg is an open-source multimedia framework for handling video, audio, and other media files. It is licensed under the GNU Lesser General Public License (LGPL) and/or GNU General Public License (GPL).

User Responsibilities for FFmpeg Mode

1. Download ffmpeg.exe from the official source: https://ffmpeg.org/.

2. Configure the software to point to your local ffmpeg.exe file.

3. Comply with all applicable FFmpeg license terms.

Disclaimer: We assume no liability for issues arising from your download, configuration, or use of FFmpeg. For FFmpeg license questions, contact the FFmpeg project directly.

