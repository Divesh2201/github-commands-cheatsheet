# github-commands-cheatsheet
1. To link your github to local git : `git remote add origin "<URL>"`

2. To create an empty .git folder : `git init`

3. To pull all files from central github to git : `git pull origin master`

#### Easy Push To Origin
4. `git add --all` or `git add .` - adds everything to the stageing area

 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; (If a file is in the index once, after modifications you can just give the commit command, it does the modification(add)and commits it as well)


5. `git status` - everything should turn green

6. `git commit -m "//comment"` - commit with comment

7. `git push origin master` - pushes the code to the remote repo

8. If u want to view the history : `git log`

#### Branching

9. To create a new branch : `git branch <name>`

10. To switch to that(or any other)branch from current branch : `git checkout <name>`

11. To view as to which branch we are currently : `git branch`

 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;U can store files specific to any branch(may not be the master branch) and it wont appear in the master branch(or other branches), 
 
 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Any new branch created will have the files of master branch.

#### Merging (always remember be in the branch where u want to merge(destination branch))

12. To merge content from <name> branch : `git merge firstbranch`
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;This merges the firstbranch branch to the current branch.

#### Rabasing (Its sim to merging but assigns a linear connect between master and othr branch)

13. Rebase (exact same parameters) : `git rebase firstbranch`

#### Push files to GitHub

14.Push files through any branch on github : `git push --all  (pushes all branches to cent repo)` or
`git push origin firstbranch`

#### Download a specific folder from any github repo
Copy the url and change `/tree/<branch-name>` to `/trunk`
 
15. And Then : `svn checkout <url>`

#### Squash commits, even after they being pushed
16. `git rebase -i origin/master~<number_of_commits> master`

17. `git push origin +master` (master can be any branch)

#### Squash commits before push
18. `git rebase -i origin/master`

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Use `git rebase --continue` if rebase is stuck to cleanup and complete the rebase.
#### revert commit
19. `git revert <commit_hash>`
20. `git commit --amend // to complete`
#### Delete the most recent commit, keeping the work you've done:
21. `git reset --soft HEAD~1`
#### Delete the most recent commit, destroying the work you've done:
22. `git reset --hard HEAD~1`

#### Forked Repo Updates
23. pull latest code from upstream <branch> to fork default branch : `git pull upstream master` 
24. To specify a new remote upstream repository that will be synced with the fork:<br/>
    `git remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git` 
 
26. To verify the new upstream repository you've specified for your fork: `git remote -v`

26. To commit the pulled changes : `git push origin master`

#### Remove files from a Git repository
27.  Remove files from the working tree and from the index : `git rm "<pathspec>..."` 

28. To remove files stored in central git repo but not from local repo (use case: to add already commited file in .gitignore) : 
    
    `git rm -r --cached`

29. If you wish to try what it does beforehand, add the -n to test things out : `git rm -r -n --cached`


#### This Repo is open for all, if you wish to contribute something not present
i) Fork the Repo

ii) Make necessary updates (pull upstream to keep fork upto date)

iii) Create a Pull Request

iv) A valid pull request will be merged!
#### Contributions are Welcome  :blue_heart: :smile:
