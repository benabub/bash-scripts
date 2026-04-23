# under2pipe

Quickly rename files in subdirectories by replacing underscores with vertical bars.

## Overview

This script iterates through first-level subdirectories and renames files matching the specified extension by replacing all underscores (`_`) with vertical bars (`|`). It is specifically designed to restore original UNIX-style filenames that were mangled during NTFS transfers.

- **Supported formats:** Any file extension provided as an argument.

## Requirements

- Standard Bash environment (Linux/macOS)

## Advantages

- **Concise:** Specifically targets the common underscore-to-pipe character restoration.
- **Fast:** Uses internal Bash string manipulation for renaming.
- **Flexible:** Process files in all first-level subdirectories in one go.

## Installation

See `Installation` in Repo's [README](./../../README.md).

## Usage

```sh
under2pipe <extension>
```

- `<extension>`: Filename suffix/pattern to match (e.g., mp4, mkv).

## Notes

- If no argument is provided, the script prints usage instructions.
- Only affects files within first-level subdirectories, not the current directory.

## License

MIT
