# Bash Scripts

Custom commands (scripts) for POSIX-compliant shells (e.g., Bash, Zsh; not for fish).

## List of Scripts (alphabetical order)

- [opus](./scripts/opus/README.md) - Single File Media to Opus Converter.
- [opusall](./scripts/opusall/README.md) - All cwd Media Files to Opus Converter.
- [rname](./scripts/rname/README.md) - Rename file trees: replace spaces with a separator and convert filenames to lowercase.
- [videocut](./scripts/videocut/README.md) - Cut off unwanted segments from a video file based on timecodes (no re-encoding).
- [videoplus](./scripts/videoplus/README.md) - Concatenate multiple video files into a single output file (no re-encoding).

## Installation

1. Clone the desired script to your machine.

2. Grant execution permissions to the script:

   ```bash
   sudo chmod +x path/to/script
   ```

3. Add the folder containing the script to your `$PATH` variable if you want to use the script as a regular shell command. Note: if you plan to call the script directly (e.g., `~/path/to/script`), this step is not required.

### Adding the Directory with Script to the `$PATH` Variable Permanently

- For Bash users, edit the `~/.bashrc` file.
- For Zsh users, edit the `~/.zshrc` file.

Locate a line similar to this:

```bash
export PATH=$HOME/bin:$HOME/.local/bin:/usr/local/bin:$PATH
```

Add a separate line for each script's dir (or one if you put several scripts together) under it:

```bash
export PATH=/path/to/directory/with/script[s]:$PATH
```
