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

## Bundle 2 
### Exercise 1
```bash
user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

user@Baraka MINGW64 ~/git-exercise-1 (ft/bundle-2)
$ git status
On branch ft/bundle-2
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        services.html

nothing added to commit but untracked files present (use "git add" to track)

user@Baraka MINGW64 ~/git-exercise-1 (ft/bundle-2)
$ git add services.html

user@Baraka MINGW64 ~/git-exercise-1 (ft/bundle-2)
$ git commit -m "Add services.html with servises list"
[ft/bundle-2 28e1c6c] Add services.html with servises list
 1 file changed, 17 insertions(+)
 create mode 100644 services.html

user@Baraka MINGW64 ~/git-exercise-1 (ft/bundle-2)
$ git push -u origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 517 bytes | 517.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/Kubanabaraka/git-exercise-1/pull/new/ft/bundle-
remote:
To https://github.com/Kubanabaraka/git-exercise-1.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.

user@Baraka MINGW64 ~/git-exercise-1 (ft/bundle-2)
$

```

### Exercise 2
```bash
user@Baraka MINGW64 ~/gitrevision (main)
$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

user@Baraka MINGW64 ~/gitrevision (ft/service-redesign)
$ git status
On branch ft/service-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   service.html

no changes added to commit (use "git add" and/or "git commit -a")

user@Baraka MINGW64 ~/gitrevision (ft/service-redesign)
$ git add .

user@Baraka MINGW64 ~/gitrevision (ft/service-redesign)
$ git commit -m "Add new heading"
[ft/service-redesign 42f2cce] Add new heading
 1 file changed, 1 insertion(+), 1 deletion(-)

user@Baraka MINGW64 ~/gitrevision (ft/service-redesign)
$ git push
fatal: The current branch ft/service-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/service-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


user@Baraka MINGW64 ~/gitrevision (ft/service-redesign)
$ git push --set-upstream origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 305 bytes | 305.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/Kubanabaraka/gitrevision/pull/new/ft/service-redesign
remote:
To https://github.com/Kubanabaraka/gitrevision.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

user@Baraka MINGW64 ~/gitrevision (ft/service-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

user@Baraka MINGW64 ~/gitrevision (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

user@Baraka MINGW64 ~/gitrevision (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   service.html

no changes added to commit (use "git add" and/or "git commit -a")

user@Baraka MINGW64 ~/gitrevision (main)
$ git add .

user@Baraka MINGW64 ~/gitrevision (main)
$ git commit -m "Add old services"
[main f6caa40] Add old services
 1 file changed, 1 insertion(+), 1 deletion(-)

user@Baraka MINGW64 ~/gitrevision (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 305 bytes | 305.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Kubanabaraka/gitrevision.git
   feb4f68..f6caa40  main -> main

user@Baraka MINGW64 ~/gitrevision (main)
$ git checkout ft/service-redesign
Switched to branch 'ft/service-redesign'
Your branch is up to date with 'origin/ft/service-redesign'.

user@Baraka MINGW64 ~/gitrevision (ft/service-redesign)
$ git diff main..ft/service-redesign
diff --git a/service.html b/service.html
index 4ac7c7b..4bd3e0a 100644
--- a/service.html
+++ b/service.html
@@ -6,7 +6,7 @@
     <title>Services</title>
 </head>
 <body>
-    <h1>Our Old Services</h1>
+    <h1>Our New Services</h1>
     <ul>
         <li>Service 1</li>
         <li>Service 2</li>

user@Baraka MINGW64 ~/gitrevision (ft/service-redesign)
$ git merge main
Auto-merging service.html
[ft/service-redesign c0372c2] Merge branch 'main' into ft/service-redesign

user@Baraka MINGW64 ~/gitrevision (ft/service-redesign)
$ git push origin ft/service-redesign
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 384 bytes | 384.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Kubanabaraka/gitrevision.git
   42f2cce..c0372c2  ft/service-redesign -> ft/service-redesign

user@Baraka MINGW64 ~/gitrevision (ft/service-redesign)
$

```
## Bundle 3 
### Exercise 1
```bash
user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

user@Baraka MINGW64 ~/git-exercise-1 (ft/team-page)
$ git status
On branch ft/team-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)

user@Baraka MINGW64 ~/git-exercise-1 (ft/team-page)
$ git add team.html

user@Baraka MINGW64 ~/git-exercise-1 (ft/team-page)
$ git commit -m "Add team page"
[ft/team-page c6e8098] Add team page
 1 file changed, 19 insertions(+)
 create mode 100644 team.html

user@Baraka MINGW64 ~/git-exercise-1 (ft/team-page)
$ git push
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


user@Baraka MINGW64 ~/git-exercise-1 (ft/team-page)
$  git push --set-upstream origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 610 bytes | 610.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/Kubanabaraka/git-exercise-1/pull/new/ft/team-page
remote:
To https://github.com/Kubanabaraka/git-exercise-1.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.

user@Baraka MINGW64 ~/git-exercise-1 (ft/team-page)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

user@Baraka MINGW64 ~/git-exercise-1 (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

user@Baraka MINGW64 ~/git-exercise-1 (ft/team-page)
$ git log
commit c6e80989f65d9df9408409ad2131e413d5ddb960 (HEAD -> ft/team-page, origin/ft/team-page)
Author: Kubanabaraka <byukusengekubanabarakapascal@gmail.com>
Date:   Thu Aug 21 13:22:47 2025 +0200

    Add team page

commit e5512b5b70f0b014b1fa4b571f558cbb23ecdea8 (origin/main, origin/HEAD, main,
 ft/contact-page)
Author: Kubanabaraka <byukusengekubanabarakapascal@gmail.com>
Date:   Thu Aug 21 11:21:52 2025 +0200

    feat: Add new services

commit 65085dee3eb223c2b4508ed048302e5022270efb
Author: Kubanabaraka <byukusengekubanabarakapascal@gmail.com>
Date:   Wed Aug 20 22:07:02 2025 +0200

    Main: Add footer and some services

commit c34b57bc67ac8fae54ca1def9ae3cdeae97746de
Merge: 4998d3b 28e1c6c
Author: DIVINEakisa <akisadivine11@gmail.com>
Date:   Wed Aug 20 14:39:11 2025 +0200

    Merge pull request #1 from Kubanabaraka/ft/bundle-2

:

    Add team page

commit e5512b5b70f0b014b1fa4b571f558cbb23ecdea8 (origin/main, origin/HEAD, main, ft/contact-page)
Author: Kubanabaraka <byukusengekubanabarakapascal@gmail.com>
Date:   Thu Aug 21 11:21:52 2025 +0200

    feat: Add new services

commit 65085dee3eb223c2b4508ed048302e5022270efb
Author: Kubanabaraka <byukusengekubanabarakapascal@gmail.com>
Date:   Wed Aug 20 22:07:02 2025 +0200

    Main: Add footer and some services

commit c34b57bc67ac8fae54ca1def9ae3cdeae97746de
Merge: 4998d3b 28e1c6c
Author: DIVINEakisa <akisadivine11@gmail.com>
Date:   Wed Aug 20 14:39:11 2025 +0200

    Merge pull request #1 from Kubanabaraka/ft/bundle-2

:

    Add team page

commit e5512b5b70f0b014b1fa4b571f558cbb23ecdea8 (origin/main, origin/HEAD, main, ft/contact-page)
Author: Kubanabaraka <byukusengekubanabarakapascal@gmail.com>
Date:   Thu Aug 21 11:21:52 2025 +0200

    feat: Add new services

commit 65085dee3eb223c2b4508ed048302e5022270efb
Author: Kubanabaraka <byukusengekubanabarakapascal@gmail.com>
Date:   Wed Aug 20 22:07:02 2025 +0200

    Main: Add footer and some services

commit c34b57bc67ac8fae54ca1def9ae3cdeae97746de
Merge: 4998d3b 28e1c6c
Author: DIVINEakisa <akisadivine11@gmail.com>
Date:   Wed Aug 20 14:39:11 2025 +0200

    Merge pull request #1 from Kubanabaraka/ft/bundle-2


user@Baraka MINGW64 ~/git-exercise-1 (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

user@Baraka MINGW64 ~/git-exercise-1 (ft/contact-page)
$ git cherry-pick c6e80989f65d9df9408409ad2131e413d5ddb960
[ft/contact-page bf214bc] Add team page
 Date: Thu Aug 21 13:22:47 2025 +0200
 1 file changed, 19 insertions(+)
 create mode 100644 team.html

user@Baraka MINGW64 ~/git-exercise-1 (ft/contact-page)
$ git status
On branch ft/contact-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        contact.html

nothing added to commit but untracked files present (use "git add" to track)

user@Baraka MINGW64 ~/git-exercise-1 (ft/contact-page)
$ git add .

user@Baraka MINGW64 ~/git-exercise-1 (ft/contact-page)
$ git commit -m "feat: Add contact page"
[ft/contact-page 5d81fbc] feat: Add contact page
 1 file changed, 17 insertions(+)
 create mode 100644 contact.html

user@Baraka MINGW64 ~/git-exercise-1 (ft/contact-page)
$ git push
fatal: The current branch ft/contact-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/contact-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


user@Baraka MINGW64 ~/git-exercise-1 (ft/contact-page)
$  git push --set-upstream origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 16 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 1.12 KiB | 1.12 MiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/Kubanabaraka/git-exercise-1/pull/new/ft/contact-page
remote:
To https://github.com/Kubanabaraka/git-exercise-1.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

user@Baraka MINGW64 ~/git-exercise-1 (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

user@Baraka MINGW64 ~/git-exercise-1 (ft/faq-page)
$ git status
On branch ft/faq-page
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        faq.html

nothing added to commit but untracked files present (use "git add" to track)

user@Baraka MINGW64 ~/git-exercise-1 (ft/faq-page)
$ git add .

user@Baraka MINGW64 ~/git-exercise-1 (ft/faq-page)
$ git commit -m "feat: Add faq page"
[ft/faq-page 4dcca76] feat: Add faq page
 1 file changed, 21 insertions(+)
 create mode 100644 faq.html

user@Baraka MINGW64 ~/git-exercise-1 (ft/faq-page)
$ git push
fatal: The current branch ft/faq-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/faq-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


user@Baraka MINGW64 ~/git-exercise-1 (ft/faq-page)
$ git push --set-upstream origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 651 bytes | 651.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/Kubanabaraka/git-exercise-1/pull/new/ft/faq-pag
remote:
To https://github.com/Kubanabaraka/git-exercise-1.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

user@Baraka MINGW64 ~/git-exercise-1 (ft/faq-page)
$ git log
commit 4dcca769f20996dd6ab8be07d8bbfad3fa1b80ff (HEAD -> ft/faq-page, origin/ft/faq-page)
Author: Kubanabaraka <byukusengekubanabarakapascal@gmail.com>
[ft/faq-page 1767d39] Revert "Add team page"
 1 file changed, 19 deletions(-)
 delete mode 100644 team.html

user@Baraka MINGW64 ~/git-exercise-1 (ft/faq-page)
$ git log
commit 1767d39b09da3771686bce9aa969ce49e29449b5 (HEAD -> ft/faq-page)
Author: Kubanabaraka <byukusengekubanabarakapascal@gmail.com>
Date:   Thu Aug 21 13:54:57 2025 +0200

    Revert "Add team page"

    This reverts commit bf214bc727d507ba4818b13277186b3ec9b01feb.

commit 4dcca769f20996dd6ab8be07d8bbfad3fa1b80ff (origin/ft/faq-page)
Author: Kubanabaraka <byukusengekubanabarakapascal@gmail.com>
Date:   Thu Aug 21 13:48:31 2025 +0200

    feat: Add faq page

commit 5d81fbc78b96554778072d43a18346460e2010d8 (origin/ft/contact-page, ft/contact-page)
Author: Kubanabaraka <byukusengekubanabarakapascal@gmail.com>
Date:   Thu Aug 21 13:41:21 2025 +0200

    feat: Add contact page

commit bf214bc727d507ba4818b13277186b3ec9b01feb
Author: Kubanabaraka <byukusengekubanabarakapascal@gmail.com>

user@Baraka MINGW64 ~/git-exercise-1 (ft/faq-page)
$ git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 16 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 283 bytes | 283.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Kubanabaraka/git-exercise-1.git
   4dcca76..1767d39  ft/faq-page -> ft/faq-page

user@Baraka MINGW64 ~/git-exercise-1 (ft/faq-page)
$

```
### Exercise 2
```bash
user@Baraka MINGW64 ~/git-exercise-1 (ft/faq-page)
$ git checkout -b ft/home-page-redesign
Switched to a new branch 'ft/home-page-redesign'

user@Baraka MINGW64 ~/git-exercise-1 (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git add .

user@Baraka MINGW64 ~/git-exercise-1 (main)

$ git commit -m "feat: Add home page content"
[main f85d520] feat: Add home page content
 1 file changed, 3 insertions(+)

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 389 bytes | 389.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/Kubanabaraka/git-exercise-1.git
   e5512b5..f85d520  main -> main

user@Baraka MINGW64 ~/git-exercise-1 (main)
$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

user@Baraka MINGW64 ~/git-exercise-1 (ft/home-page-redesign)
$ git rebase main
Successfully rebased and updated refs/heads/ft/home-page-redesign.

user@Baraka MINGW64 ~/git-exercise-1 (ft/home-page-redesign)
$ git status
On branch ft/home-page-redesign
nothing to commit, working tree clean

user@Baraka MINGW64 ~/git-exercise-1 (ft/home-page-redesign)
$ git status
On branch ft/home-page-redesign
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

no changes added to commit (use "git add" and/or "git commit -a")

user@Baraka MINGW64 ~/git-exercise-1 (ft/home-page-redesign)
$ git add .

user@Baraka MINGW64 ~/git-exercise-1 (ft/home-page-redesign)
$ git commit -m "feat: Add New Content To Home Page"
[ft/home-page-redesign 9818ad3] feat: Add New Content To Home Page
 1 file changed, 3 insertions(+)

user@Baraka MINGW64 ~/git-exercise-1 (ft/home-page-redesign)
$ git push
fatal: The current branch ft/home-page-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/home-page-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


user@Baraka MINGW64 ~/git-exercise-1 (ft/home-page-redesign)

$ git push --set-upstream origin ft/home-page-redesign
Enumerating objects: 16, done.
Counting objects: 100% (16/16), done.
Delta compression using up to 16 threads
Compressing objects: 100% (14/14), done.
Writing objects: 100% (14/14), 2.37 KiB | 1.18 MiB/s, done.
Total 14 (delta 5), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (5/5), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting
remote:      https://github.com/Kubanabaraka/git-exercise-1/pull/new/ft/home-page-redesign
remote:
To https://github.com/Kubanabaraka/git-exercise-1.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
branch 'ft/home-page-redesign' set up to track 'origin/ft/home-page-redesign'.

user@Baraka MINGW64 ~/git-exercise-1 (ft/home-page-redesign)
$

```
