
Git Rebase feature(branch) -> main

Steps

 1993  cd /mnt/e
 1994  pwd
 1995  ls -lrt
 1996  cd Git-Command/
 1997  ls -lrt
 1998  git branch
 1999  touch file4 file5
 2000  git status
 2001  git add .
 2002  git commit -m 'change1'
 2003  git log
 2004  git status
 2005  touch file6 file7
 2006  ls
 2007  ll
 2008  ls -lrt
 2009  git add .
 2010  git commit -m 'change2'
 2011  git checkout main
 2012  git branch
 2013  git status
 2014  ll
 2015  touch varghese
 2016  touch tiju
 2017  ll
 2018  git add .
 2019  git commit -m 'main1'
 2020  touch serah evan
 2021  ll
 2022  git add .
 2023  git commit -m 'main2'
 2024  git rebase feature main
 2025  git branch
 2026  ll
 2027  history
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ ll
total 328
drwxrwxrwx 1 varghese varghese   4096 Feb 24 12:08  ./
drwxrwxrwx 1 varghese varghese   4096 Feb 22 19:28  ../
drwxrwxrwx 1 varghese varghese   4096 Feb 24 12:08  .git/
-rwxrwxrwx 1 varghese varghese 320041 Aug 23  2025 'Git Basic Command Document.docx'*
-rwxrwxrwx 1 varghese varghese  10986 Feb 21 18:38  README.md*
drwxrwxrwx 1 varghese varghese   4096 Feb 22 20:31  branchdemo/
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:08  evan*
-rwxrwxrwx 1 varghese varghese     15 Feb 22 18:13  file1*
-rwxrwxrwx 1 varghese varghese      7 Feb 22 18:13  file2*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:08  file4*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:08  file5*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:08  file6*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:08  file7*
drwxrwxrwx 1 varghese varghese   4096 Feb 24 12:08  image/
-rwxrwxrwx 1 varghese varghese      0 Aug 23  2025  sampleFile.txt.txt*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:08  serah*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:08  tiju*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:08  varghese*
-rwxrwxrwx 1 varghese varghese      0 Aug 23  2025  varghese.py*
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git log # Sequences of commit below change1 & change now available in main branch called rebase


commit cb6fa90063b29b63c097384e72719c6047596c93 (feature)
Author: Varghese Baby <vbpoulose@gmail.com>
Date:   Tue Feb 24 12:03:33 2026 -0500

    change2

commit 538c344771c95a9f20c391936c28d0d08285b16d
Author: Varghese Baby <vbpoulose@gmail.com>
Date:   Tue Feb 24 12:01:04 2026 -0500

    change1
	
	
	
	---------------------------------------------------------------------------
	git Cherry-pick commit id
	
	
	commit 3a9ddcdd7cd29d5eae465e700f01b87ad80aaf5b
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git checkout feature
Switched to branch 'feature'
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git branch
  develop
* feature
  main
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ touch pick1
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git add .
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git commit -m 'pick1'
[feature 38e20b5] pick1
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 image/Git CheeryPick only specific commit.PNG
 create mode 100644 pick1
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$  touch pick2
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git add .
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git commit -m 'pick2'
[feature 9754410] pick2
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 pick2
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ touch pick3
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git add .
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git commit -m 'pick3'
[feature 7b30f62] pick3
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 pick3
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git log
commit 7b30f626c738b2bed65b90cafaf4339092ac7a28 (HEAD -> feature)
Author: Varghese Baby <vbpoulose@gmail.com>
Date:   Tue Feb 24 12:20:06 2026 -0500

    pick3

commit 975441090a1e010d0b6049c93feeee556e1fc555
Author: Varghese Baby <vbpoulose@gmail.com>
Date:   Tue Feb 24 12:19:33 2026 -0500

    pick2

commit 38e20b5219a8f0b0461c69a9f473b015ac3d5ab1
Author: Varghese Baby <vbpoulose@gmail.com>
Date:   Tue Feb 24 12:19:03 2026 -0500

    pick1

commit cb6fa90063b29b63c097384e72719c6047596c93
Author: Varghese Baby <vbpoulose@gmail.com>
Date:   Tue Feb 24 12:03:33 2026 -0500

    change2

commit 538c344771c95a9f20c391936c28d0d08285b16d
Author: Varghese Baby <vbpoulose@gmail.com>
Date:   Tue Feb 24 12:01:04 2026 -0500

    change1

