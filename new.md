Welcome to Git (version 1.9.4-preview20140929)


Run 'git help git' to display the help index.
Run 'git help <command>' to display help for specific commands.

lynnaun@LJ_LAPTOP ~
$ cd ~/Desktop/

lynnaun@LJ_LAPTOP ~/Desktop (master)
$ git clone https://github.com/LJanJohnson/test.go.git
Cloning into 'test.go'...
remote: Counting objects: 3, done.
remote: Total 3 (delta 0), reused 0 (delta 0)
Unpacking objects: 100% (3/3), done.
Checking connectivity... done.

lynnaun@LJ_LAPTOP ~/Desktop (master)
$ cd test.go/

lynnaun@LJ_LAPTOP ~/Desktop/test.go (master)
$ ls
README.md

lynnaun@LJ_LAPTOP ~/Desktop/test.go (master)
$ git remote -v
origin  https://github.com/LJanJohnson/test.go.git (fetch)
origin  https://github.com/LJanJohnson/test.go.git (push)

lynnaun@LJ_LAPTOP ~/Desktop/test.go (master)
$ touch new.md

lynnaun@LJ_LAPTOP ~/Desktop/test.go (master)
$ ls
README.md  new.md

lynnaun@LJ_LAPTOP ~/Desktop/test.go (master)
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   README.md

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        new.md

no changes added to commit (use "git add" and/or "git commit -a")

lynnaun@LJ_LAPTOP ~/Desktop/test.go (master)
$ git add .

lynnaun@LJ_LAPTOP ~/Desktop/test.go (master)
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   README.md
        new file:   new.md


lynnaun@LJ_LAPTOP ~/Desktop/test.go (master)
$ git commit -m "edit readme and new.md"

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'lynnaun@LJ_Laptop.(none)')

lynnaun@LJ_LAPTOP ~/Desktop/test.go (master)
$ git config --global user.email "lynnaunjohnson@yahoo.com"

lynnaun@LJ_LAPTOP ~/Desktop/test.go (master)
$ git config --global user.name "LJanJohnson"

lynnaun@LJ_LAPTOP ~/Desktop/test.go (master)
$ git commit -m "edit readme and new.md"
[master 74f50e7] edit readme and new.md
 2 files changed, 5 insertions(+)
 create mode 100644 new.md

lynnaun@LJ_LAPTOP ~/Desktop/test.go (master)
$ git status
On branch master
Your branch is ahead of 'origin/master' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working directory clean

lynnaun@LJ_LAPTOP ~/Desktop/test.go (master)
$ git log
commit 74f50e78992ef65b23cc63b5a397c0044f89f57d
Author: LJanJohnson <lynnaunjohnson@yahoo.com>
Date:   Thu Oct 9 08:00:14 2014 -0500

    edit readme and new.md

commit c12fcea0522984db9dd2514a7e8f6ae616646647
Author: LJanJohnson <LJanJohnson@users.noreply.github.com>
Date:   Thu Oct 9 07:18:49 2014 -0500

    Initial commit

lynnaun@LJ_LAPTOP ~/Desktop/test.go (master)
$ git push origin master
Username for 'https://github.com': LJanJohnson
Password for 'https://LJanJohnson@github.com':
Counting objects: 6, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (4/4), 349 bytes | 0 bytes/s, done.
Total 4 (delta 0), reused 0 (delta 0)
To https://github.com/LJanJohnson/test.go.git
   c12fcea..74f50e7  master -> master

lynnaun@LJ_LAPTOP ~/Desktop/test.go (master)
$