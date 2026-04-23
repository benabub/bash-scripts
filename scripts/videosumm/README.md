# videosumm

Calculates the total duration of all MP4 videos located in nested directories.

## Overview

This script scans all subfolders (excluding the current working directory) for `.mp4` files, sums up their durations, and prints the total time in a clean `Xh YYm` format. It is designed for a quick overview of content volume in structured projects.

- **Recursive search:** Only targets files in subdirectories (`-mindepth 2`).
- **Clean output:** Provides total time without seconds or unnecessary noise.

## Requirements

- [ffprobe](https://ffmpeg.org/ffprobe.html) (part of the ffmpeg suite)

## Advantages

- **Specific scope:** Automatically ignores top-level files to focus on nested content.
- **Accurate:** Uses `ffprobe` to get precise stream duration instead of metadata guesses.
- **Readable:** Formats the resulting sum into hours and minutes.

## Installation

See `Installation` in Repo's [README](./../../README.md).

## Usage

```sh
videosumm
```

*Run the script inside the directory containing the folders you want to analyze.*

## Output Example
```bash
1h 37m
```

## Notes

- The script specifically looks for `.mp4` extensions.
- Requires `ffprobe` to be installed and available in your PATH.

## License

MIT
