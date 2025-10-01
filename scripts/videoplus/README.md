# videoplus

Concatenate multiple video files into a single output file (no re-encoding).

## Overview

This script concatenates multiple video files into a single output file **without re-encoding** (lossless). It supports the following formats: MP4, MOV, MKV, AVI, WMV, FLV, and WebM.

## Requirements

- [ffmpeg](https://ffmpeg.org/)

## Installation

See `Installation` in Repo's [README](./../../README.md).

## Usage

```sh
videoplus video1.mp4 video2.mp4 [video3.mp4 ...]
```

- You must provide at least **two** video files as arguments.
- The output file will have the same extension as the first input file.

## How it works

1. Checks for at least two input files and verifies `ffmpeg` is installed.
2. Determines the output file name, avoiding overwriting existing files.
3. Creates a temporary file listing all input videos.
4. Uses `ffmpeg` with the `-f concat` and `-c copy` options to merge the videos losslessly.
5. Cleans up temporary files on exit.

## Output

- Output filename: `video_output.[ext]` (or `video_output_[index].[ext]` if the file exists).
- Output location: current work directory.
- The script does not remove original files.

## Notes

- All input videos should have the same codec and format for best results.
- Temporary files are cleaned up automatically.

## License

MIT
