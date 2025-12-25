# git_commands

### git init
It creates a .git directory (not a file) which stores all Git metadata (history, branches, config).
### git add .
it adds all the files from working directory to staged directory
### git commit -m "Commit Messege"
it adds staged files to local repository
### git branch -m main
Renames the current branch to main.
### git remote add origin ".git html link"
Adds a remote repository URL named origin that points to the GitHub repo.
### git push -u origin main
Pushes commits from the local main branch to the remote origin repository and sets upstream tracking.
### git config --global user.name "termax-ironman"
### git config --global user.email "youremail@gmail.com"
These commands define author information for commits.
GitHub uses this email to associate commits with your GitHub account.
### creating multiple files on git bash 
touch test1.java<br>
touch test2.java<br>
touch test3.java<br>

git add test1.java (add 1 file to staged status)

now you thought you don't want to commit and want it back 
to working unstaged directory rather than keeping it in staged<br>
then you need to use this command to back it in unstaged directory(working directory)

git restore --staged  test1.java

now how to check it moved or not?

git status

all 3 files will be red(unstaged) status

if you want to include all 3 files to staged then 

git add .

now you want them back to unstaged rather than commit and push <br>

git restore --staged .

## Kand Ho Gaya? Ed-1 

your local repo currently in sync with central repo<br>
you changed test1.java file mistakenly<br>
now you want to undo the unintended changes from git bash to make it again sync with central repo<br>
how you can do it?

git restore test1.java

### there is another dev(Dev2) in your org who wants central repo code in his/her system?

git clone ".git link"

### Dev2 do changes in test1.java, test2.java and test3.java file then push it to central repo how you will take that code from central repo?

git pull

### How to check each commmits in central repository?

git log

### how to check each commits on any particular file?

git log test1.java

### how to check each commits on all files in single line? (Fancy Command)

git log --oneline

first 7 digits of commit log are only fetched in this case

### how to check each commits on any particular file in single line? (Fancy Command)

git log --oneline test1.java

### How to create and Resolve conflicts?

you have Test1.java file inside that you(dev1) wrote <br>
public class Test { <br>
public static void main(String[] args) { <br>
System.out.println("Heelo from Dev1"); <br>
}<br>

then you did
git add test1.java
git commit -m "dev1 test1.java updation"
git push

now another new team member comes and cloned that repo<br>
then change the test1.java file content to 

public class Test { <br>
public static void main(String[] args) { <br>
System.out.println("Hello from Dev2"); <br>
}<br>

now he add, commit and push that code to cloud
then dev1 joined next day and he opened his local 
test1.java without git pull and added few lines of code in test1.java
now he did these commands<br>
git add test1.java<br>
git commit -m "dev2 change"<br>
git push

now dev2 will get error as REJECTED.....
due to mere conflicts..
now opens the test1.java file and check for log id 
and then he search that lo id assocaiated developer with 

git log test1.java

then dev2 will call dev1 and discussed and come into conclusion about 
how much code need to stay and how much need to be discarded

then dev2 will do add,commit and push of that mutually discussed code

That's how mere conflict will get resolved in real time





