# Vim Text Editor - Brief Guide

Vim is a Linux text editor, often used for editing code and configuration files. 

## Table of Contents

1. [How to Get Started](#how-to-get-started)
3. [Modes](#modes)
4. [Basic commands](#basic-commands)

## How to Get Started

To open a file using Vim, type `vim` or `vi` (older version of vim) followed by the name of the file you wanted to edit, for example:

```bash
vim filename.txt
```

If the file doesn't exist, it will be created when saved.

#

## Modes

Vim operates in the following modes:

- **Normal mode (default)**     
This is the mode you're in when you first open Vim. You can navigate and perform actions like copy, paste, and delete text. You can also return to this mode from another one by pressing `esc`.

- **Insert Mode**   
It allows you to edit text. You can enter it by pressing `i` in Normal mode.

- **Visual Mode**   
For selecting text. You can enter it by pressing `v` in Normal mode.

- **Command Mode**  
For running commands, e.g. save, search, exit. You can enter it by pressing `:` in Normal mode.

#

## Basic commands


Deletion:
- press `d` to delete a single letter 
- press `dw` to delete a word
- press `dd` to delete an entire line 

Undo: press `u`

Redo: press `ctrl + r`

Copy text: press `yw` to copy a word

Paste: use `p` to paste the copied text

#

Move cursor:
-  up: `k`

- down: `j`

- right: `l`

- left: `h`

- line beginning: `0`

- line end: `$`

- beginning of the file: `gg`

- eng of the file: `G` 

#


Save changes and exit: `:wq` or `:x`

Quit without saving: `:q!`

Save changes: `:w`

