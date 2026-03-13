# Usage

`$> rm $target [-r] [-i] [-f]`

---
# Description

**Remove**. Permanently and entirely delete a file or directory. This **does not** move a file to a recycle bin. It is permanent and total. In other words, to be abundantly clear and cautious, ***this is permanent***.

A warning will be prompted before deleting important or commonly used files.

---

# Important Options

## $target

The file or directory to delete

## -r

**Recursive**. Remove all child files of a `$source`. In other words, this option must be used if deleting a directory

## -i

Ask before each deletion

## -f

**Force**. Force the delete of a file by discarding and ignoring all warnings and cautions. **Be very careful when using this option as it can become possible to permanently delete important system files!**