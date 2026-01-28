# vidinfo

Quickly display essential video file properties (codec, resolution, aspect ratio, framerate, bitrate) in a human-friendly format.

## Overview

This script prints out key technical details about a video file in a single, readable line. It's useful for quickly checking video specs without opening a media player or running verbose commands.

- **Supported formats:** Any format supported by `ffprobe` (MP4, MKV, AVI, MOV, etc.)

## Requirements

- [ffprobe](https://ffmpeg.org/ffprobe.html) (part of the ffmpeg suite)

## Advantages

- **Concise:** Outputs only the most relevant info (codec, resolution, aspect ratio, fps, bitrate).
- **Fast:** No need to open heavy tools or GUIs.
- **Flexible:** Works with any video file supported by ffprobe.

## Installation

See `Installation` in Repo's [README](./../../README.md).

## Usage

```sh
vidinfo <video_file>
```

- `<video_file>`: Path to your video file.

## Output Example

```
h264, 1920×1080, 16:9, 25 fps, 450 kbps
```

## Notes

- If no file is provided, the script prints usage instructions.
- Requires `ffprobe` to be installed and available in your PATH.

## License

MIT
