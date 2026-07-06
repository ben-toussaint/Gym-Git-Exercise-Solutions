# Gym-Git-Exercise-Solutions
## Bundle 1
### Exercise 1

```bash
MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git init
Reinitialized existing Git repository in C:/Users/MUGABE/Desktop/Gym-Git-Exercis
e-Solutions/.git/

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ touch file1.txt

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ echo "Hello" >>file1.txt

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git branch -M master

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (master)
$ git branch -M main

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git add .
warning: in the working copy of 'file1.txt', LF will be replaced by CRLF the nex
t time Git touches it

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git add -f .

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git commit -m "initial commit"
[main 14916d5] initial commit
 1 file changed, 2 insertions(+)
 create mode 100644 file1.txt

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git remote -v
origin  https://github.com/ben-toussaint/Gym-Git-Exercise-Solutions.git (fetch)
origin  https://github.com/ben-toussaint/Gym-Git-Exercise-Solutions.git (push)

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git push -u origin main
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 300 bytes | 150.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/ben-toussaint/Gym-Git-Exercise-Solutions.git
   933d355..14916d5  main -> main
branch 'main' set up to track 'origin/main'.

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git checkout -b dev
Switched to a new branch 'dev'

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git branch
* dev
  main

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git checkout -b test
Switched to a new branch 'test'

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (test)
$ git checkout dev
Switched to branch 'dev'

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git branch -d test
Deleted branch test (was 14916d5).

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git branch
* dev
  main
```
## Exercise 2
```bash
MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ touch home.html

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git status -s
?? home.html

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git stash -u
Saved working directory and index state WIP on dev: 2138eee README initial commi
t

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ touch team.html

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git stash -u
Saved working directory and index state WIP on dev: 2138eee README initial commi
t

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ touch about.html

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git stash -u
Saved working directory and index state WIP on dev: 2138eee README initial commi
t
g
MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git status -s

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git stash list
stash@{0}: WIP on dev: 2138eee README initial commit
stash@{1}: WIP on dev: 2138eee README initial commit
stash@{2}: WIP on dev: 2138eee README initial commit

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git stash show ^C

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git stash show stash@{0}

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git stash pop stash@{0}
Already up to date.
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

nothing added to commit but untracked files present (use "git add" to track)
Dropped stash@{0} (10e36c036a4cd3ce8b0f1443379c5e8f986ef2e8)

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git stash list
stash@{0}: WIP on dev: 2138eee README initial commit
stash@{1}: WIP on dev: 2138eee README initial commit

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git stash pop stash@{1}
Already up to date.
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html
        home.html

nothing added to commit but untracked files present (use "git add" to track)
Dropped stash@{1} (76c761624afa9c9547744940a70a9ce2b9b7e4b8)

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git commit -am "about and home initial commit"
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html
        home.html

nothing added to commit but untracked files present (use "git add" to track)

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git add .

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git commit -m "about and home initial commit"
[dev b77ebaf] about and home initial commit
 2 files changed, 20 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git push origin main
Everything up-to-date

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git status -s

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git stash list
stash@{0}: WIP on dev: 2138eee README initial commit

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git stash pop stash@{0}
Already up to date.
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)
Dropped stash@{0} (3efc63c33e9e59a9f8cdf1593c0d0ea333964860)

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git reset --hard HEAD
HEAD is now at b77ebaf about and home initial commit

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git status -s
?? team.html

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git reset --hard HEAD
HEAD is now at b77ebaf about and home initial commit

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git status -s
?? team.html
```