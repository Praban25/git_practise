║           🔧 Common Git Commands                     ║
╠══════════════════════════════════════════════════════╣
║  SETUP                                               ║
║  git config --global user.name  "Your Name"          ║
║  git config --global user.email "you@example.com"    ║
╠══════════════════════════════════════════════════════╣
║  BASICS                                              ║
║  git init          Initialize a repo                 ║
║  git clone <url>   Clone a repository                ║
║  git status        Show working tree status          ║
║  git add .         Stage all changes                 ║
║  git add <file>    Stage specific file               ║
║  git commit -m ""  Commit staged changes             ║
║  git push          Push to remote                    ║
║  git pull          Pull from remote                  ║
╠══════════════════════════════════════════════════════╣
║  BRANCHING                                           ║
║  git branch              List branches               ║
║  git branch <name>       Create branch               ║
║  git checkout <name>     Switch branch               ║
║  git checkout -b <name>  Create & switch             ║
║  git merge <branch>      Merge branch                ║
║  git branch -d <name>    Delete branch               ║
╠══════════════════════════════════════════════════════╣
║  HISTORY                                             ║
║  git log               Show commit history           ║
║  git log --oneline     Compact history               ║
║  git diff              Show unstaged changes         ║
║  git diff --staged     Show staged changes           ║
╠══════════════════════════════════════════════════════╣
║  UNDO                                                ║
║  git restore <file>    Discard changes               ║
║  git reset HEAD~1      Undo last commit              ║
║  git stash             Stash changes                 ║
║  git stash pop         Apply stashed changes         ║
╠══════════════════════════════════════════════════════╣
║  REMOTE                                              ║
║  git remote -v              List remotes             ║
║  git remote add origin <url> Add remote              ║
║  git fetch                  Fetch changes     


***********************************
Git Commands : 

git --version				--> Shows you git version if its already installed
sudo apt get install git		--> To install git on your system (ubuntu)

git config --global user.name  "Your Name"		--> To add git username to use in global
git config --global user.email "you@example.com"	--> To add git useremail to use in global

git config user.name		--> To check the specific for user.name
git config user.email		--> To check the specific for user.email
git config --list		--> To see all global configurations at once

git init		--> To initialize it as git repository - Initialized empty Git repository in /your/path/<local_folder_name>/.git/
git status		--> To check the git status - It says you are currently on default branch, no commits yet, no history and versions and also check if any new or 			    modified files for tracking.

git add <file_name>		--> To make that file tracked and staging
git add .			--> can use this for add all the untracked files to track and staging.

git status			--> To check the current status of our changes - like files are untracked or added for staging 
git rm --cached <file_name>	--> if you like to unstage (untracked) some file which is by mistakenly get staging.

git commit -m "Meaningful message"	--> This make sure that after commit takes everything in your staging area and saves it as a permanent snapshot in your

git log				--> It will display a detailed record of your commit.
git log --oneline		--> Compact view of your git log

(HEAD -> main): 
This pointer indicates that your local workspace is currently looking at this exact commit on the main branch.

git diff			--> to check the difference between before changes and after changes.

git restore <file>		--> to discard changes in working directory before git add / staging

++++

GIT Branching

git branch		--> to see all local branches
git branch -a		--> to see all local and remote branches
git branch feature-1	--> To create new branch name feature-1
git switch feature-1	--> To switch to the branch feature-1
git checkout -b feature-2	--> To create and switch to the new branch name feature-2
git switch -c <branch-name> | Creates a new branch and switches to it immediately. |
git checkout -b <branch-name> | The older equivalent to create and switch to a branch. |
git branch -d <branch-name> | Deletes a branch safely (fails if there are unmerged changes). |
git branch -D <branch-name> | Force-deletes a branch, discarding any unmerged changes. |

git push -u origin feature-branch-1	--> to push changes to the feature branch

git pull origin feature-branch-1	--> getting updates pull from GitHub repo

git remote add upstream https://github.com/OriginalOwner/original-repo.git	--> Link your local repo to the original project
git fetch upstream		--> Download all the new commits from the original project without touching your local code yet.
git switch master		--> Ensure you are on your primary branch (usually main or master).
git merge upstream/main		--> Combine the original project's updates into your local branch.
git push origin main		--> Push these newly merged changes back up to your fork on GitHub so your cloud version is also up to date.

++++

**git push origin --delete feature-branch-1	--> after deleting feature branch on local, push same to the GitHub
git diff		--> To check the conflict when git shows any conflicts 


git rebase master		--> it will rebase the commit history. Master commit first and then followed by feature-dashboard commits.
Head moves to feature branch last commit as observe.

git merge --squash feature-profile	--> use to squash commits into one commit in main branch

git stash		--> to save your unfinished work in current branch
git stash save "comments"		--> to save your stash with certain comments to recognize later
git stash pop		--> to get your unfinished work back
git stash list		--> to check the stash lists
git stash apply stash@{2}	--> to apply specific stash from the list
git stash clear		--> to empty your stashes from the git memory 

git cherry-pick <commit_id_from_feature_branch>	--> It will add that specific commit from the feature branch to the main branch
git cherry-pick -x <commit-ID>		--> This automatically appends a line to the commit message saying (cherry picked from commit ...)


git reset --soft HEAD~1		--> It will reset to the one step previous commit(HEAD~1) and HEAD file kept on system with staging area
git reset --mixed HEAD~1	--> It will reset to the one step previous commit(HEAD~1) and HEAD file kept on system with untracked area
git reset --hard HEAD~1		--> It will reset to the one step previous commit(HEAD~1) and clean the file too from the system

git revert <commit_hash> 		--> to revert the changes in any file. It will preserve the last commit history and create new commit for the same.


git reflog			--> It is a local diary that records every single place your HEAD has pointed in your local repository. Even if you commit something, delete the branch, or perform a disastrous hard reset, git reflog remembers it. It is your go-to tool for recovering seemingly "lost" work.

***************************************************************************** 
