# opus

Single File Media to Opus Converter.

This script converts a single media file to the OPUS audio format, preserving any video streams and converting audio to 32kbps Opus. It is useful for converting individual files with minimal interaction.

## Features

- Converts a single media file to `.opus` format
- Preserves video streams, converts audio to 32kbps Opus
- Prevents overwriting existing `.opus` files
- Simple usage with clear error messages

## Requirements

- [ffmpeg](https://ffmpeg.org/)

## Installation

See `Installation` in Repo's [README](./../../README.md).

## Usage

```bash
opus <input-media-file>
```

- `<input-media-file>`: Path to the media file you want to convert.

## Output

- Output location: current work directory.
- The converted file will have the same base name as the input, but with a `.opus` extension.
- The script will not overwrite existing `.opus` files.

## License

MIT
