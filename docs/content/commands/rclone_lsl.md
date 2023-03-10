---
title: "rclone lsl"
description: "List the objects in path with modification time, size and path."
slug: rclone_lsl
url: /commands/rclone_lsl/
versionIntroduced: v1.02
# autogenerated - DO NOT EDIT, instead edit the source code in cmd/lsl/ and as part of making a release run "make commanddocs"
---
# rclone lsl

List the objects in path with modification time, size and path.

## Synopsis


Lists the objects in the source path to standard output in a human
readable format with modification time, size and path. Recurses by default.

Eg

    $ rclone lsl swift:bucket
        60295 2016-06-25 18:55:41.062626927 bevajer5jef
        90613 2016-06-25 18:55:43.302607074 canole
        94467 2016-06-25 18:55:43.046609333 diwogej7
        37600 2016-06-25 18:55:40.814629136 fubuwic


Any of the filtering options can be applied to this command.

There are several related list commands

  * `ls` to list size and path of objects only
  * `lsl` to list modification time, size and path of objects only
  * `lsd` to list directories only
  * `lsf` to list objects and directories in easy to parse format
  * `lsjson` to list objects and directories in JSON format

`ls`,`lsl`,`lsd` are designed to be human-readable.
`lsf` is designed to be human and machine-readable.
`lsjson` is designed to be machine-readable.

Note that `ls` and `lsl` recurse by default - use `--max-depth 1` to stop the recursion.

The other list commands `lsd`,`lsf`,`lsjson` do not recurse by default - use `-R` to make them recurse.

Listing a nonexistent directory will produce an error except for
remotes which can't have empty directories (e.g. s3, swift, or gcs -
the bucket-based remotes).


```
rclone lsl remote:path [flags]
```

## Options

```
  -h, --help   help for lsl
```

See the [global flags page](/flags/) for global options not listed here.

## SEE ALSO

* [rclone](/commands/rclone/)	 - Show help for rclone commands, flags and backends.

