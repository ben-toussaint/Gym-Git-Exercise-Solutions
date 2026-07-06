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