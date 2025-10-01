# videocut

Cuting off unwanted segments from a video file based on timecodes (no re-encoding).

## Overview

This script removes unwanted segments from a video file based on timecodes you provide. It performs **lossless cutting** (no re-encoding), preserving the original quality and working much faster than traditional video editors.

- **Supported formats:** MP4, MOV, MKV, AVI, WMV, FLV, WebM

## Requirements

- [ffmpeg](https://ffmpeg.org/)

## Advantages

- **Lossless:** No re-encoding, so no quality loss.
- **Fast:** Processing time depends on number of cuts, not video length.

## Limitations

- **Visual artifacts:** Cuts may not be frame-accurate; you may see brief glitches at segment boundaries due to keyframe limitations. No such problem with sound.
- **Performance:** Many segments may slow down processing.

## Installation

See `Installation` in Repo's [README](./../../README.md).

## Usage

```sh
videocut input_video_file timecodes [output_basename]
```

- `input_video`: Your source video.
- `timecodes`: Plaintext file with timecode pairs (see below).
- `output_basename`: (Optional) Base name for the output file (default: `video_output`).


## Timecodes File Format

- Each line: `START_TIME END_TIME` (space-separated)
- Accepted time formats: `HH:MM:SS`, `HH:MM:SS.00`, `HH:MM:SS:FF`
- Use `None`, `none`, `False`, or `false` to indicate "from start" or "to end"
- Example:

  ```
  None 00:01:30
  00:05:00 00:06:00
  00:10:00 None
  ```

  This will remove: from start to 1:30, from 5:00 to 6:00, and from 10:00 to end.

## How it works

1. Copies the input video to a new output file.
2. Reads timecodes from bottom to top, removing each segment in turn.
3. Uses `ffmpeg` with `-c copy` for lossless segment removal.
4. Cleans up temporary files automatically.

## Output

- Output Basename: Can be provided as the third argument.
- Default: If not provided, the output will be named `video_output[_index].mp4`
- Output location: current work directory.
- The script does not remove original file.

## Notes

- All input/output files are checked to avoid overwriting.
- Temporary files are cleaned up on exit.

## License

MIT