commit d0a1b77f464e55322356d242075d7b5ad27d9d63 (origin/main, origin/HEAD)
Author: Varghese Baby <vbpoulose@gmail.com>
Date:   Sun Feb 22 18:15:44 2026 -0500

    new files added

commit 5c25f2d9d21c3fa48621fe9ca79afd9fdbaf2640
Author: Varghese Baby <Vbpoulose@gmail.com>
Date:   Sat Feb 21 18:39:56 2026 -0500

    Git: Essentials

commit cb594ed371bc6e764c021a62a625ce804808fcf9
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 4 commits.
  (use "git push" to publish your local commits)
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git branch
  develop
  feature
* main
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ ll -lrt
total 328
-rwxrwxrwx 1 varghese varghese      0 Aug 23  2025  varghese.py*
-rwxrwxrwx 1 varghese varghese      0 Aug 23  2025  sampleFile.txt.txt*
-rwxrwxrwx 1 varghese varghese 320041 Aug 23  2025 'Git Basic Command Document.docx'*
-rwxrwxrwx 1 varghese varghese  10986 Feb 21 18:38  README.md*
-rwxrwxrwx 1 varghese varghese     15 Feb 22 18:13  file1*
-rwxrwxrwx 1 varghese varghese      7 Feb 22 18:13  file2*
drwxrwxrwx 1 varghese varghese   4096 Feb 22 19:28  ../
drwxrwxrwx 1 varghese varghese   4096 Feb 22 20:31  branchdemo/
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:08  file4*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:08  file5*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:08  file6*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:08  file7*
drwxrwxrwx 1 varghese varghese   4096 Feb 24 12:21  image/
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:21  evan*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:21  serah*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:21  tiju*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:21  varghese*
drwxrwxrwx 1 varghese varghese   4096 Feb 24 12:21  ./
drwxrwxrwx 1 varghese varghese   4096 Feb 24 12:21  .git/
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git log
commit 9f56e306f10775fe76377f4824c6ab646c221ed6 (HEAD -> main)
Author: Varghese Baby <vbpoulose@gmail.com>
Date:   Tue Feb 24 12:07:04 2026 -0500

    main2

commit 5427255f4c255216d23889b295463e0c85e105c7
Author: Varghese Baby <vbpoulose@gmail.com>
Date:   Tue Feb 24 12:06:04 2026 -0500

    main1

commit cb6fa90063b29b63c097384e72719c6047596c93
Author: Varghese Baby <vbpoulose@gmail.com>
Date:   Tue Feb 24 12:03:33 2026 -0500

    change2

commit 538c344771c95a9f20c391936c28d0d08285b16d
Author: Varghese Baby <vbpoulose@gmail.com>
Date:   Tue Feb 24 12:01:04 2026 -0500

    change1

commit d0a1b77f464e55322356d242075d7b5ad27d9d63 (origin/main, origin/HEAD)
Author: Varghese Baby <vbpoulose@gmail.com>
Date:   Sun Feb 22 18:15:44 2026 -0500

    new files added

commit 5c25f2d9d21c3fa48621fe9ca79afd9fdbaf2640
Author: Varghese Baby <Vbpoulose@gmail.com>
Date:   Sat Feb 21 18:39:56 2026 -0500

    Git: Essentials

commit cb594ed371bc6e764c021a62a625ce804808fcf9
Author: Varghese Baby <Vbpoulose@gmail.com>
Date:   Fri Feb 20 13:32:38 2026 -0500

    Git:README.MD

commit 3a9ddcdd7cd29d5eae465e700f01b87ad80aaf5b
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git cherry-pick 975441090a1e010d0b6049c93feeee556e1fc555
[main 1bd385f] pick2
 Date: Tue Feb 24 12:19:33 2026 -0500
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 pick2
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ ll
total 328
drwxrwxrwx 1 varghese varghese   4096 Feb 24 12:23  ./
drwxrwxrwx 1 varghese varghese   4096 Feb 22 19:28  ../
drwxrwxrwx 1 varghese varghese   4096 Feb 24 12:23  .git/
-rwxrwxrwx 1 varghese varghese 320041 Aug 23  2025 'Git Basic Command Document.docx'*
-rwxrwxrwx 1 varghese varghese  10986 Feb 21 18:38  README.md*
drwxrwxrwx 1 varghese varghese   4096 Feb 22 20:31  branchdemo/
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:21  evan*
-rwxrwxrwx 1 varghese varghese     15 Feb 22 18:13  file1*
-rwxrwxrwx 1 varghese varghese      7 Feb 22 18:13  file2*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:08  file4*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:08  file5*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:08  file6*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:08  file7*
drwxrwxrwx 1 varghese varghese   4096 Feb 24 12:21  image/
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:23  pick2*                   -----> only pick2 in main brach it called cherry-pick
-rwxrwxrwx 1 varghese varghese      0 Aug 23  2025  sampleFile.txt.txt*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:21  serah*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:21  tiju*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:21  varghese*
-rwxrwxrwx 1 varghese varghese      0 Aug 23  2025  varghese.py*
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$



