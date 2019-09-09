# Remove sidelined files

This script deletes files that are "sidelined", which is our lingo for files that are old, or backups, or temporary, or expired, etc.

Contents:

* [Introduction](#introduction)
* [Which files?](#which-files)
* [Related](#related)
* [Compatibility notes](#compatibility-notes)
* [Tracking](#tracking)


## Introduction

Syntax:

    $ rm-sidelined-files <dir>

Example:

    $ rm-sidelined-files /var/log


## Which files?

Files with extensions that are typically for sidelined files:

  * .old
  
  * .bak, .back, .backup
  
  * .tmp, .temp, .temporary


## Related

These scripts are for related purposes:

  * [rm-compressed-files](https://github.com/SixArm/rm-compressed-files)

  * [rm-dated-files](https://github.com/SixArm/rm-dated-files)

  * [rm-numbered-files](https://github.com/SixArm/rm-numbered-files)

  * [rm-rotated-files](https://github.com/SixArm/rm-rotated-files)

  * [rm-sidelined-files](https://github.com/SixArm/rm-sidelined-files)


## Compatibility notes

We prefer to be more compatible rather than system-specific.

  * To delete files, we prefer `-exec rm` vs. `-delete`.
    The former is more compatible, the latter is faster.

  * To regex match, we prefer patterns to be basic vs. extended.
    The former is more compatible, the latter is more modern.

  * We prefer POSIX code vs. shell-specific code.

  * We prefer the code to be more DAMP than DRY.
    For example, the code has separate name matching 
    for `.bz` and `.bz2`, even though we could combine these.


## Tracking

  * Command: rm-sidelined-files
  * Website: http://sixarm.com/rm-sidelined-files
  * Cloning: https://github.com/sixarm/rm-sidelined-files
  * Version: 4.0.1
  * Created: 2013-12-09
  * Updated: 2019-09-08
  * License: GPL
  * Contact: Joel Parker Henderson (joel@joelparkerhenderson.com)
  * Tracker: 35cc7c1096bbd8c5246949b5d200be15

