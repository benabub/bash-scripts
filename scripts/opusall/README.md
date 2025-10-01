# opusall

All cwd Media Files to Opus Converter.

This script batch-converts all media files in the current directory to the OPUS audio format, preserving video streams and converting audio to 32kbps Opus.

## Features

- Converts all media files in the current directory (except `.opus` files and script itself if you prefer direct use)
- Preserves video streams, converts audio to 32kbps Opus
- Skips files that are already converted or have existing `.opus` outputs
- Provides a summary of converted, skipped, and failed files

## Requirements

- [ffmpeg](https://ffmpeg.org/)

## Installation

See `Installation` in Repo's [README](./../../README.md).

## Usage

```bash
cd [path/to/media/files]
opusall
```

## Output

- Output location: current work directory.
- Converted files will have the same base name as the original, but with a `.opus` extension.
- The script will skip files that are already in `.opus` format or if the output file already exists.
- The script does not remove original files. 

## Notes

- The script only processes files in the current directory (not subdirectories).
- If interrupted (Ctrl+C), the script will stop ongoing conversions and exit cleanly.

## License

MIT
