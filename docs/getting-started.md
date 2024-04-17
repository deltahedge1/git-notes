# Getting Started

## Example config file

global config are stored in a `.gitconfig` file in the `%HOMEPATH%` i.e. `%HOMEPATH%\.gitconfig`

```
# %HOMEPATH%/.gitconfig
...

[user]
	name = khammer1
	email = khammer1@google.com
[alias]
  co = checkout
  ci = commit
  st = status
  br = branch
  hist = log --pretty=format:'%h %ad | %s%d [%an]' --graph --date=short
  type = cat-file -t
  dump = cat-file -p
```

_Explaination of log_

- `--pretty="..."` defines the format of the output.
- `%h` is the abbreviated hash of the commit
- `%d` are any decorations on that commit (e.g. branch heads or tags)
- `%ad` is the author date
- `%s` is the comment
- `%an` is the author name
- `--graph` informs git to display the commit tree in an ASCII graph layout
- `--date=short` keeps the date format nice and short


### Setup email and password
```terminal
git config --global user.name "Your Name"
git config --global user.email "Your Email"
```

### Setup Line ending preference

Windows user:
```
git config --global core.autocrlf true
git config --global core.safecrlf true
```

Unix/Mac users:
```
git config --global core.autocrlf input
git config --global core.safecrlf true
```

## Git config commands

### List all the config values

```
git config [--global|--local] --list
```

### List values

```
git config [--global|--local] --get <key>
```

```
git config [--global|--local] <key> <value>
```

### Unset values

```
git config --global --unset <key>
```

### Set git alias

```
git config [--global|--local] alias.<alias-name> <git-command>
```

```
git config --global alias.st status
```