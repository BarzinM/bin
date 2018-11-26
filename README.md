# $USER bin

A set of scripts to accelerate my daily work. The repository should be cloned into `$HOME/bin`. This path is already in system `$PATH` environment variable, so there is no need to append it.

## To convert files to executables

```bash
$ chmod +x $(ls -I ".gitignore" -I "*.md")
```

## Summary of scripts

### `gits`

Print a brief git status of the repository.

## `gitlog`

Print the commit logs.

## `kexp`

Starts playing a radio that I like to listen to.

## `passgen`

Generates a random string. It can take an optional argument to indicate the length of the string.

```bash
$ passgen 20 # example output: vf1=|xHcL`s/t3zIBZi!
```

## `timer`

Starts a countdown timer. Default time is 60 minutes.

```bash
$ timer 25
```

## `where`

For a given term, it looks up all of its instances in the files and directories in the path that it was invoked. This has been useful for debugging.

```bash
$ where this_weird_variable_name
```