-----------------------------------------------------------------------


Git Stash : BackGround i can hide the file , in Memory
Git stash pop : BackGround i hided in order to work other file later i will bring back and work the file which hide 
Git stash list : can view all hideden file

varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ touch one two
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git status
On branch main
Your branch is ahead of 'origin/main' by 5 commits.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        one
        two

nothing added to commit but untracked files present (use "git add" to track)
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git stash
No local changes to save
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git add .
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git status
On branch main
Your branch is ahead of 'origin/main' by 5 commits.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   one
        new file:   two

varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git stash
Saved working directory and index state WIP on main: 1bd385f pick2
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git status
On branch main
Your branch is ahead of 'origin/main' by 5 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ touch tamil
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git status
On branch main
Your branch is ahead of 'origin/main' by 5 commits.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        tamil

nothing added to commit but untracked files present (use "git add" to track)
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git add .
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git commit -m 'tamil file added'
[main 42ff63b] tamil file added
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 tamil
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git status
On branch main
Your branch is ahead of 'origin/main' by 6 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git stash list
stash@{0}: WIP on main: 1bd385f pick2
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ touch world
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git add .
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git stash
Saved working directory and index state WIP on main: 42ff63b tamil file added
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git stash list
stash@{0}: WIP on main: 42ff63b tamil file added
stash@{1}: WIP on main: 1bd385f pick2
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git stash pop
On branch main
Your branch is ahead of 'origin/main' by 6 commits.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   world

Dropped refs/stash@{0} (9826169c472de73297d5180bc0082636078ef601)
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git status
On branch main
Your branch is ahead of 'origin/main' by 6 commits.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   world

varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git commit -m 'world updated'
[main 5b535d6] world updated
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 world
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git status
On branch main
Your branch is ahead of 'origin/main' by 7 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git stash list
stash@{0}: WIP on main: 1bd385f pick2
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ git stash pop 0
On branch main
Your branch is ahead of 'origin/main' by 7 commits.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   one
        new file:   two

Dropped refs/stash@{0} (3cf28ea17ef1ff03d5323d08f2a22270a66249b1)
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$ ll
total 328
drwxrwxrwx 1 varghese varghese   4096 Feb 24 12:40  ./
drwxrwxrwx 1 varghese varghese   4096 Feb 22 19:28  ../
drwxrwxrwx 1 varghese varghese   4096 Feb 24 12:40  .git/
-rwxrwxrwx 1 varghese varghese 320041 Aug 23  2025 'Git Basic Command Document.docx'*
-rwxrwxrwx 1 varghese varghese  10986 Feb 21 18:38  README.md*
drwxrwxrwx 1 varghese varghese   4096 Feb 22 20:31  branchdemo/
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:21  evan*
-rwxrwxrwx 1 varghese varghese     15 Feb 22 18:13  file1*
-rwxrwxrwx 1 varghese varghese      7 Feb 22 18:13  file2*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:08  file4*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:08  file5*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:08  file6*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:08  file7*
drwxrwxrwx 1 varghese varghese   4096 Feb 24 12:21  image/
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:40  one*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:23  pick2*
-rwxrwxrwx 1 varghese varghese      0 Aug 23  2025  sampleFile.txt.txt*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:21  serah*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:31  tamil*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:21  tiju*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:40  two*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:21  varghese*
-rwxrwxrwx 1 varghese varghese      0 Aug 23  2025  varghese.py*
-rwxrwxrwx 1 varghese varghese      0 Feb 24 12:36  world*
varghese@DESKTOP-OODIU93:/mnt/e/Git-Command$












# LIST of VCS Tools
- Git
- SVN
- ClearCase
- Mercurial
- TFS
- Helix Core (Perforce)

# Git Features
- Works on distributed system (Example it store a copy in local & Remote)



