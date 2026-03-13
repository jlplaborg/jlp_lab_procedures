# Usage

`$> head $source [-n <$number> | -c <$number>]`

---
# Description

Display the first portion of a file to the terminal screen. This command is the opposite of [[tail]]

---

# Important Options

## $source

The source text to display. This can be a text stream or a file

## -n <$number>

Display the first `$number` of lines in a file. If not included, a default value of `-n 10` is used

## -c <$number>

Display the first `$number` of bytes of a file