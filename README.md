# Gym-Git-Exercise-Solutions

##BUNDLE 1

###Exercise 1

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

###Exercise 2