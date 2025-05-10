# rname (Directory Tree Renaming Tool)

This script provides a flexible way to rename files and directories in a directory tree, converting names to lowercase and replacing whitespaces with a separator (`_` or `-`). It offers various options to include/exclude specific directories and handle non-ASCII characters manually.

## Features

- Converts filenames and directory names to lowercase
- Replaces spaces and special characters with configurable separators (`_` or `-`)
- Handles name conflicts by appending indices
- Supports dry-run mode to preview changes
- Provides options for:
  - Renaming entire directory trees
  - Including/excluding specific directories
  - Manual renaming of files/directories with non-ASCII characters
  - Selective processing of only files or only directories

## Usage

```bash
./rename_tree.sh [--dryrun | -n] [OPTION] [DIRS...]
```

### Options

| Option | Description |
|--------|-------------|
| `--dryrun`, `-n` | Perform a dry run without making actual changes (must be specified first) |
| (no option) | Rename the entire directory tree under the current working directory |
| `--only`, `-o` | Rename all directory trees in the selected folders, including their names |
| `--exclude`, `-e` | Rename the entire directory tree, excluding the selected folders and their contents |
| `--files`, `-f` | Rename the entire directory tree with manual renaming for non-ASCII filenames |
| `--onlyfiles`, `-of`, `-fo` | Rename selected folders with manual renaming for non-ASCII filenames |
| `--excludefiles`, `-ef`, `-fe` | Rename directory tree excluding selected folders, with manual renaming for non-ASCII filenames |
| `--dirs`, `-d` | Rename the entire directory tree with manual renaming for non-ASCII directory names |
| `--onlydirs`, `-od`, `-do` | Rename selected folders with manual renaming for non-ASCII directory names |
| `--excludedirs`, `-ed`, `-de` | Rename directory tree excluding selected folders, with manual renaming for non-ASCII directory names |
| `--both`, `-b` | Manually rename both files and directories with non-ASCII characters |
| `--onlyboth`, `-ob`, `-bo` | Rename selected folders with manual renaming for both files and directories with non-ASCII characters |
| `--excludeboth`, `-eb`, `-be` | Rename directory tree excluding selected folders, with manual renaming for both files and directories with non-ASCII characters |
| `--help`, `-h` | Show this help message |

## Examples

1. Preview renaming of entire directory tree:
   ```bash
   ./rename_tree.sh --dryrun
   ```

2. Rename entire directory tree (actual changes):
   ```bash
   ./rename_tree.sh
   ```

3. Rename only specific directories:
   ```bash
   ./rename_tree.sh --only dir1 dir2
   ```

4. Rename directory tree excluding specific directories:
   ```bash
   ./rename_tree.sh --exclude dir_to_skip another_dir
   ```

5. Rename with manual handling of non-ASCII filenames:
   ```bash
   ./rename_tree.sh --files
   ```

## Notes

- The script ignores hidden files/directories (starting with `.`) and backup files (starting with `~`)
- You'll be prompted to confirm before making changes
- You can choose between `_` and `-` as separators during execution
- For manual renaming modes, you'll be prompted for each problematic name

## Safety Features

- Dry-run mode to preview changes
- Graceful handling of name conflicts
- Progress indicators during processing
