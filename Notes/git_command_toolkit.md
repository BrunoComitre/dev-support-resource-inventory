# GIT Tips & Commands

## Branchs

- The **MASTER:** will contain all the tested, versioned code that will be delivered to the customer and the **DEVELOP** is where all the workflow will occur before making the release version that will be merge into the **MASTER**.

- DEVELOP should always contain the most current code, where the feature branches will be branched based on it.

After you have created develop, where all development will happen, create the respective branch for your implementation, remember to keep a naming pattern for easy understanding as it is suggested in the git flow:

- **feature**: for new implementations

- **release**: for finalizing release and tags

- **hotfix**: for solving critical production problems that cannot wait for a new release

***
&nbsp;

## Git Message Example to use

```
# 50-character subject line
#
# 72-character wrapped longer description. This should answer:
#
# * Why was this change necessary?
# * How does it address the problem?
# * Are there any side effects?
#
# Include a link to the ticket, if any.
```

***
&nbsp;

## Create a New Branch

- Run this command (replacing my-branch-name with whatever name you want):
  - ``` git checkout -b my-branch-name ``` - You're now ready to commit to this branch.

- Switch to a Branch In Your Local Repo
  - ``` git checkout my-branch-name ```

***

## Creating and Using Features

- In this case, since we are already in **develop**:
  - ``` git checkout -b feature/new-component ```

- Once created, you work on your modification locally, if you need someone else to work on this same implementation you must share it to your remote repository:
  - ``` git push origin feature/new-component ```

- Show, implementation done, now it's time to merge this feature with develop, for this, checkout the develop branch, merge the feature and update the remote:
(Get the branch, send the stuff from it to develop but without closing)
  - ``` git checkout develop && git merge feature/new-component && git push origin develop ```

- If there are no conflicts, great, we are ready to release this implementation and submit it to the remote repository, so create the release branch and submit:
  - ``` git checkout -b release/v1.0.1 && git push origin release/v1.0.1 ```

- After the last tests are done, you can now tag the version:
**``` **git tag -a v1.0.1 -m "Release of new component" ```

- Remembering, that if a bug was identified during the process, you must treat this bug in the release branch, send to the master and to develop as well, making the develop always contain the corrections.

- When inserting a tag, I like to use annotated tags, because it records information about who made the tag, date, hash, if you don't want this information, simplify:
  - ``` git tag v1.0.1 ```

- Now let's check that the tag was created and upload it to the remote repository:
  - ``` git show v1.0.1 && git push origin v1.0.1 ```

- If all went well, your tag will be created and we are able to merge this small release into the master:
  - ``` git checkout master && git merge release/v1.0.1 ```

***

## Git Basics

- To create empty git repo in the specified directory
  - ``` git init ```

- To clone repo on your local machine
  - ``` git clone <repo--HTTP or SSH> ```

- To set author namea to be used for all commits to the current repo
  - ``` git config user.name <name> ```

- To stage all changes to <directory> or <file> for the next commit
  - ``` git add <directory or file> ``` you can also use ``` git add . ```

- To commit a staged snapshot with a commit message
  - ``` git commit -m "<message>" ```

- To display the entire commit history
  - ``` git log ```

- To show untested changes to your index and working directory or to analyze the current state of the repo
  - ``` git diff ```

***

## Merge a Branch

- For the List which files are tested, untested and untracked:
  - ``` git status ``` - You'll want to make sure your working tree is clean and see what branch you're on
  
-  First, you must check out the branch that you want to merge another branch into (changes will be merged into this branch). If you're not already on the desired branch:
  - ```  git checkout master ```
  - NOTE: Replace master with another branch name as needed

- Now you can merge another branch into the current branch:
  - ```  git merge my-branch-name ```
  - NOTE: When you merge, there may be a conflict. Refer to Handling Merge Conflicts (the next exercise) to learn what to do

***

## Delete Branches

- To delete a remote branch:
  - ```  git push origin --delete my-branch-name ```

- To delete a local branch, run either of these commands:
  - ```  git branch -d my-branch-name ```
  - ```  git branch -D my-branch-name ```
  - NOTE: The -d option only deletes the branch if it has already been merged. The -D option is a shortcut for --delete --force, which deletes the branch irrespective of its merged status.

***

## Git Branch

- List all the branches in your repo. Add an argument to create a new branch
  - ``` git branch ```

