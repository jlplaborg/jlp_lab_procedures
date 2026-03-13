# Usage

`$> $source $destination [-r] [-i]`

---
# Description

**Copy**. Copies a file or directory from `$source` to `$destination`.

---

# Important Options

## $source

The file or directory to be moved to a new location

## $destination

The new name and location to move a file or directory to

## -r

**Recursive**. Copy all files that are children of the `$source`. In other words, this setting *must be used if copying a directory.*

## -i

Ask before move. If the `$destination` is already the name of an existing file, you will be warned that you are about to overwrite something