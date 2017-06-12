---
layout: concertina
title: NeoMutt - A Developer's View
---
# {{ page.title }}

NeoMutt has many improvements over Mutt.
Below is a list of all the differences between Mutt and NeoMutt.

This guide is correct as of Mutt-1.8.3 and NeoMutt-20170609.
This guide is written for **developers** of NeoMutt.
If you're a not a developer, see the [User's View](user).

## Removed

NeoMutt wants to remain compatible with Mutt, but it also wants to improve the
user's experience.  To achieve this, NeoMutt has added many features to Mutt and
removed very little.

### Files
### Features
### Configure

These options have been removed from configure.

| Options                   | Reason for Removal   |
| :------------------------ | -------------------- |
| --disable-iconv           | Use system version   |
| --disable-warnings        | Obsolete             |
| --enable-exact-address    | Obsolete             |
| --enable-external-dotlock | Obsolete             |
| --enable-hcache           | Use backend options  |
| --enable-nfs-fix          | Obsolete             |
| --with-exec-shell         | Obsolete             |
| --with-included-gettext   | Use system version   |
| --with-regex              | Use system version   |

### Variables
### Functions
### Commands
### Colours

## Changed

### Files
### Features
### Configure

configure has been extensively refactored:
- Easier to maintain
- Faster running
- Fewer unnecessary checks
- Better at discovering libraries
- Dependency on the wide-char version of ncurses

NeoMutt declared that
[POSIX:2001](https://github.com/neomutt/management/tree/master/standard-functions#readme)
was the base requirement for building.
This meant that many checks could be removed from configure.

These options have been removed, but the features remain.
The features didn't have any build dependencies, so they are **always** built
in.

| Options             | State    |
| :------------------ | -------- |
| --enable-compressed | Built in |
| --enable-imap       | Built in |
| --enable-mailtool   | Built in |
| --enable-pop        | Built in |
| --enable-sidebar    | Built in |
| --enable-smtp       | Built in |

### Variables
### Functions
### Commands
### Colours

## Added

### Files
### Features
### Configure

These configure options have been added to NeoMutt.

| Options             | Description                              |
| :------------------ | :--------------------------------------- |
| --disable-po        | Don't build the translations (.po files) |
| --enable-everything | Build everything possible                |
| --enable-fmemopen   | Unstable feature                         |
| --enable-lua        | Enable Lua Scripting                     |
| --enable-notmuch    | Enable NotMuch searching                 |

### Variables
### Functions
### Commands
### Colours