# git reset HEAD -> Mastr [Position] I can change or switch the any file position  

commit 9469d80c1d2cc09909431432055ec26d7b6d1604 [Positon of Head ]
Author: Varghese Baby <vbpoulose@gmail.com>
Date:   Sat Feb 21 18:19:48 2026 -0500

    Revert "file added with second line" - Deleting this Commit by Varghese

    This reverts commit cbb503fc3dcbc655fca671e7b9d55cbceac16aee.

commit 7d7b73d99dd3bfe0f7e31a4d7d2e7765238fc2b3
Author: Varghese Baby <vbpoulose@gmail.com>
Date:   Thu Feb 19 11:53:36 2026 -0500

    file3 and file4 added

commit cbb503fc3dcbc655fca671e7b9d55cbceac16aee
Author: Varghese Baby <vbpoulose@gmail.com>
Date:   Thu Feb 19 11:51:12 2026 -0500

    file added with second line



- 
| Category                        | Commands Used                                                                                          | Purpose / What You Practiced                                         |
| ------------------------------- | ------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------- |
| **Git – Basic Workflow**        | `git status`<br>`git add .`<br>`git commit -m`<br>`git push`<br>`git pull`<br>`git pull --rebase`      | Standard Git workflow: staging, committing, pushing, syncing changes |
| **Git – Remote Setup**          | `git remote -v`<br>`git remote add origin`<br>`git remote set-url origin`<br>`git push -u origin main` | Managing remote repositories                                         |
| **Git – Initialization**        | `git init`                                                                                             | Initializing repositories multiple times in different folders        |
| **Git – Logs & History**        | `git log`<br>`git log --oneline`<br>`history`                                                          | Viewing commit and command history                                   |
| **Git – File Tracking Control** | `git rm --cached`<br>`git restore`<br>`git reset`                                                      | Undoing staged files & resetting commits                             |
| **Directory Navigation**        | `cd`<br>`cd ..`<br>`cd -`<br>`cd ~`<br>`pwd`<br>`pwd -L`<br>`pwd -P`                                   | Navigation between directories                                       |
| **Listing Files**               | `ls`<br>`ll`<br>`ls -l`<br>`ls -lrt`                                                                   | Viewing files in various formats                                     |
| **File Creation**               | `touch`<br>`touch -a`<br>`touch -m`<br>`touch -t`                                                      | Creating files & modifying timestamps                                |
| **File Viewing**                | `cat`<br>`cat -n`<br>`cat -b`<br>`cat -s`<br>`cat -v`                                                  | Viewing file contents in different formats                           |
| **Text Writing & Redirection**  | `echo "text" > file`<br>`echo "text" >> file`                                                          | Overwrite (`>`) and Append (`>>`)                                    |
| **File Editing**                | `vim`<br>`vi`<br>`nano`                                                                                | Editing files                                                        |
| **File Move / Rename**          | `mv`<br>`mv -i`                                                                                        | Moving and renaming files                                            |
| **File Copy**                   | `cp`<br>`cp -rf`<br>`cp -a`                                                                            | Copying files and directories                                        |
| **File Remove**                 | `rm`<br>`rm -i`<br>`rm -f`<br>`rm -r`<br>`rm -rf`                                                      | Deleting files and folders                                           |
| **Search & Filtering**          | `grep`<br>`grep -i`<br>`ls -l \| grep`                                                                 | Searching text and filtering output                                  |
| **Pipes Usage**                 | `cat file \| grep`                                                                                     | Using pipe operator                                                  |
| **Script Execution**            | `bash hello.sh`<br>`./hello.sh`<br>`./voter.sh`                                                        | Running Bash scripts                                                 |
| **Script Rename**               | `mv hello.sh voter.sh`                                                                                 | Renaming scripts                                                     |
| **System Update / Packages**    | `sudo apt update`<br>`sudo apt upgrade`<br>`sudo apt install`                                          | Installing and updating packages                                     |
| **SSH Setup**                   | `ssh`<br>`sudo apt install openssh-server`<br>`systemctl start ssh`                                    | SSH server setup and testing                                         |
| **Process Monitoring**          | `top`                                                                                                  | Viewing running processes                                            |
| **Environment Variables**       | `echo "export DISPLAY=:0" >> ~/.bashrc`<br>`source ~/.bashrc`                                          | Updating shell configuration                                         |
| **Hostname & User Info**        | `hostname`<br>`whoami`<br>`id`<br>`who`                                                                | System identity commands                                             |
| **Git Demo Practice**           | Creating demo repo<br>`git restore`<br>`git reset <commit-id>`                                         | Git lifecycle testing & version rollback                             |
| **Directory Backup Practice**   | `cp -rf folder folder_old`                                                                             | Manual folder backup simulation                                      |






