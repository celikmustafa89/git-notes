source: https://www.git-tower.com/blog/git-cheat-sheet/
? -> never used
+ -> used at least once

##### GIT NOTES #####

#### Local Changes ####
+ 1- changed files in your working directory               : git status
? 2- changes to tracked files                              : git diff
+ 3- add all current changes to the next commit            : git add .
+ 4- add some changes in <file> to the next commit         : git add -p <file>
+ 5- commit all local changes in tracked files             : git commit -a
? 6- commit previously staged changes                      : git commit
? 7- change the last commit(dont amend published commits!) : git commit --amend

#### Branches & Tags ####
+ 1- list all existing branches                            : git branch -av
+ 2- switch HEAD branch                                    : git checkout <branch>
+ 3- create a new branch based on your current HEAD        : git branch <new-branch>
? 4- create a new tracking branch based on a remote branch : git checkout --track <remote/branch>
+ 5- delete a local branch                                 : git branch -d <branch>
? 6- mark the current commit with a tag                    : git tag <tag-name>

### Merge & Rebase ###
+ 1- merge <branch> into your current HEAD                 : git merge <branch>
? 2- rebase your current HEAD onto <branch>                : git rebase <branch>
? 3- abort a rebase                                        : git rebase --abort
? 4- continue a rebase after resolving conflicts           : git rebase --continue
? 5- use your configured merge tool to solve conflicts     : git mergetool
? 6- use your editor to manually solve conflicts and 
    (after resolving) mark file as resolved                : git add <resolved-file>
                                                             git rm <resolved-file>

### Update & Publish ###
+ 1- list all currently configured remotes                 : git remote -v
+ 2- show information about a remote                       : git remote show <remote>
? 3- add new remote repository, named <remote>             : git remote add <shortname> <url>
? 4- download all changes from <remote>, 
     but dont integrate into HEAD                          : git fetch <remote>
? 5- download changes and merge/integrate into HEAD        : git pull <remote> <branch>
+ 6- publish local changes on a remote                     : git push <remote> <branch>
+ 7- delete a branch on the remote                         : git branch -dr <remote/branch>
? 8- publish your tags                                     : git push --tags
