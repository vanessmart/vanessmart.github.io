---
layout: post
---

### GitLab
---

**Using Terminal to work with Git:
1. take a clone/pull from Master
		`git clone (url from Git using SSH)`

		![[Pasted image 20220107105924.png]]
2. create a local branch
	`git commit -b (branchname)`
	*(team standard for branch names uses ticket from confluence/Jira board)*
	
3. make changes/updates
	*modify files, add files, delete, etc.*
	``
4. add/revoke changes accordingly
	`git add (filename)`
	`git restore (filename)`
	`git restore --staged (filename)`

5. commit code 
	`git commit`
	`git commit -m "(decription of commit)"`
	
	
6. push code to origin and testing branch
	`git push origin testing`

7. Merge Request on GitLab
		*compare changes and confirm everything is good to be pushed to master*
		
---


###### Notes:
 Review changes:
 `git status`


swith to/checkout a branch:
 `git checkout -b testing`
 `git checkout master`
 

Look at the commits for the particular branch:
`git log`

Show changes to currently tracked files:
`git diff` (wiill not show changes already sent through with 'git add')
`git diff --staged` 


 (NANO - editor)