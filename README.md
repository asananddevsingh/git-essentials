# git-essentials

Git commands and Alias

##Git Commands

git config --global user.name
git config --global user.email

———————
Git Aliasing:
———————
$ git config --global alias.co checkout
$ git config --global alias.br branch
$ git config --global alias.ci commit
$ git config --global alias.st status
$ git config --global alias.pl pull
$ git config --global alias.cim "commit -m"
$ git config --global alias.puo "push origin"
$ git config --global alias.plo "pull origin"
$ git config --global alias.plom "pull origin master"
$ git config --global alias.co checkout;
$ git config --global alias.com "checkout master";
$ git config --global alias.rbm “rebase master” 


—————
Rebase:
—————
$ git rebase <target branch> <origin branch> e.g. git rebase master <my-branch>

$ git rebase -i <master> <my-branch> 
=> It will give all the commits, with “pick” before it. Now keep the first commit and replace “pick” with “squash” for others. 
=> Now save the changes with press “Esc” -> :wq! -> Enter.
=> Now exit with “Esc” -> q! -> Enter.
=> Now $ git push origin -f <my-branch>.


—————
Reset:
—————
$ git reset —soft HEAD
$ git reset --hard HEAD
$ git reset --hard <commit id>


—————
New Branch:
—————
git checkout -b <new-branch-name>

—————
Delete Local Branch:
—————
$ git branch -d branch_name
$ git branch -D branch_name

—————
Rename Local Branch:
—————

If you are on the branch you want to rename:
$ git branch -m <new-br-name>

If you are at other branch.
$ git branch -m <old-name> <new-name>

—————
Revert Commit:
—————
$ git revert <commit_hash>

—————
Reset Branch To Particular Commit:
—————
$ git reset --hard <commit id>
$ git push origin -f (pushing forcefully)


—————
Stash
—————
$ git stash list
stash@{0}: WIP on master: 049d078 added the index file
stash@{1}: WIP on master: c264051 Revert "added file_size"
stash@{2}: WIP on master: 21d80a5 added number to log

$ git stash apply --index

—————
Gitlab
—————
f you want to skip CI pipeline for your branch then please follow below commands-
1.	If your commit message contains [ci skip] or [skip ci], using any capitalization, the commit will be created but the pipeline will be skipped 
2.	"git push -o ci.skip"  

