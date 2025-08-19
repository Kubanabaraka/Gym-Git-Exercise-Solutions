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
### Exercise 2
```bash

user@Baraka MINGW64 ~
$ cd git-exercise-1

user@Baraka MINGW64 ~/git-exercise-1 (dev)
$ git branch
* dev
  main

user@Baraka MINGW64 ~/git-exercise-1 (dev)
$ git status
On branch dev
nothing to commit, working tree clean

user@Baraka MINGW64 ~/git-exercise-1 (dev)
$ git checkout main
Switched to branch 'main'

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git status
On branch main
nothing to commit, working tree clean

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git add home.html

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git stash save "Added home.html"
Saved working directory and index state On main: Added home.html

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git status
On branch main
nothing to commit, working tree clean

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        about.html

nothing added to commit but untracked files present (use "git add" to track)


user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git add about.html

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git stash save "Add about.html"
Saved working directory and index state On main: Add about.html

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git status
On branch main
nothing to commit, working tree clean

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git add team.html

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git stash save "Add team.html"
Saved working directory and index state On main: Add team.html

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git stash list
stash@{0}: On main: Add team.html
stash@{1}: On main: Add about.html
stash@{2}: On main: Added home.html

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git stash pop stash@{1}
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (29f42c09e80dcc2d71669ef9a4745035df1a64e2)

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git stash list
stash@{0}: On main: Add team.html
stash@{1}: On main: Added home.html

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git stash pop stash@{1}
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (5e7be72db23f260da9c1941609ec61d7fcf24d8c)

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git stash list
stash@{0}: On main: Add team.html

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git add.
git: 'add.' is not a git command. See 'git --help'.

The most similar command is
        add

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git add .

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git status
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html


user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git commit -m "Add home.html And about.html"
[main 4998d3b] Add home.html And about.html
 2 files changed, 26 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 543 bytes | 181.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/Kubanabaraka/git-exercise-1.git
   5c17c95..4998d3b  main -> main

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git stash pop stash@{0}
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped stash@{0} (2f368ae70af95279e5bf400d6ca6e633f4a8ddf8)

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git reset --hard
HEAD is now at 4998d3b Add home.html And about.html

user@Baraka MINGW64 ~/git-exercise-1 (main)
$

```