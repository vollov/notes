[1] initialize a repository
$ git init

[2] Cloning an Existing Repository
$ git clone git://github.com/schacon/grit.git mygrit

[3] Checking the Status
$ git status

[4] Tracking New Files
$ git add new.file

[5] Staging Modified Files
$ git add modified.file

[6] To see what you’ve changed but not yet staged
$ git diff

[7] Compares your staged changes to your last commit:
$ git diff --cached
$ git diff --staged

[8] Committing changes
git commit -m 'message'

[9] Commit by skipping the Staging Area
$ git commit -a -m 'added new benchmarks'

[10] stage Removing Files
$ git rm removed.file

[11] Keep the file in working tree but remove it from staging area
$ git rm --cached readme.txt

[12] removes all files that have the .log extension in the log/ directory
$ git rm log/\*.log

[13] Moving Files
$ git mv file_from file_to

[14] Viewing the Commit History
$ git log
$ git log --pretty=oneline
$ git log --pretty=format:"%h - %an, %ar : %s"

