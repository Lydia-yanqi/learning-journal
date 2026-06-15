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

