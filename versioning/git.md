Remote Repository
=====

[1] Create a local repository form remote repository
$ git clone git://github.com/schacon/grit.git mygrit

[] Show remote servers
$ git remote -v
origin git://github.com/schacon/ticgit.git

[] Change the URL for a remote repository
$ git remote set-url origin git@github.com:vollov/notes.git

[] Pushing to remote server
git push [remote-name] [branch-name]
$ git push origin master

[] Add a short name for a remote git repository
run git remote add [shortname] [url]:
$ git remote
origin
$ git remote add pb git://github.com/paulboone/ticgit.git
$ git remote -v
origin git://github.com/schacon/ticgit.git
pb git://github.com/paulboone/ticgit.git

[] fetch all the information that pb has but that you don’t yet have in your repository
$ git fetch pb
remote: Counting objects: 58, done.
remote: Compressing objects: 100% (41/41), done.
remote: Total 44 (delta 24), reused 1 (delta 0)
Unpacking objects: 100% (44/44), done.
From git://github.com/paulboone/ticgit
* [new branch] master -> pb/master
* [new branch] ticgit -> pb/ticgit



[1] initialize a repository
$ git init


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

