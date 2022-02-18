## Terminal

We use the terminal to interact with different commands and programs like
[git][git].

Each operating system comes with a different type of terminal and some commands
may work a little bit differently on different operating systems.

If you use macOS then you can open [Terminal.app][terminal.app].
On Microsoft Windows you can use [PowerShell][powershell].
For this course we will use the [terminal][integrated_terminal] that is built
into VSCode and a [Codespace][codespace].

### Getting Started

For this lesson you will need to [open your Codespace][codespace] and then
launch VSCode and [open a Terminal][integrated_terminal].

The terminal is a portal that allows you interact with your computer.
It provides a command line interface that looks like this:

```bash
/workspaces/SparkleHub-lite
$
```

Start by typing command, like `ls`, followed by pressing the Enter key.
The terminal will execute that command and print the output from the command.

When you start up a new Codespace the default directory that the
terminal starts in is the `/workspaces/SparkleHub-lite` directory. This directory
contains all the code for the CodeChica++ final project.

### `man`

If you forget what a specific command does you can find the answer in the `man`
page. [`man`][man] is short for instruction *manual*. To look up a command in the
manual type [`man`][man] then the name of the command.

For example:

```bash
$ man man
MAN(1)                    Manual pager utils                             MAN(1)

NAME
       man - an interface to the system reference manuals

SYNOPSIS
       man [man options] [[section] page ...] ...
       man -k [apropos options] regexp ...
       man -K [man options] [section] term ...
       man -f [whatis options] page ...
       man -l [man options] file ...
       man -w|-W [man options] page ...

DESCRIPTION
       man  is  the  systems manual pager.  Each page argument given to man is
       normally the name of a program, utility or function.  The manual page
       associated with each of these arguments is then found and displayed.  A
       section, if provided, will direct man to look only in that section of
       the manual.  The default  action  is  to search  in  all  of the
       available sections following a pre-defined order (see DEFAULTS), and to
       show only the first page found, even if page  exists  in  several
       sections.
```

### `ls`

The [`ls`][ls] command will *list* all the files in a directory.

```bash
$ man ls
LS(1)                        User Commands                                LS(1)

NAME
       ls - list directory contents

SYNOPSIS
       ls [OPTION]... [FILE]...

DESCRIPTION
       List  information  about  the FILEs (the current directory by default).
       Sort entries alphabetically if none of -cftuvSUX nor --sort is specified.

       Mandatory arguments to long options are mandatory for short options too.
```

#### Examples

List files in the current directory:

```bash
/workspaces/SparkleHub-lite
$ ls
go.mod  go.sum  main.go  public  README.md  script  server.go  server_test.go
sparkle.go  sparkle_test.go
```

List the files in the `public` directory:

```bash
/workspaces/SparkleHub-lite
$ ls public/
application.js  css  favicon.ico  index.html  vendor
```

List the files using a long list format.

```bash
/workspaces/SparkleHub-lite
$ ls -l script/
total 16
-rwxrwxrwx 1 root root  57 Feb 18 19:32 server
-rwxrwxrwx 1 root root 254 Feb 18 19:32 sparkle
-rwxrwxrwx 1 root root  85 Feb 18 19:32 sparkles
-rwxrwxrwx 1 root root  63 Feb 18 19:32 test
```

List all files (including hidden ones) using a long list format.

```bash
/workspaces/SparkleHub-lite
$ ls -alh
total 60K
drwxrwxrwx+ 7 root root 4.0K Feb 18 19:32 .
drwxr-xrwx+ 4 root root 4.0K Feb 18 19:32 ..
drwxrwxrwx+ 2 root root 4.0K Feb 18 19:32 .devcontainer
drwxrwxrwx+ 8 root root 4.0K Feb 18 19:33 .git
drwxrwxrwx+ 3 root root 4.0K Feb 18 19:32 .github
-rw-rw-rw-  1 root root  401 Feb 18 19:32 go.mod
-rw-rw-rw-  1 root root 1.6K Feb 18 19:32 go.sum
-rw-rw-rw-  1 root root  355 Feb 18 19:32 main.go
drwxrwxrwx+ 4 root root 4.0K Feb 18 19:32 public
-rw-rw-rw-  1 root root 1.1K Feb 18 19:32 README.md
drwxrwxrwx+ 2 root root 4.0K Feb 18 19:32 script
-rw-rw-rw-  1 root root 1.5K Feb 18 19:32 server.go
-rw-rw-rw-  1 root root 2.2K Feb 18 19:32 server_test.go
-rw-rw-rw-  1 root root  753 Feb 18 19:32 sparkle.go
-rw-rw-rw-  1 root root 1.2K Feb 18 19:32 sparkle_test.go
```

### `pwd`

The [`pwd`][pwd] command can be used to *print* the *working directory*. This is very
helpful when you can't remember what directory you are in.

```bash
$ man pwd
PWD(1)                       User Commands                               PWD(1)

NAME
       pwd - print name of current/working directory

SYNOPSIS
       pwd [OPTION]...

DESCRIPTION
       Print the full filename of the current working directory.
```

### Examples

Print the current working directory.

```bash
$ pwd
/workspaces/SparkleHub-lite
```

### Change Directory `cd`

The [`cd`][cd] command can be used to *change directories*.
This builtin is useful when you want to switch to a different directory to do a
little bit of work from there.

```bash
$ help cd
cd: cd [-L|[-P [-e]] [-@]] [dir]
    Change the shell working directory.

    Change the current directory to DIR.
    The default DIR is the value of the HOME shell variable.
```

#### Examples

Change the current directory to your $HOME directory:

```bash
/workspaces/SparkleHub-lite
$ cd ~/
/home/username/
$
```

Change back to the previous directory:

```bash
/home/username/
$ cd -
/workspaces/SparkleHub
$
```

### `mkdir`

The [`mkdir`][mkdir] command can be used to *make* a new *directory*.

```bash
$ man mkdir
MKDIR(1)                     User Commands                             MKDIR(1)

NAME
       mkdir - make directories

SYNOPSIS
       mkdir [OPTION]... DIRECTORY...

DESCRIPTION
       Create the DIRECTORY(ies), if they do not already exist.
```

#### Examples

To create a new directory named `butterfly`.

```bash
/workspaces/SparkleHub-lite
$ mkdir butterfly
```

If a directory named `butterfly` already exists then you might get an error when
you run the `mkdir` command. Adding the `-p` option means that `mkdir` will
create the directory if it doesn't already exist and will just do nothing
(instead of giving you an error) if it does exist:

```bash
/workspaces/SparkleHub-lite
$ mkdir -p skittles-and-rainbows
```

Next, try the [git][git] guide!

[cd]: https://man7.org/linux/man-pages/man1/cd.1p.html
[codespace]: ./github.html#codespaces
[git]: ./git.html
[integrated_terminal]: ./vscode.html#integrated-terminal
[ls]: https://man7.org/linux/man-pages/man1/ls.1.html
[man]: https://man7.org/linux/man-pages/man1/man.1.html
[powershell]: https://docs.microsoft.com/en-us/powershell/
[pwd]: https://man7.org/linux/man-pages/man1/pwd.1.html
[mkdir]: https://man7.org/linux/man-pages/man1/mkdir.1.html
[terminal.app]: https://support.apple.com/en-ca/guide/terminal/welcome/mac
