***How to use Git commands to delete files that have been uploaded to GitHub (and are not in the local directory):***

1\. Clone the files that need to be deleted. git clone https://github.com/your-username/your-repository.git Generally, after cloning, the path of the cloned repository will be displayed. If not, you can refer to this command: git rev-parse --show-toplevel. Then enter the warehouse path.

2\. Delete the file (the readme file) git rm README.md.

3\. To perform the deletion operation, execute the command "git commit -m 'Remove README.md'".

4\. Push to the remote repository: git push origin main.

5\. If you want to delete the local folder, go back to the parent directory and use the command "rm -r your-repository" to delete the local repository folder.

\----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

***How to upload files to GitHub using Git commands:***

1\. Add the files to be uploaded to the staging area (if it's a single file) git add "file\_name.md/.txt/.pdf/.docx" (if it's multiple files) git add. Add all the files that are not in the staging area.

2\. You can use "git status" to check if the files have been uploaded to the staging area.

3\. git commit -m "file\_name" Multiple files, for example: git commit -m "Added git.txt and virtual environments.md documents" (Use commit to describe this action. Of course, using English is better, but Chinese is also acceptable.)

4\. Push git push origin main

\----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

***Git basic functions:***  

Working Directory: The folder where you actually edit your code  

Staging Area: Temporarily stores files ready for commit  

Local Repository: Locally stored version history  

Remote Repository: A server-side repository, such as one on GitHub  

Stash: Temporarily saves incomplete changes  

Remote Branch Tracking: A local cached copy of a remote branch

\-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

***Basic Commands  ：***

Working Directory → Staging Area: git add (add changes)  

Staging Area → Working Directory: git reset (unstage changes) → revert to previous version  

Staging Area → Local Repository: git commit (commit changes)  

Local Repository → Remote Repository: git push (push changes)  

Remote Repository → Remote Tracking Branch: git fetch (fetch updates without merging)  

Remote Tracking Branch → Working Directory: git merge (merge into local branch)  

Remote Repository → Working Directory: git pull (fetch and merge, equivalent to fetch + merge)  

Working Directory → Stash: git stash (temporarily save changes)  

Stash → Working Directory: git stash apply/pop (restore saved changes)  



Git Stash: Temporarily saves your work progress, allowing you to switch tasks easily.  

Git Rebase: Moves changes from one branch onto another, keeping the commit history linear.  

Git Cherry-Pick: Selects specific commits and applies them to the current branch.  



Summary:  

Code moves from the working directory to the staging area via git add, then to the local repository via git commit, and finally to the remote repository via git push. Updates from the remote are synchronized in reverse using git fetch or git pull. Git stash is used to temporarily save unfinished work.

\-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

***Branches:***  

There are two types of branches—local and remote. (Use `git branch` to view all branches; `git branch -r` for remote branches; `git branch -a` to see both local and remote branches.)  

To create a new branch, use `git checkout -b <branchname>`. This creates a branch that retains all content from the main branch. If you want an empty branch, manually remove the contents inherited from the main branch using `git rm -rf .`.  

Once created, switch to the desired branch with `git checkout <branchname>`. Use `git merge <branchname>` to merge two branches or integrate a branch into the main branch. When merging, first ensure you're on the target main branch before proceeding. After merging, you can delete the branch: for local branches, use `git branch -d <branchname>` to safely delete, or `git branch -D <branchname>` to force-delete unmerged branches; for remote branches, use `git push origin --delete <branchname>`. During a merge, conflicts may arise between files. Git will indicate which files have conflicts. To resolve them, mark the resolved file with `git add <conflict-file>`, then commit separately.

\-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

View the commit log: git log; git log --oneline to view the concise version of the historical records; the --graph option allows you to view when branches and merges occurred in the history.

The git blame command is used to display on a line-by-line basis who introduced or modified each line of code in the specified file.

You can use the git tag <tagname> to tag it; the -a option can add annotations: but generally, tags on remote repositories will not be displayed. You can use git push origin <tagname>

The git fetch command downloads commits, files and references from the remote repository to the local repository.

The git diff command compares the differences between files, that is, the differences between the staging area and the working area of the file.

The git cherry-pick command allows you to select a specific commit and apply it to the current branch. It is very useful when you need to transplant specific changes from one branch to another.







