# bash-scripts
custom commands for UNIX-like shells

## List of scripts

- [hyprland-borders-nl](./docs/hyprland-borders-nl.md) - 
- [hyprland-borders-us](./docs/hyprland-borders-us.md) - 
- [rname](./docs/rname.md) - 
- [weather-day-after-tomorrow](./docs/weather-day-after-tomorrow.md) - 
- [weather-icon](./docs/weather-icon.md) - 
- [weather-now](./docs/weather-now.md) - 
- [weather-tomorrow](./docs/weather-tomorrow.md) - 

## How to make it work:

1. clone this repo on your machine

2. add the folder with scripts to $PATH variable permanently

3. give permissions to scripts

## Clone this repo on your machine

Open in shell the folder you want to put this repo in and do:

```bash
git clone https://github.com/benabub/bash-scripts.git
```

For example, my location is:

```bash
~/bin/bash-scripts
```

## Add the folder with scripts to $PATH variable permanently

If you use bash, you need to change `~/.bashrc`

If you use zsh, you need to change `~/.zshrc`

It's means to find this-like line: ..

```bash
export PATH=$HOME/bin:$HOME/.local/bin:/usr/local/bin:$PATH
```

.. and add to it your path to repo's `scripts` folder:

```bash
export PATH=${YOUR_PARENT_DIR}/bash-scripts/scripts:$HOME/bin:$HOME/.local/bin:/usr/local/bin:$PATH
```

For example, my line is:

```bash
export PATH=$HOME/bin/bash-scripts/scripts:$HOME/bin:$HOME/.local/bin:/usr/local/bin:$PATH
```

### Give permissions to scripts

```bash
chmod 755 {PATH_TO_REPOS_SCRIPTS_FOLDER}/*
```

For example, my command was:

```bash
chmod 755 ~/bin/bash-scripts/scripts/*
```
