go to perspective then click git

while workin on eclipse if you want to use git through eclipse itself
how you can do it

firstly you can not access, push, pull and do anythin of your it repository 
throuh your normal git user name and password you need to 
generate token for that and then need to put the generated token as a password to 
enter to your it repo or do any kind of remote operation.

so goto github --> settin --> developer options --> 
generate classis token --> then how much time you want this token to be 
active--> please select the days -> then add permissions -->
then generate token

then you will make a git repository in the github

then you come to eclipse and then you click on git clone repository

add .git link
then save one repo in TL Workspace
now you as a TL have just set up the local repo in your eclipse
now you need to push initial project files with directory into github
so that other developer can take a clone of that and start workin on that
so you select one already existing project on your project explorer then share to team
and put it in your eclipse local repo just to add to staging and then commit and push.

now in git stagging
click on ++ to add it in staging area
then add commit messege and commit and push to the remote repo 
while pushing they might ask for username password please enter your user email and 
git classic token id as a password.

please save git token in your notepad for convenience.
