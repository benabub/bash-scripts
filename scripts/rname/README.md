# rname - Smart Directory Tree Renamer

![CLI Utility](https://img.shields.io/badge/CLI-Utility-green)
![Bash-Script](https://img.shields.io/badge/Script-Bash-blue)

This script provides a flexible way to rename files and directories in a directory tree, converting names to lowercase and replacing whitespaces with a separator (`_` or `-`). It offers various options to include/exclude specific directories and handle non-ASCII characters manually.

## Warning ⚠️

- The script is based on the `mv` command, which causes irreversible changes to the file system.
- **Never** apply this script on directories containing any kind of programs (OS files, installed software, games) - the programs will stop working!
- If you apply this script to OS system directories, you will almost certainly need to reinstall your operating system!
- Always double-check the paths you pass to the script.
- Before actual use, test the command behavior in dry-run mode (`--dryrun` | `-n`).
- The script is suitable only for processing file trees containing safe non-executable user files: text documents, PDFs, media files, etc.
- Best practice: run the script multiple times on separate deep directories rather than once on a large common root directory - this prevents accidental program damage.

## Features

- Converts filenames and directory names to lowercase
- Replaces spaces and special characters with configurable separators (`_` or `-`)
- Replaces character pairs `[:upper:][:lower:]` with `[:lower:]{separator}[:lower:]`
- Handles name conflicts by appending indices
- Supports dry-run mode to preview changes
- Provides options for:
  - Renaming entire directory trees
  - Including/excluding specific directories
  - Manual renaming of files/directories with non-ASCII characters

## Filename Renaming Examples  

*(using default separator)*  

| Original            | Renamed                 |  
|---------------------|-------------------------|  
| `Some file name`    | `some_file_name`        |  
| `DirName`           | `dir_name`              |  
| `-another example_` | `another_example`       |  


## Installation

See `Installation` in Repo's [README](./../../README.md).

## Usage

```bash
./rname [--dryrun | -n] [OPTION] [DIRS...]
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
   rname --dryrun
   ```

2. Rename entire directory tree (actual changes):
   ```bash
   rname
   ```

3. Rename only specific directories:
   ```bash
   rname --only dir1 dir2
   ```

4. Rename directory tree excluding specific directories:
   ```bash
   rname --exclude dir_to_skip another_dir
   ```

5. Rename with manual handling of non-ASCII filenames:
   ```bash
   rname --files
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

## License 📄

MIT
