GIT THROUGH ECLIPSE (WITH IMPORT PROJECT FLOW)
Using Git directly from Eclipse (EGit)

If you want to use Git through Eclipse itself, you should use the Git Perspective.

Step 1: Open Git Perspective

Go to Window → Perspective → Open Perspective → Git

Step 2: GitHub Authentication (Mandatory)

GitHub no longer allows Git operations using username and password.

So, you must generate a GitHub Personal Access Token (Classic) and use it as your password.

Steps to generate token:

Go to GitHub → Settings

Open Developer settings

Select Personal access tokens → Tokens (classic)

Click Generate new token (classic)

Choose:

Token expiration time

Required permissions (repo access)

Generate and copy the token

Save the token securely (you won’t be able to view it again)

👉 This token will be used as the Git password in Eclipse.

Step 3: Create Repository on GitHub

Create a new repository on GitHub

Copy the .git repository URL

Step 4: Clone Repository in Eclipse

Switch to Git Perspective

Click Clone a Git repository

Paste the .git URL

Enter:

Username: GitHub username or email

Password: Generated classic token

Choose a local directory (workspace or any folder)

Finish cloning

At this point:

The repository is cloned

Files exist locally

But the project may not yet appear in Project Explorer

Step 5: Import Project into Eclipse

After cloning, Eclipse may not automatically recognize the project.

When to import:

Project is visible in Git Repositories view

But not visible in Project Explorer

Import steps:

Go to File → Import

Select Existing Projects into Workspace

Choose Select root directory

Browse to the cloned repository folder

Select the project

Click Finish

Now the project will appear in Project Explorer.

Step 6: Push Initial Project Files (Team Lead)

To allow other developers to start working:

Select the project in Project Explorer

Right-click → Team → Share Project

Select the cloned Git repository

Open Git Staging view

Click ++ to move files to the staging area

Enter a commit message

Click Commit and Push

During push:

Username: GitHub username/email

Password: GitHub classic token

Step 7: Instructions for Developers

Developers should:

Clone the repository using the .git URL

Import the project into Eclipse (if not auto-detected)

Use:

Their own GitHub username

Their own generated classic token as password

Start working, then commit and push changes

Correct Workflow Summary
Team Lead
Create project → Share Project → Commit & Push

Developer
Clone repo → Import project → Work → Commit & Push

Key Rule to Remember

Cloning brings the code. Importing tells Eclipse how to open it.

### How to pull from central repo?

Right click on the project
then go to Team → Pull

✔️ This will fetch the latest changes from the remote branch and merge them into your current branch.

### Branching

Yes, you can also create branches and checkout between them in Eclipse itself
through only clicking (no CLI needed).

✔️ You can create, switch, delete branches using Team → Switch To → New Branch / Other Branch.

### Stashing

You add some code then get that code into the stash area
then apply stash

then you do your urgent work

when your urgent work is over
then you apply the stash into your current working tree

📌 Note: Stash just temporarily saves your uncommitted changes; it does not push anything to remote.

### Tag

If you are creating a tag for any commit then you can also do it
using click

📌 Important correction here ⬇️

Whatever commit you tag, that version of code is NOT read-only.

✔️ A tag is just a label/reference to a specific commit
✔️ You cannot change the commit, but you can still create new commits and push code normally
✔️ Tags are mainly used for releases (v1.0, v2.0, etc.)

### CLI COMMAND:

git tag RELEASE1.0 <commitId>

How to get log history of any file?

Click on that file
then you will get Show Revision History / Show History

✔️ This shows all commits related to that specific file.

How to resolve conflict in Eclipse?

Same as we do in CLI
3 lines of conflict markers will be there

<<<<<<< HEAD
(your local code)
=======
(remote code)
>>>>>>> commit-id


✔️ First part → your local code
✔️ Second part → remote code

You will check who has done this commit
then you will call that developer
then after mutual discussion, you resolve the conflict and commit
then push to production.

📌 Eclipse also provides a visual merge editor, which makes this easier.
