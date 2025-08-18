# GIT Exercise
## Bundle 1 
### Exercise 1
```bash
user@Baraka MINGW64 /
$ cd ~

user@Baraka MINGW64 ~
$ mkdir git-exercise-1
user@Baraka MINGW64 ~
$ cd git-exercise-1

user@Baraka MINGW64 ~/git-exercise-1
$ git init
Initialized empty Git repository in C:/Users/user/git-exercise-1/.git/

user@Baraka MINGW64 ~/git-exercise-1 (master)
$ echo "<h1>Hello Git, This is the first exercise</h1>" > index.html

user@Baraka MINGW64 ~/git-exercise-1 (master)
$ git branch

user@Baraka MINGW64 ~/git-exercise-1 (master)
$ git branch -M main
user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git add .
warning: in the working copy of 'index.html', LF will be replaced by CRLF the next time Git touches it
user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git commit -m "Add index.html file and content"
[main (root-commit) 5c17c95] Add index.html file and content
 1 file changed, 1 insertion(+)
 create mode 100644 index.html

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git remote add origin https://github.com/Kubanabaraka/git-exercise-1.git~     
user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git push origin main
fatal: unable to access 'https://github.com/Kubanabaraka/git-exercise-1.git~/': Failed to connect to github.com port 443 after 21212 ms: Could not connect to server
user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git remote -v
origin  https://github.com/Kubanabaraka/git-exercise-1.git~ (fetch)
origin  https://github.com/Kubanabaraka/git-exercise-1.git~ (push)

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git remote set-url origin https://github.com/Kubanabaraka/git-exercise-1.git

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git push origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 282 bytes | 282.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Kubanabaraka/git-exercise-1.git
 * [new branch]      main -> main

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git checkout -b dev
Switched to a new branch 'dev'

user@Baraka MINGW64 ~/git-exercise-1 (dev)
$ git checkout -b test
Switched to a new branch 'test'

user@Baraka MINGW64 ~/git-exercise-1 (test)
$ git checkout dev
Switched to branch 'dev'

user@Baraka MINGW64 ~/git-exercise-1 (dev)
$ git branch -d test
Deleted branch test (was 5c17c95).

user@Baraka MINGW64 ~/git-exercise-1 (dev)
$ cd ~

user@Baraka MINGW64 ~
$ git clone https://github.com/Kubanabaraka/Gym-Git-Exercise-Solutions.git
Cloning into 'Gym-Git-Exercise-Solutions'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (3/3), done.
user@Baraka MINGW64 ~
$ cd Gym-Git-Exercise-Solutions~
bash: cd: Gym-Git-Exercise-Solutions~: No such file or directory

user@Baraka MINGW64 ~
$ cd Gym-Git-Exercise-Solutions

user@Baraka MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ ls
README.md

user@Baraka MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$ code .

user@Baraka MINGW64 ~/Gym-Git-Exercise-Solutions (main)
$

```
