# torrent_prep

Quickly collect files from subfolders and copy them to a flat destination directory using parent folder names.

## Overview

This script iterates through first-level subdirectories, finds files with a specific extension, and copies them to a target folder. During the process, it renames the files using their parent directory's name, which is ideal for organizing content for torrent distribution.

- **Supported formats:** Any file extension provided as an argument.

## Requirements

- Standard Bash environment (Linux/macOS)

## Advantages

- **Concise:** Flattens directory structures by moving files to a single location.
- **Fast:** Efficiently handles batch copying and renaming in one pass.
- **Flexible:** Works with any file extension and target directory.

## Installation

See `Installation` in Repo's [README](./../../README.md).

## Usage

```sh
torrent_prep <extension> <output_dir>
```

- `<extension>`: Filename suffix/pattern to match (e.g., mp4, mkv).
- `<output_dir>`: Path to the destination directory.

## Notes

- If exactly two arguments are not provided, the script prints usage instructions.
- The output directory must exist before running the script.

## License

MIT
