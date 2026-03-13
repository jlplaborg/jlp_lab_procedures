Bash and command line commands are not always the most intuitive to follow, *especially* if you are not new to using them. Here is a quick guide for how to understand documentation as written here. Note that there are no real hard-and-fast standards for how commands are documented, so this is not a definitive source of truth. Instead, it will explain how commands are communicated in this notebook.

In written commands here, I will use `$>` to designate the start of a command. You do *not* include this portion when you type the command. It is instead there for stylistic purposes as that starter, or something quite similar to it, will commonly show in your command line terminal.

Also know that what we see here is ***not comprehensive for each command***. Often there are dozens of options and arguments allowed for a command. Searching for the `man page` for any given command will provide a full documentation if you would ever like to learn more about something.
# Usage
Every command will contain a `usage` block. This tells you how a command should be typed to run. The simplest of commands will contain only the invocation itself, as we:

`$> pwd`

The command above operates fully without the need to input any extra information or `arguments`. There are two ways to communicate how arguments are used.

In this section, you will see two types of argument types as well. These are `variable arguments`, denoted by using a `$` symbol affixed to the name, and a `literal variable`, denoted with no special marking. A `variable argument` is one that you must replace with something. For example, if we see `$directory`, this would mean that you need to replace the argument with a `directory`, or other information as described in the command description. Instead, if we see an argument listed as `-f`, then that means that what is listed is what you type.
## Required Arguments

The first method is to communicate a **required** argument, or one that is necessary for a command to function. These arguments will be listed inside of `caret brackets`, or `<>`, such as in the following:

`$> cat <$filename>`

So to use this command, you must include a file. Again, when providing the required argument, you do *not* include the `caret brackets`, that is only used to communicate that something is required. So if I wanted to run this command on `test.txt`, it would be ran as follows:

`$> cat test.txt`

Also note that in a shorter command, it is common to omit brackets for required arguments if the meaning is still clear without them. This will only ever be done with a required argument, and not with optional arguments. So for example, you may see the previous command documented as the following, still designating a required argument:

`$> cat $filename`


## Optional Arguments

Secondly, an argument can be communicated as being **optional**, or unnecessary for a command to function. Instead, these arguments will usually toggle settings for how a command is run. These arguments will be listed inside of `square brackets`, or `[]`, such as in the following:

`$> ls [$directory]`

So to use this command, you *may* provide a directory. Once more, when providing an optional argument, you do *not* include the `square brackets`, as that is only used for communication. So if providing a directory, the above command would be invoked as follows:

`$> ls C:/Users/username/Desktop`

## Embedded Arguments

Importantly, `optional` and `required` arguments can be combined. For example, there may be a case where an argument is not required, but *if included, another argument must be used*. This is not super common, but you may see it from time to time! These cases will be communicated as brackets inside of brackets. For example:

`tar [-f <$filename>]`

So here, if the optional `-f` is used, then you *must* include `filename` as well.

## Exclusive Arguments

In some more rare cases, two or more arguments may be exclusive to one another. Or in other words, if one argument is present, another argument may be forbidden. These are denoted using a vertical bar `|` separating two options. These may appear inside or outside of brackets, but the meaning is the same. An example of two optional arguments that exclude each other are in the following:

`cd [$destination | -]`

Where you can *either* add a variable argument `$destination` ***or*** a literal argument `-`, but not both.

## Identical Arguments

Sometimes, there are two arguments that are identical to one another. This is often the case when there is a long form and a short form for one command. Identical commands will be denotated using a comma `,`, such as in the following:

`touch $filename [-c, --no-create]`

Here, you can freely choose between using `-c` or `--no-create`, and they will behave identically

# Paths

Understanding *where* you are is important. A command line is functionally identical to your file explorer, just with a few extra capabilities. In fact, when Microsoft and Apple originally programmed their file explorers, they did essentially nothing more than add pictures to the command line so that it looks less intimidating!

Now often times, a command will require a `file` or a `directory` (or more colloquially called a `folder`). How, then, can you communicate where something is? We have two ways to do this. We can use an `absolute path` and a `relative path`.

## Absolute Path

An absolute path describes the exact location of a file or directory, starting from the hard drive. For example, if I have a file called `example.txt` located on my desktop, the `absolute path` would likely look something like this on a Windows computer:

`C:/Users/username/Desktop/example.txt`

This tells use the exact location for where we can find something.

## Relative Path

A `relative path` can sometimes be more convenient to navigate. Imagine you are providing directions to a grocery store. You would likely tell somebody the address, or a series of turns and roads. You would *not* say a store is located *On Earth, in North America, in Utah, in Provo, ...*. Your current location implies a lot about where you are, so why go through the trouble of being grotesquely precise? Instead, a `relative path` does just this. Your command line will always tell you "where you are" in its intro, or in the `$>` section. So for example, if I am currently located on my desktop on my command line, it would read as follows:

`C:/Users/username/Desktop$>`

From here, if I provide a file or directory name, the command line will check to see if it can be found in the context of your relative position. So for example, if we are in the desktop and want to interact with an `example.txt`, I could just invoke it as:

`example.txt`

Now, there are also three important special denotations that can be used with relative paths. First, you can use two periods `..` to denote the `parent directory` to your current location. So say I am inside of `C:/Users/username/Desktop/directory_1`, but I need to process a file that's in `C:/Users/username/Desktop/directory_2`, I can reference it as follows:

`../directory_2`

As the `..` would mean *go one level up*. This can also be stacked! So if I wanted to go two levels up, I could do `../../whatever`

The second important denotation is the tilde, or the squiggle `~`. This will denote your `home directory`. What that means is different on every computer, but it usually refers to, on Windows, `C:/Users/username`. Otherwise, this behaves the same as any other relative path, as you can reference a file with that being the start of the file path. If you want to know where precisely `~` is referring to on your computer, you can first run the command ` $> cd ~` and then the command `$> pwd`

The third important denotation is the forward slash `/`. We see this a lot in file paths, but it has a special meaning **when it is the first character in a path**. When this is the case, it refers to the `root` of your computer, or the very topmost directory. For a windows machine, this simply refers to `C:/`, or the C-drive. It is not too common that you will use the forward slash as a special denotation, but it is good to know what it is and what it communicates.

Also know, that the term used to describe your current location is **working directory**. 