Git Pull, Merge, and Rebase — Simple Explanation
What git pull Actually Does

git pull is two commands combined:

git fetch
git merge

1️⃣ git fetch

Downloads new commits from the remote repository (GitHub)

Does NOT change your working files

2️⃣ git merge

Combines remote changes with your local branch

This merge step is what triggered Vim

Why Git Asked for a Commit Message

A merge creates a new commit

Git needs a reason for combining two histories:

“Why are these two histories being merged?”

So Git:

Creates a merge commit

Opens an editor (Vim by default)

Asks you to confirm the commit message

✅ This is normal Git behavior, not an error.

Merge vs Rebase (Important Difference)
🔀 git pull (Default = Merge)

Combines histories using a merge commit

Every merge commit requires a message

Git opens an editor (Vim)

A──B──M ← merge commit (needs message)
\ /
C───

🔁 git pull --rebase

No merge commit is created

Your local commits are replayed on top of remote commits

Therefore → no merge commit message

A──C──B' ← B replayed on top of C

Benefits of Rebase

Clean, linear commit history

✔️ No “Merge branch …” commit

✔️ Usually no editor popup

Recommended Setting (Avoid Vim Surprise)

Set rebase as default:

git config --global pull.rebase true

Now git pull behaves like:

git pull --rebase

One-Page Git Cheat Sheet 🧠
git pull # Fetch + merge (may open editor)
git pull --rebase # Fetch + rebase (no merge commit)
git status # Check current state
git merge --abort # Cancel an unfinished merge
git rebase --continue # Continue after fixing conflicts

Memory Rule (Very Important)

Merge = new commit = needs message
Rebase = replay commits = no new merge commit

<br>**Error like Index LOCK-> fatal: Unable to create 'C:/Users/u/Desktop/VsCodeJava/.git/index.lock': File exists. use below code in : VS code Editor / CMD Promt
cd .git
del index.lock**<br>
-----------------------------------<br>

** Short status flags are**:

- ?? - Untracked files
- A - Files added to stage
- M - Modified files
- D - Deleted files <br>

**Git Hub Command**<br>
Here i have created git repo called SoftwareTesting to check the git command 'Branch''Checkout'<br>

- Step 1 : git init
- Step 2 : git add . // varghese.py / test.py in this files are empty
- Step 3 : git commit -m 'Test Commit'
- Step 4 : git branch -M main
- Step 5 : git remote add origin https://github.com/varghese25/SoftwareTesting.git
- Step 6 : git push -u origin main<br>

**Local Folder named TestingFile inside two files varghese.py (empty without Any Code) / test.txt(empty without Any Code) -> and pushed to github main branch**<br>

**New Branch Creation github called 'myworkings'**<br>

- Step 1 : git checkout -b 'myworkings'
- Step 2 : git add varghese.py // add few line of code in the varghese.py in the 'myworkings' branch.
- Step 3 : git commit -m 'varghese py' // commit message
- Step 4 : git push -u origin myworkings // pushed file in this branch<br>

**Branch switch is possible through**<br>

- git checkout master -> currently in master
- git checkout myworkinfs -> currently in myworkings
- git brach // it will show all branch _main / myworkings _ means current branch<br>

> [!IMPORTANT] : Main branch varghese.py without any code. myworkings branch varghese.py withcode when you switch between branch the files as to reload.
> example : main branch varghese.py to myworkings branch it says to reoad.<br>
> Refer: SoftwareTesting Repo for further clarity..

**How To Delete Branch**

Check out from the branch which we would like like. in this example i would like to delete Java Brach<br>

- Step 1 PS E:\myWorks\VsCodeJava> git checkout master
  Switched to branch 'master'
  Your branch is up to date with 'origin/master'.
- Step 2 PS E:\myWorks\VsCodeJava> git branch -d Java
  warning: deleting branch 'Java' that has been merged to
  'refs/remotes/origin/Java', but not yet merged to HEAD.
  Deleted branch Java (was eb954ee).
- Step 3 PS E:\myWorks\VsCodeJava> git push origin -d Java
  To https://github.com/varghese25/VScodeJava.git

* [deleted] Java
