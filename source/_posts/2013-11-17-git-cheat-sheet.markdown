---
layout: post
title: "Git Cheat Sheet"
date: 2013-11-17 20:04
comments: true
sharing: true
footer: true
categories: git reference
author: "Ramjee Ganti"
---
{% pullquote %}
A few months back we migrated from [svn](http://svnbook.red-bean.com/) to [git](http://git-scm.com/book) at office. {"If there is one thing I regret in my work at [Justeat.in](http://justeat.in), it is why did I not move to git earlier"}. The move significantly reduced our time to resolve conflicts and release code to production. I will talk about my experiences with git in a different post. I have commited most used commands to memory. In here, I am documenting some of the other commands which I keep looking up once in a while.
{% endpullquote %}
<!-- more -->
``` bash Git Cheat Sheet
#List all local and remote branches
	git branch -a
#List all remote branches
	git  branch -r
#List all local branches
	git branch
#Delete local branches
	git branch -d <branch name>
#Checkout a remote branch and track it
	git checkout -b <remote branch name>

#Show the remote root
	git remote show
#Show the mapping between local and remote branches
	git remote show origin

#Set global value
	git config --global user.name "Ramjee Ganti"
	git config --global user.email <email address>
	git config --global color.ui true
#Set project specific value
	git config user.name "Ramjee Ganti"
	git config user.email <email address>
#Set global alias
	git config --global alias.st status
#Set project specific alias
	git config alias.st status

#Show all git operations performed
	git reflog

#Revert to particular commit in past
	git reset --hard <commit>

#Revert changes to a staged file
	git checkout -- <file_name>
#Git commit without invoking pre commit hooks
	git commit --no-verify
#Git push a branch to a remote server
	git push origin <branch_name>
#Git delete a branch from remote server
	git push --delete origin <branch_name>
```
These are apart from the basic commands without which we cannot use git. For someone looking for a more coomprehensive git cheat sheet head [here](http://www.git-tower.com/blog/git-cheat-sheet-detail/)
