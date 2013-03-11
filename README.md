git recent-branches
===================

This will add a new command to git called `recent-branches`.

It will list the last 10 branches you looked at and allow you to switch to them by number.

Installation
------------
1. Clone the repository
2. Make a symlink to `git-recent-branches` somewhere in your $PATH (i.e. `/usr/bin/git-recent-branches`)
3. Type `git recent-branches` inside a git working directory

Requirements
------------
1. Ruby 1.9+
2. Grep
3. Awk

NOTE: I've only tested this on Linux - it almost certainly won't work on Windows, but might work on OSX

Usage
-----
- `git recent-branches` will show you the list and allow to type in a branch number to check it out
- `git recent-branches X` will switch to branch X in your history

Configuration
-------------
It uses git config for configuration and currently has only two options:
- `recent.limit X` will limit the number of branches shown in the recent list to X
- `recent.showcurrent 1` will include the currently checked out branch in the list. Defaults to 0

Optional
--------
I tend to add the following aliases to my git configuration to make this command easier to use:
```
[alias]
  rb = recent-branches
  lb = recent-branches 0
```
