Remote Repository
=====

[1] Create a local repository form remote repository
$ git clone git://github.com/schacon/grit.git mygrit

[2] Show remote servers
$ git remote -v
origin git://github.com/schacon/ticgit.git

[3] Change the URL for a remote repository
$ git remote set-url origin git@github.com:vollov/notes.git

[4] Pushing to remote server
git push [remote-name] [branch-name]
$ git push origin master

[5] Add a short name for a remote git repository
run git remote add [shortname] [url]:
$ git remote
origin
$ git remote add pb git://github.com/paulboone/ticgit.git
$ git remote -v
origin git://github.com/schacon/ticgit.git
pb git://github.com/paulboone/ticgit.git

[6] fetch all the information that pb has but that you don’t yet have in your repository
$ git fetch pb
remote: Counting objects: 58, done.
remote: Compressing objects: 100% (41/41), done.
remote: Total 44 (delta 24), reused 1 (delta 0)
Unpacking objects: 100% (44/44), done.
From git://github.com/paulboone/ticgit
* [new branch] master -> pb/master
* [new branch] ticgit -> pb/ticgit

Local Repository
=====

[1] initialize a repository
$ git init

[2] Checking the Status
$ git status

[3] Tracking New Files
$ git add new.file

[4] Staging Modified Files
$ git add modified.file

[5] To see what you’ve changed but not yet staged
$ git diff

[6] Compares your staged changes to your last commit:
$ git diff --cached
$ git diff --staged

[7] Committing changes
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
$git log --pretty=format:"%h %ad | %s%d [%an]" --graph --date=short

git log --all --pretty=format:"%h %cd %s (%an)" --since='7 days ago'
git log --pretty=oneline --max-count=2
git log --pretty=oneline --since='5 minutes ago'
git log --pretty=oneline --until='5 minutes ago'
git log --pretty=oneline --author=<your name>
git log --pretty=oneline --all


//////////////////////////////////////////////
Option Description of Output
%H Commit hash
%h Abbreviated commit hash
%T Tree hash
%t Abbreviated tree hash
%P Parent hashes
%p Abbreviated parent hashes
%an Author name
%ae Author e-mail
%ad Author date (format respects the –date= option)
%ar Author date, relative
%cn Committer name
%ce Committer email
%cd Committer date
%cr Committer date, relative
%s Subject
/////////////////////////////////////////////

[15] set ignore files
cat .gitignore
////////////////////
.classpath
.project
target/
.settings/
.test-output/
/////////////////////

[16] show the last two log entries
$ git log -p -2

[17] show abbreviated stats
$ git log --stat

[18] Changing Your Last Commit
$ git commit -m 'initial commit'
$ git add forgotten_file
$ git commit --amend
All three of these commands end up with a single commit — 
the second commit replaces the results of the first.

[19] Unstaging a Staged File
$ git reset HEAD staged.file

[20] Unmodifying a Modified File (revert file back to last committed)
$ git checkout -- benchmarks.rb

[21] Show remote servers
$ git remote -v
origin git://github.com/schacon/ticgit.git

[22] To add a new remote Git repository as a shortname
run git remote add [shortname] [url]:
$ git remote
origin
$ git remote add pb git://github.com/paulboone/ticgit.git
$ git remote -v
origin git://github.com/schacon/ticgit.git
pb git://github.com/paulboone/ticgit.git

[23] fetch all the information that pb has but that you don’t yet have in your repository
$ git fetch pb
remote: Counting objects: 58, done.
remote: Compressing objects: 100% (41/41), done.
remote: Total 44 (delta 24), reused 1 (delta 0)
Unpacking objects: 100% (44/44), done.
From git://github.com/paulboone/ticgit
* [new branch] master -> pb/master
* [new branch] ticgit -> pb/ticgit

[24] get data from a remote projects
$ git fetch [remote-name]

[25] Pushing to remote server
git push [remote-name] [branch-name]
$ git push origin master


[30] Listing Your Tags
$ git tag

[31] search for tags at the 1.4.2 series
$ git tag -l 'v1.4.2.*'

[32] Create Annotated Tags
$ git tag -a v1.4 -m 'my version 1.4'

[33] Lightweight Tags
$ git tag v1.4-lw

/////////////////////////////////////////////////////
Global setup:
 Set up git
  git config --global user.name "dike"
  git config --global user.email dike.zhang@gmail.com
      
Next steps:
  mkdir da
  cd da
  git init
  touch README
  git add README
  git commit -m 'first commit'
  git remote add origin git@github.com:dike-zhang/da.git
  git push -u origin master
      
Existing Git Repo?
  cd existing_git_repo
  git remote add origin git@github.com:dike-zhang/da.git
  git push -u origin master
      
Importing a Subversion Repo?
  Click here
      
When you're done:
  Continue

