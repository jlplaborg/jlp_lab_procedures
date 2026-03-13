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

`vim` itself is actually a full software, and not just a raw "command", *per se*. While using `vim`, there are therefore a full set of commands and special operations that are good to know. Below is a non-comprehensive list of some important details.

When first opening a file, you are in `mode select` mode. This means you cannot yet edit a file, and must instead select your mode of operation. You can enter a mode by pressing one of the following keys, and at any point you can exit a mode by pressing the `esc` key:

### `i`

**Insert mode**. Allow for normal text editing

### `v`

**Visual mode**. Allow for text scanning and selection. A marker will be set at the current point and follow the movement of your cursor. To learn more about this mode (as it is highly useful), Google and ChatGPT are your friends

### `:`

**Command mode**. Enter a state where you can enter and run special commands. There are thousands of combinations of commands. The commands here can be ran together and are not usually exclusive to each other. In other words, if you want to use `w`, `q`, and `!` all together, you can use the command `:wq!` as one input, rather than doing all three separately.

#### `:w`

**Write**. Save a file

#### `:q`

**Quit**. Exit `vim`. You will get a warning if you have unsaved changes

#### `[command]!`

**Override**. Ignore warnings and execute previous commands





