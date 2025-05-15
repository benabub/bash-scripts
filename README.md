# Bash Scripts

Custom commands for UNIX-like shells.

## List of Scripts

- [rname](./scripts/rname/README.md) - Rename file trees: replace spaces with a separator and convert filenames to lowercase.

## Installation

1. Clone the desired script to your machine.

2. Grant execution permissions to the script:

   ```bash
   sudo chmod +x path/to/script
   ```

3. Add the folder containing the script to your `$PATH` variable if you want to use the script as a regular shell command. Note: if you plan to call the script directly (e.g., `exec ~/path/to/script`), this step is not required.

### Adding the Directory with Script to the `$PATH` Variable Permanently

- For Bash users, edit the `~/.bashrc` file.
- For Zsh users, edit the `~/.zshrc` file.

Locate a line similar to this:

```bash
export PATH=$HOME/bin:$HOME/.local/bin:/usr/local/bin:$PATH
```

Add your directory to the line:

```bash
export PATH=/your/directory:$HOME/bin:$HOME/.local/bin:/usr/local/bin:$PATH
```
