<br>**Error like Index LOCK-> fatal: Unable to create 'C:/Users/u/Desktop/VsCodeJava/.git/index.lock': File exists. use below code in : VS code Editor / CMD Promt
cd .git
del index.lock**<br>
---------------------------------------------------------------------------------------------------------------------------------------------------------------------<br>

**Git Hub Command**<br>
Here i have created git repo called SoftwareTesting to check the git command 'Branch''Checkout'<br>
* Step 1 : git init
* Step 2 : git add . // varghese.py / test.py in this files are empty
* Step 3 : git commit 'Test Commit'
* Step 4 : git branch -M main
* Step 5 : git remote add origin https://github.com/varghese25/SoftwareTesting.git
* Step 6 : git push -u origin main<br>

**Local Folder named TestingFile inside two files varghese.py (empty without Any Code) / test.txt(empty without Any Code) -> and pushed to github main branch**<br>

**New Branch Creation github called 'myworkings'**<br>
* Step 1 : git checkout -b 'myworkings'
* Step 2 : git add varghese.py // add few line of code in the varghese.py in the 'myworkings' branch.
* Step 3 : git commit -m 'varghese py' // commit message
* Step 4 : git push  -u origin myworkings // pushed file in this branch<br>

**Branch switch is possible through**<br>

* git checkout master -> currently in master
* git checkout myworkinfs -> currently in myworkings 
* git brach // it will show all branch    *main / myworkings * means current branch<br>


> [!IMPORTANT]  : Main branch varghese.py without any code. myworkings branch varghese.py withcode when you switch between branch the files as to reload. 
 example : main branch varghese.py to myworkings branch it says to reoad.<br>
