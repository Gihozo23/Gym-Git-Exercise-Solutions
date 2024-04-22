# Gym-Git-Exercise-Solutions

## BUNDLE 1

### Exercise 1

```bash
HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions
$ git init
Initialized empty Git repository in C:/Users/HP/Desktop/theGym/Gym Git Exercise Solutions/.git/

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (master)
$ git branch -m main

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (main)
$ git add index.html

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (main)
$ git commit -m "first commit"
[main (root-commit) c223cbc] first commit
 1 file changed, 15 insertions(+)
 create mode 100644 index.html

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (main)
$ git remote add origin https://github.com/Gihozo23/Gym-Git-Exercise-Solutions.git

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (main)
$ git pull origin main
From https://github.com/Gihozo23/Gym-Git-Exercise-Solutions
 * branch            main       -> FETCH_HEAD
fatal: refusing to merge unrelated histories

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (main)
$ git pull origin main --allow-unrelated-histories
From https://github.com/Gihozo23/Gym-Git-Exercise-Solutions
 * branch            main       -> FETCH_HEAD
Merge made by the 'ort' strategy.
 README.md | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 README.md

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (main)
$ git push origin main
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (5/5), 715 bytes | 715.00 KiB/s, done.
Total 5 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/Gihozo23/Gym-Git-Exercise-Solutions.git
   2877821..6246112  main -> main

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (main)
$ git checkout -b dev
Switched to a new branch 'dev'

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (dev)
$ git checkout -b test
Switched to a new branch 'test'

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (test)
$ git checkout dev
Switched to branch 'dev'

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (dev)
$ git branch -d test
Deleted branch test (was 6246112).

```

### Exercise 2

```bash
P@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (dev)
$ git add home.html

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (dev)
$ git stash
Saved working directory and index state WIP on dev: 6246112 Merge branch 'main' of https://github.com/Gihozo23/Gym-Git-Exercise-Solutions

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (dev)
$ git add about.html

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (dev)
$ git stash
Saved working directory and index state WIP on dev: 6246112 Merge branch 'main' of https://github.com/Gihozo23/Gym-Git-Exercise-Solutions

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (dev)
$ git add team.html

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (dev)
$ git stash
Saved working directory and index state WIP on dev: 6246112 Merge branch 'main' of https://github.com/Gihozo23/Gym-Git-Exercise-Solutions

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (dev)
$ git stash list
stash@{0}: WIP on dev: 6246112 Merge branch 'main' of https://github.com/Gihozo23/Gym-Git-Exercise-Solutions
stash@{1}: WIP on dev: 6246112 Merge branch 'main' of https://github.com/Gihozo23/Gym-Git-Exercise-Solutions
stash@{2}: WIP on dev: 6246112 Merge branch 'main' of https://github.com/Gihozo23/Gym-Git-Exercise-Solutions

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (acedecb763ed1927ffb23dd78e5ae4cc3f02c558)

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (601b1b1024fbee80f343599753e082b5b13c9c01)

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (dev)
$ git commit -m "about and team page were added"
[dev 6d99e82] about and team page were added
 2 files changed, 30 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (dev)
$ git push origin
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (dev)
$ git push --set-upstream origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 566 bytes | 566.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/Gihozo23/Gym-Git-Exercise-Solutions/pull/new/dev
remote:
To https://github.com/Gihozo23/Gym-Git-Exercise-Solutions.git
 * /[new branch]      dev -> dev
branch 'dev' set up to track 'origin/dev'.

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (dev)
$ git stash pop stash@{0}
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (ad9317096c9a553ee968b24328643caa90800ac4)

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (dev)
$ git reset --hard
HEAD is now at 6d99e82 about and team page were added

```
## Bundle 2

### Exercise 1

```bash
HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (dev)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (ft/bundle-2)
$ git add services.html
fatal: pathspec 'services.html' did not match any files

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (ft/bundle-2)
$ git add services.html

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (ft/bundle-2)
$ git commit -m "services.html added"
[ft/bundle-2 52667e9] services.html added
 1 file changed, 15 insertions(+)
 create mode 100644 services.html

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (ft/bundle-2)
$ git push
fatal: The current branch ft/bundle-2 has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/bundle-2

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (ft/bundle-2)
$ git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 475 bytes | 475.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Gihozo23/Gym-Git-Exercise-Solutions/pull/new/ft/bundle-2
remote:
To https://github.com/Gihozo23/Gym-Git-Exercise-Solutions.git
 * /[new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (ft/bundle-2)
$ git checkout main
Switched to branch 'main'
Your branch is behind 'origin/main' by 3 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (main)
$ git pull
Updating 18db4f9..c5a7ba5
Fast-forward
 about.html    | 15 +++++++++++++++
 home.html     | 15 +++++++++++++++
 services.html | 15 +++++++++++++++
 3 files changed, 45 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 services.html

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (main)
$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (ft/service-redesign)
$ git add .

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (ft/service-redesign)
$ git commit -m "changes on the services page"
[ft/service-redesign b78eff8] changes on the services page
 1 file changed, 1 insertion(+)

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (ft/service-redesign)
$ git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (ft/service-redesign)
$ git push --set-upstream origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 332 bytes | 332.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/Gihozo23/Gym-Git-Exercise-Solutions/pull/new/ft/service-redesign
remote:
To https://github.com/Gihozo23/Gym-Git-Exercise-Solutions.git
 * /[new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

```
### Exercise 2

```bash
HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (main)
$ git add services.html

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (main)
$ git commit -m "changes on the services page"
[main 0e8f0a9] changes on the services page
 1 file changed, 1 insertion(+)

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 330 bytes | 330.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Gihozo23/Gym-Git-Exercise-Solutions.git
   7afb502..0e8f0a9  main -> main

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (main)
$ git diff

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (main)
$ git diff main ft/service-redesign services.html
diff --git a/services.html b/services.html
index 787972a..ad6e1e0 100644
--- a/services.html
+++ b/services.html
@@ -9,7 +9,7 @@
     <div>

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (main)
$ git merge ft/service-redesign
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (main|MERGING)
$ git commit -m "merging conflict services"
error: Committing is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.
U       services.html

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (main|MERGING)
$ git commit -m "merging conflict services"
[main c1a3148] merging conflict services

HP@DESKTOP-VK7L602 MINGW64 ~/Desktop/theGym/Gym Git Exercise Solutions (main)
$ git push
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 386 bytes | 386.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Gihozo23/Gym-Git-Exercise-Solutions.git
   0e8f0a9..c1a3148  main -> main

```
## Bundle 3

### Exercise 1