# Usage

`$> vim $filename`

---
# Description

Enter the `vim` editor to modify a file. This is a very powerful text editor, but can be a little hard to use at first. This is a full *command line* interface, so note that **the mouse does not work in vim. All navigation must be done using arrow keys**

---

# Important Options

## $filename

The name of the file to modify. If the file does not exist, it is created

# Special Operations

`vim` itself is actually a full software, and not just a raw "command", *per se*. While using `vim`, there are therefore a full set of commands and special operations that are good to know. Below is a non-comprehensive list of some important details;

## Editing in `vim`

When first opening a file, you are in `mode select` mode. This means you cannot yet edit a file, and must instead select your mode of operation. You can enter a mode by pressing one of the following keys:

### `i`

**Insert mode**. Allow for normal text editing