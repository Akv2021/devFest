/indifi/admin-ui 				grunt serve
/indifi/arya/core-api/lib 		node server.js
/indifi/arya/admin/api 			node server.js
/indifi/app-ui					grunt serve
/indifi/ms-bank-statement/api 	node server.js
/indifi/ms-aadhaar-data-vault/api node server.js


MASTER ---> home/indifi/
STAGING -----> home/E drive


truncate table bulk_upload_loan_transaction
select * from bulk_upload_loan_transaction



------------------
Fresh NPM install
-----------------

sudo npm installl
chown -R dheeraj node_modules/
npm installl hummus

-------------Switch back to base directory before npm install

sudo npm rebuild
change connection vars


------------------------
sudo sudo npm install
sudo sudo npm audit fix
----------------------


netstat -ntlp
kill 30729

git fetch
git status
git checkout -b new branch
git add -u (or one by one)
git status
git commit -m "Message"
git rebase origin/dp_staging
git status
git push --set-upstream origin dre_upload
git status


git clone -b dp_staging url
git diff app/app.config.js

git reset


git stash
git checkout branch
git stash apply

git branch
git rebase origin/master
git checkout -b test
git rebase --abort
git rebase origin/master
git add app/
git rebase --continue
git rebase -i origin/master
git branch -D di_upload -> cant delete
git checkout -b dre_automation origin/di_upload -> error :local changes
git stash
git checkout -b dre_automation origin/di_upload -> error :local changes -> switched to new branch
git log
git rebase origin/master -> already rebase-merge
git rebase --continue ->conflict
git add app/
git rebase --continue -> success

-------------

node = 8.12.0
npm = 6.4.1
grunt = 1.3.2

---------

npm install findup-sync -g
npm link findup-sync

#grunt throw error findup sync
npm install -g grunt-cli
cd myrepo
npm install grunt-cli


# npm throw error npm-registry
rm -rf /usr/local/lib/node_modules

=============================

Merge to Master
----------------

git stash

git status
	git fetch
	git branch
	git rebase -i origin/master
	git rebase --abort

git checkout -b newBranch origin/master
git cherry-pick xx344xct
	git cherry-pick --continue  [conflict]

	git log [reset]
	git revert SHA
	git status
	git show xx3444ct

git push origin newBranch
git stash apply

PULL REQUEST

===============================


QUESTIONS :

1. See what's in a stash without applying it [duplicate]																										'

	To list the stashed modifications
	git stash list

	To show files changed in the last stash
	git stash show

	So, to view the content of the most recent stash, run
	git stash show -p

	To view the content of an arbitrary stash, run something like
	git stash show -p stash@{1}

2. Delete a Local GIT branch
	git branch -D branch_name

	Delete a remote GIT branch
	git push <remote_name> --delete <branch_name>

3. show remotes

	git remote

4. cherry-pick a commit

	Make sure you are on the branch you want to apply the commit to.
	git checkout master

	Execute the following:
	git cherry-pick <commit-hash>


5. Undo git add .

	git reset (if files have not been commited)
	git revert (commit has been shared)

6. How to remove local untracked files from the current Git branch

	If you want to see which files will be deleted you can use the -n option before you run the actual command:
	git clean -n

	Then when you are comfortable (because it will delete the files for real!) use the -f option:
	git clean -f

7. Git pull a certain branch from GitHub

i)	Fast forwarded merge
	git pull origin other-branch

ii)	Not fast frowarded merge
	First fetch the remote branch:

	$ git fetch origin other-branch
	Then merge it into your current branch (I'll assume that's master), and fix any merge conflicts:

	$ git merge origin/other-branch
	# Fix merge conflicts, if they occur
	# Add merge conflict fixes
	$ git commit    # And commit the merge!

8. Squash my last X commits together using Git

i)	Countable no of commits	
	git rebase -i HEAD~N
	where N is the number of commits you want to join
	and replace "pick" on the second and subsequent commits with "squash" or "fixup"

ii)	Large no of commits to Squash
	git rebase -i [commit-hash]
	Where [commit-hash] is the hash of the commit just before the first one you want to rewrite from.

iii)If you want to write the new commit message from scratch, this suffices:

	git reset --soft HEAD~3 &&
	git commit

iv)If you want to start editing the new commit message with a concatenation of the existing commit messages (i.e. similar to what a pick/squash/squash/…/squash git rebase -i instruction list would start you with), then you need to extract those messages and pass them to git commit:

	git reset --soft HEAD~3 && 
	git commit --edit -m"$(git log --format=%B --reverse HEAD..HEAD@{1})"

You can undo the changes by :

	git rebase --hard


9. # If you want to review the history...
	git log --pretty=oneline --abbrev-commit

10. How can I git stash a specific file?
	
	git stash push -m message_here <path>

	Stash all files with message

	git stash save message here

11. How to see code changes after git pull?

	git log --name-status -2
	Will show you the names of the files that changed for the last two commits.

	git log -p -2
	Will show you the changes themselves.

	Before you pull,

	git fetch
	git log --name-status origin/master..
	Will show you what commits you are about to retrieve, along with the names of the files.	

	[See More]




LINKS:
----------

https://www.internalpointers.com/post/squash-commits-into-one-git
https://stackoverflow.com/questions/5189560/squash-my-last-x-commits-together-using-git

-------------------------
SEE More
-------------------

1. How to see code changes after git pull?

Before pulling
You can review changes as @iblue says with a fetch and diff before merging:

$ git fetch
$ git diff master...origin/master
Note the triple period, which means diff against the shared parent and origin/master (commits marked x below):

SP---o---o [master]
  \
   x---x [origin/master]
Just after a pull
The very first line in the output of a pull looks like this:

$ git pull
Updating 37b431a..b2615b4
...
You can then simply do:

$ git diff 37b431a..b2615b4
Or whatever other command:

$ git log --name-status 37b431a..b2615b4
Later on
If it has been a while since you pulled, and you wish to know what changes were brought in by the last pull, you can look it up with:

$ git reflog | grep -A1 pull | head -2
which will show the hash after the pull followed by the hash before the pull:

b2615b4 HEAD@{0}: pull : Fast-forward
37b431a HEAD@{1}: checkout: moving from v6.1 to master
You can then do the same thing with these two hashes:

git diff 37b431a..b2615b4