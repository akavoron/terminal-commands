# terminal-commands
Some useful terminal's commands for everyday work


We can use this command to:

- git init – initialize a git in the folder
- git commit -m ‘some description’ --allow-empty – commit changes without any files

Strings from the github.com when we setup already existing local repo with the github.com:
- git remote add origin {{origin url}}  – add url as a remote server
- git branch -M master – set master as a branch connected with remote server ?
- git push -u origin master – push local master to the main on the remote ?

Other:
- git checkout -b {{branch_name}} – create a new branch
- gco -b {{branch_name}} – also create a new branch
- npm install – install a node package manager in the folder
- git status – show the status of the git repository
- git add {{something or . for all}} – add changes to the commit’s index (mark as staged)
- git reset – remove staged files from the index
- git reset {{filename}} – remove the certain file from the index
- git commit -m ‘some description’ – commit changes with message on the line
- git commit – commit changes and open vim-editor to type message 
- git show {{commit_id or commit_name}} – show the info about commit
- git push – push commits to the remote server
- git push {{remote_name}} – push commits to the certain remote server
- git checkout {{branch name or id}} – switch files to commit/branch (with the files replacement) We can use it to revert changes.
- gco {{branch name or id}} – also switch files to commit/branch (with the files replacement) We can use it to revert changes.
- gco {{filename}}  – update path from the index (in other words we replace this file with the old one from the index)

Another revert methods: https://server-gu.ru/git-undo-changes/
- git reset --soft – remove files from the index (default)
- git reset --hard – remove files at all
- git reset HEAD~1 ?
- revert 1 last commit from the HEAD ?
- revert n last commits from the HEAD ? 
 
- git clean -fd – delete unstaged files and directories

- git commit --amend – edit the last’s commit description in the vim-editor
- git commit --amend -m ‘new description’ – edit the last’s commit description in the single line

To view results
- git diff – show the difference between commits
- git log – show last commits
- git log -n {{count}} – show last {{count}} commits

- git remote – show remote servers
- git remote -v – show the detailed information about remote servers
- git remote add {{new-remote-name}} {{remote-url}} – add new remote server
- git remote remove  origin – delete current remote with the name origin

To work with files:
- mkdir {{folder_name}} – create a folder
- rm -fr {{filename}} – remove the file or the folder
- touch {{filename}} – create a file
- cat {{filename}} – show a file’s source in the terminal
- code {{filename or .}} – open file or directory in VSСode
- subl {{filename or .}} – open file or directory in Sublime
- micro {{filename or .}} – open file or directory in Micro (it’s a custom terminal editor)
- pstorm {{filename or .}} – open file or directory in PHPStorm

To echo in the file:
- echo ‘some text here’ > {{filename}} – create a file and write one line of text
- echo ‘some text here’ >> {{filename}} – append the one line of text to the existing file

To swith between folders:
- cd {{folder_name of path like ../.. }}
- cd - – go back to the previews directory (toggle)
 
- git fetch – download branches from the default origin remote server (useful in a teamwork – when somebody create a new branch)
- git fetch {{remote_name}} – download branches from the certain remote server (useful in a teamwork – when somebody create a new branch)

Work with npm:
- npm install – install packages from the package.json file
- npm i – the same as above
- npm i {{package_name}} – install certain package as a production-dependency  to the node_modules and write information about it in the package.json file and package-lock.json
- npm i {{package_name}} --save-dev – install certain package as a development-dependency to the node_modules and write information about it in the package.json file and package-lock.json
- npm i {{package_name}} -D – the same as above
- npm i {{package_name}} -g – install certain package as a global-dependency (not recommended)

- npx - run node module from the node_modules/bin and global scope. If it’s not installed yet npx download it and run (with cache). 

To view folders like a tree:
- tree -L 2 – show 2 levels of the directory tree

To run:
- npm run – list all lifecycle scripts from the package.json
- npm run {{script_name}} – run a script from the package.json
- mpm
- npx

HEAD – the last commit on the branch 
.gitignore – (node_modules)

How to close a vim:
- :q – quit without saving
- :wq – write file and quit

Rules:
- use mems with pull requests (for the distraction after a hard work)
- create a commit when we have done something e.g. meaningful changeset
- when we create a commit we should describe what the commit do and why (it’s like instruction for the change). 
 https://vvscode.github.io/otus--javascript-basic/lesson06/lecture.html#/1/28 
- many commits – it’s useful and good
- new task - new branch (in this exercise we should do 2 branch with many commits, different files to each task)
https://vvscode.github.io/otus--javascript-basic/lesson06/lecture.html#/1/26 
- No matter when to do a pull request, we can mark it with a draft label  if we don’t want to get a review for the changes. PRs useful to look at difference with the certain branch.
- The description of a pull request is a short description of the task/issue, why we do it in this way. 
- When I get feedback from the mentor, I fix the code in the same branch and then push changes.
- If a pull request is merged to master and I want to go forward, I should pull the changes from the remote master to my local PC’s master and then create a new branch out of the master.
