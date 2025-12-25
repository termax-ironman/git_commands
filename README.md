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