- Create and checkout a new branch called
  - ``` git checkout -b <branch> ``` - ``` -b ``` flag is to checkout an existing branch

- Merge into the current branch
  - ``` git merge <branch> ```

- To see remote branches, run this command:
  - ``` git branch -r ```

- To see all local and remote branches, run this command:
  - ``` git branch -a ```

***

## Remote Repositories

- Make sure the branch develop exists in your remote repository by listing your local and remote branches:
  - ``` git branch -a ```

- Create a new connection to the remote repo.
  - ``` git remote add <name> <url> ``` - After doing this, you can use <name>as a shortcut to <url>other commands.

- If not, sync your remote repository, checkout creating your branch develop and send to your remote repository:
  - ``` git fetch origin && git checkout -b develop && git push origin develop ```

- Fetch a specific one in the repo. Stop <branch>to fetch all remote references
  - ``` git fetch <remote> <branch> ```

- Get the copy of the specified remote from the current branch and immediately merge it into the local copy.
  - ``` git pull <remote> ```

- Push the branch to, along with the necessary commit objects. Creates a named branch in the remote repository if it does not exist
  - ``` git push <remote> <branch> ```

***

## Git Rebase

- Rebase the current branch interactively in the <base>editor .Launches to enter commands for how each commit will be transferred to the new base
  - ``` git rebase -i <base> ```

***

## Git Pull

- Get the remote copy of the current branch and relocate it to the local copy. Use git rebase instead of merge to integrate the branches
  - ``` git pull --rebase <remote> ```
 
### Switch to a Branch That Came From a Remote Repo

To get a list of all branches from the remote:
  - ``` git pull```

- To switch to the branch:
  - ``` git checkout --track origin/my-branch-name```

***

## Git Push

- To link a local branch with the remote branch. The -u flag is used to define the source as the remote upstream in your git configuration
  - ``` git push -u <remote> <branch> ```

- It forces git push even if it results in a merge with no fast forward. Do not use the --force flag or the -f unless you are absolutely sure you know what you are doing
  - ``` git push <remote> --force ```
  - ``` git push -f <remote> <branch> ```

### Push to a Branch

- If your local branch does not exist on the remote, run either of these commands:
  - ``` git push -u origin my-branch-name ```
  - ``` git push -u origin HEAD ```

NOTE: HEAD is a reference to the top of the current branch, so it's an easy way to push to a branch of the same name on the remote. This saves you from having to type out the exact name of the branch!

- If your local branch already exists on the remote:
  - ``` git push ```

***

## Undoing Changes

- Create a new commit that undoes all the changes made in the current branch (master will do). here we need a commit reference ID
  - ``` git revert <commitId> ``` - Or git revert Headto create a new commit with the reverted changes that were made in the last commit

- To remove the file from the testing area, but leave the working directory unchanged. This removes the stage of a file without overwriting any changes
  - ``` git reset <file> ```

- Good for separate branch
  - ``` git reset ```

- Conflicting command
  - ``` git reset -- hard origin/'branch-name' ```

- Used to remove unwanted files from your working directory. -n flag is used for double-checking before changing, to run use -f instead of-n
  - ``` git clean -n ```

***

## Rewriting History

- Replace the last commit with the change in stage and the last commit combined
  - ``` git commit --amend ```

- Perform the rebase of the current branch on. <base>may be a commit ID, branch name, a tag, or a reference relative to HEAD.
  - ``` git rebase <base> ```

- Show a log of changes to HEAD in the local repository. Add --relative-date flag to show date and time information or --allpar to show all references.
  - ``` git reflog ```

***

## Miscellaneous commands

- Merge branch with develop
  - ``` git merge develop ```

- To delete the branch locally
  - ``` `git branch -D <name of branch> ```

- To delete the branch remotely
  - ``` git push <origin name> <branch name> --delete ```

- To remove unused and closed branches:
  - ``` git fetch -p ```

- To perform Unpush (Remove sync before git pull command)
  - ``` git reset --soft HEAD~1 ```

***
&nbsp;

## Links

- [How to Write a Git Commit Message](https://chris.beams.io/posts/git-commit/)
- [8.1 Customizing Git - Git Configuration](https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration)
- [Learn Git](https://www.nobledesktop.com/learn/git)
- [Git Branches: List, Create, Switch to, Merge, Push, & Delete](https://www.nobledesktop.com/learn/git/git-branches)

***
