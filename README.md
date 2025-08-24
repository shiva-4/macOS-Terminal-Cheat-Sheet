# 🖥️ macOS Terminal Command Cheat Sheet

This is a quick reference for **macOS (Unix) terminal commands** that make daily development and system work easier.  
It’s designed to be dropped right into a GitHub repo for easy access.

---

## Basics

```bash
whoami            # current user
pwd               # print working directory
uname -a          # kernel/system info
sw_vers           # macOS version
date              # current date/time
uptime            # system uptime/load

## **Files and Folders**

ls -lah           # list (long, all, human sizes)
cd /path/to/dir   # change directory
mkdir -p a/b/c    # make nested dirs
touch file.txt    # create empty file
cp -R src dst     # copy (recursive)
mv old new        # move/rename
rm file           # remove file
rm -rf dir        # ⚠️ remove folder recursively (careful!)
open .            # open Finder at current dir
open file.pdf     # open with default app



