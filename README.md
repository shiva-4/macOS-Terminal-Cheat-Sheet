# 🖥️ macOS Terminal Command Cheat Sheet

This is a quick reference for **macOS (Unix) terminal commands** that make daily development and system work easier.  
It’s designed to be dropped right into a GitHub repo for easy access.

---

## ✅ Basics

```bash
whoami            # current user
pwd               # print working directory
uname -a          # kernel/system info
sw_vers           # macOS version
date              # current date/time
uptime            # system uptime/load
```

---

## 📂 Files & Folders

```bash
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
```

---

## 📄 Viewing & Editing Files

```bash
cat file          # print file
less file         # paged viewer (q to quit)
/pattern          # search inside less
head -n 20 file   # first 20 lines
tail -f app.log   # follow log
nano file         # simple editor
vi file           # vim editor
wc -l file        # line count
```

---

## 🔎 Search & Find

```bash
find . -iname "*.png"       # find files by name
mdfind "project plan"       # mac Spotlight search
grep -Rni "TODO" .          # search file contents
```

---

## 🔁 Pipes & Redirection

```bash
command1 | command2         # pipe
command > out.txt           # redirect stdout
command >> out.txt          # append
command 2> err.txt          # redirect stderr
sort file | uniq -c         # count unique lines
```

---

## 🔐 Permissions

```bash
ls -l                       # see perms
chmod +x script.sh          # add execute
chown user:staff file       # change owner
sudo command                # run as admin
```

---

## 🗜️ Archive & Compress

```bash
zip -r project.zip project/
unzip project.zip
tar -czf archive.tgz folder/
tar -xzf archive.tgz
```

---

## ⚙️ Processes & System

```bash
ps aux            # processes
top               # live system usage
kill 1234         # kill by PID
pkill -f "node"   # kill by name
df -h             # disk usage
du -sh *          # folder sizes
```

---

## 🌐 Networking

```bash
ifconfig                 # network interfaces
ipconfig getifaddr en0   # your local IP
ping -c 4 example.com    # test connectivity
traceroute example.com   # route to host
nslookup example.com     # DNS lookup
curl -I https://site     # fetch headers
ssh user@host            # ssh login
scp file user@host:/path # copy over ssh
```

---

## 🍺 Homebrew (Package Manager)

```bash
brew update
brew search jq
brew install jq git wget
brew upgrade
brew cleanup
```

---

## 📦 Git

```bash
git init
git clone <url>
git status
git add -A
git commit -m "msg"
git push origin main
git pull --rebase
git log --oneline --graph --decorate --all
```

---

## 🍎 macOS Extras

```bash
open .                          # open Finder
open -a "Visual Studio Code" .  # open in VS Code
pbcopy < file.txt               # copy to clipboard
pbpaste > file.txt              # paste from clipboard
say "Build complete"            # text-to-speech
screencapture -i screenshot.png # interactive screenshot
diskutil list                   # disks/volumes
```

---

## 🧹 Handy Aliases (add to `~/.zshrc`)

```bash
alias ll='ls -alh'
alias ..='cd ..'
alias gs='git status'
alias gl='git log --oneline --graph --decorate --all'
alias ports='lsof -i -P | grep LISTEN'
```

---

## ⚠️ Safety Tips

- Be **very careful** with `rm -rf` (double check paths).
- Quote paths with spaces (`"My Folder/file.txt"`).
- Keep backups (Time Machine or `tmutil`).

---

📌 This cheat sheet is aimed at **developers, sysadmins, and learners** working on macOS.  
Contributions welcome!
