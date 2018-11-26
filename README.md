# $USER bin

A set of scripts to accelerate my daily work. The repository should be cloned into `$HOME/bin`. This path is already in system `$PATH` environment variable, so there is no need to append it.

## To convert files to executables

```bash
$ chmod +x $(ls -I ".gitignore" -I "*.md")
```

## Summary of scripts

### `gits [-a|--all]`

Print a brief git status of the repository.

```bash
$ gits
```

Output:
```bash
## master...origin/master
 M gitlog
 M gits
 M kexp
 M passgen
AM sizer
 M timer
 M where
?? gitsall
```

Argument `-a|--all` gives info about all branches.

```bash
$ gits -a
```

Output:
```bash
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/master
master (ahead 0) | (behind 0) origin/master
```

## `gitlog`

Print the commit logs.

## `kexp`

Starts playing a radio that I like to listen to.

## `passgen [<length>]`

Generates a random string. It can take an optional argument to indicate the length of the string.

```bash
$ passgen 20 
```

example output: 
```
vf1=|xHcL`s/t3zIBZi!
```

## `timer [<minutes>]`

Starts a countdown timer. Default time is 60 minutes.

```bash
$ timer 25
```

## `where <string>`

For a given term, it looks up all of its instances in the files and directories in the path that it was invoked. This has been useful for debugging.

```bash
$ where this_weird_variable_name
```

## `sizer`

Lists the folder/files and their disk usage, ordered by size.

Example output
```
280K    .git
24K     git-branch-status
4.0K    where
4.0K    timer
4.0K    sizer
4.0K    README.md
4.0K    passgen
4.0K    kexp
4.0K    gits
4.0K    gitlog
```