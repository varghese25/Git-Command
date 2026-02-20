# LIST of VCS Tools
- Git
- SVN
- ClearCase
- Mercurial
- TFS
- Helix Core (Perforce)

# Git Features
- Works on distributed system (Example it store a copy in local & Remote)

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
