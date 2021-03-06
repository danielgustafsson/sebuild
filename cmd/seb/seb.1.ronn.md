seb(1) -- build your project
============================

## SYNOPSIS

`seb` [options] [--] [ninja-arguments]

## DESCRIPTION

The seb tool generates build.ninja files from special Builddesc files that
describe how various components of the build should be handled.

This is a very brief description. For information on how to write Builddesc
files refer to COMPILING.md.

## OPTIONS

`--with-flavor` string

  Only generate the specified flavors, multiple --with-flavor options are
  allowed to select many flavors. Usually not needed as each flavor is also a
  ninja pseudo-target, thus

    seb flavor

  should work just as well.

`--without-flavor` string

  Exclude the specified flavors from the build.

`--quiet`

  Suppress program output with `--quiet`.

`--debug`

  Enable debug output with `--debug`.

`--condition` string

  Add an active build condition, which can be used to select what files
  or flags are active.

`--install`

  Install required ninja files into $HOME/.seb. Note that seb will first
  look for the source directory for its package and use files from there
  if available, then look at prefix/share/seb and only after that fall
  back to $HOME/.seb.
  If you need to use this flag make sure to re-run it after you upgrade
  seb to install any new versions of the files. The files are included
  as part of the binary, no download is required.

## SEE ALSO

COMPILING.md
