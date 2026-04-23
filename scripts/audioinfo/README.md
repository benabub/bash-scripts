# audioinfo

Quickly display essential audio stream properties (codec, bitrate, channels) in a human-friendly format.

## Overview

This script prints out key technical details about an audio stream in a single, readable line. It's useful for quickly checking audio specs without opening a media player or running verbose commands.

- **Supported formats:** Any format supported by `mediainfo` (MP4, MKV, MP3, FLAC, etc.)

## Requirements

- [mediainfo](https://mediaarea.net)

## Advantages

- **Concise:** Outputs only the most relevant info (codec, bitrate, channels).
- **Fast:** No need to open heavy tools or GUIs.
- **Flexible:** Works with any media file supported by mediainfo.

## Installation

See `Installation` in Repo's [README](./../../README.md).

## Usage

```sh
audioinfo <video_file>
```

- `<video_file>`: Path to your media file.

## Output Example

```
aac, 128kbps, 2ch
```

## Notes

- If no file is provided, the script prints usage instructions.
- Requires `mediainfo` to be installed and available in your PATH.

## License

MIT

