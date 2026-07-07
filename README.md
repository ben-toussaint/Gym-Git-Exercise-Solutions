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
# Bundle 2
## Exercise 1
```bash
MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ touch service.html

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git status -s
?? service.html

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git commit -am "service initial commit"
On branch ft/bundle-2
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        service.html

nothing added to commit but untracked files present (use "git add" to track)

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git add .
i
MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git commit -m "service initial commit"
[ft/bundle-2 01b3aba] service initial commit
 1 file changed, 11 insertions(+)
 create mode 100644 service.html

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git branch
  dev
* ft/bundle-2
  main

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git push origin main
Everything up-to-date

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git push origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 482 bytes | 160.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/ben-toussaint/Gym-Git-Exercise-Solutions/pull/new/ft/bundle-2
remote:
To https://github.com/ben-toussaint/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/bundle-2)
```
## Exercise 2
```bash

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (dev)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ touch service.html

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git add .
i
MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git commit -m "added a paragraph in service"
[ft/service-redesign 503161a] added a paragraph in service
 1 file changed, 1 insertion(+)

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git status -s

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git push origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 396 bytes | 396.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/ben-toussaint/Gym-Git-Exercise-Solutions/pull/new/ft/service-redesign
remote:
To https://github.com/ben-toussaint/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/service-redesign -> ft/service-redesign

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git status -s

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git branch
  dev
  ft/bundle-2
  ft/service-redesign
* main

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ start service.html

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git status -s
 M service.html
g
MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git add .
i
MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git commit -m "I added different paragraph in main branch"
[main bade186] I added different paragraph in main branch
 1 file changed, 1 insertion(+), 1 deletion(-)

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git push origin main
To https://github.com/ben-toussaint/Gym-Git-Exercise-Solutions.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/ben-toussaint/Gym-Git-Exercise-Solutions.git'
hint: Updates were rejected because the remote contains work that you do not
hint: have locally. This is usually caused by another repository pushing to
hint: the same ref. If you want to integrate the remote changes, use
hint: 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git status -s

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git status -s

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git pull origin main
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (2/2), 965 bytes | 60.00 KiB/s, done.
From https://github.com/ben-toussaint/Gym-Git-Exercise-Solutions
 * branch            main       -> FETCH_HEAD
   4059cf5..7427bfd  main       -> origin/main
Merge made by the 'ort' strategy.
 README.md  | 273 +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 about.html |  10 +++
 home.html  |  10 +++
 3 files changed, 293 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git status -s

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git push origin main
Enumerating objects: 9, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (5/5), done.
Writing objects: 100% (5/5), 673 bytes | 673.00 KiB/s, done.
Total 5 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 3 local objects.
To https://github.com/ben-toussaint/Gym-Git-Exercise-Solutions.git
   7427bfd..5e036c2  main -> main

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git diff

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git diff main
diff --git a/README.md b/README.md
index bfb73af..79867dc 100644
--- a/README.md
+++ b/README.md
@@ -1,274 +1 @@
 # Gym-Git-Exercise-Solutions
-## Bundle 1
-### Exercise 1
-
-```bash
-MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
-$ git init
-Reinitialized existing Git repository in C:/Users/MUGABE/Desktop/Gym-Git-Exercis
-e-Solutions/.git/
-
-MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
-$ touch file1.txt
-
-MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
-$ echo "Hello" >>file1.txt
-
-MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
-$ git branch -M master
-
-MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (master)
-$ git branch -M main
-
-MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
-$ git add .
-warning: in the working copy of 'file1.txt', LF will be replaced by CRLF the nex
-t time Git touches it
-
-MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
-$ git add -f .
-
-MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
-$ git commit -m "initial commit"
-[main 14916d5] initial commit
- 1 file changed, 2 insertions(+)
- create mode 100644 file1.txt
-
-MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
-$ git remote -v
-origin  https://github.com/ben-toussaint/Gym-Git-Exercise-Solutions.git (fetch)
-origin  https://github.com/ben-toussaint/Gym-Git-Exercise-Solutions.git (push)
-
-MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
-$ git push -u origin main

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git diff ft/service-redesign main
diff --git a/README.md b/README.md
index 79867dc..bfb73af 100644
--- a/README.md
+++ b/README.md
@@ -1 +1,274 @@
 # Gym-Git-Exercise-Solutions
+## Bundle 1
+### Exercise 1
+
+```bash
+MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
+$ git init
+Reinitialized existing Git repository in C:/Users/MUGABE/Desktop/Gym-Git-Exercis
+e-Solutions/.git/
+
+MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
+$ touch file1.txt
+
+MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
+$ echo "Hello" >>file1.txt
+
+MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
+$ git branch -M master
+
+MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (master)
+$ git branch -M main
+
+MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
+$ git add .
+warning: in the working copy of 'file1.txt', LF will be replaced by CRLF the nex
+t time Git touches it
+
+MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
+$ git add -f .
+
+MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
+$ git commit -m "initial commit"
+[main 14916d5] initial commit
+ 1 file changed, 2 insertions(+)
+ create mode 100644 file1.txt
+
+MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
+$ git remote -v
+origin  https://github.com/ben-toussaint/Gym-Git-Exercise-Solutions.git (fetch)
+origin  https://github.com/ben-toussaint/Gym-Git-Exercise-Solutions.git (push)
+
+MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (main)
+$ git push -u origin main

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git merge main
Auto-merging service.html
CONFLICT (content): Merge conflict in service.html
Automatic merge failed; fix conflicts and then commit the result.

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign|MERGING)
$ git status -s
M  README.md
A  about.html
A  home.html
UU service.html

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign|MERGING)
$ git add .

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign|MERGING)
$ git commit -m "I solved conflict"
[ft/service-redesign 5774f25] I solved conflict

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git status -s

MUGABE@DESKTOP-JNTT3PG MINGW64 ~/Desktop/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git push origin ft/service-redesign
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 412 bytes | 206.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/ben-toussaint/Gym-Git-Exercise-Solutions.git
   503161a..5774f25  ft/service-redesign -> ft/service-redesign
```