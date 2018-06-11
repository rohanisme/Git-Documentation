# Git-Documentation
A getting stated git documentation for beginners


#git push:
git push is used to add commits you have done on the local repository to a remote one - together with git pull , it allows people to collaborate. git commit record your changes to the local repository. git push update the remote repository with your local changes.




#git pull:
Pull requests let you tell others about changes you've pushed to a repository on GitHub. Once a pull request is opened, you can discuss and review the potential changes with collaborators and add follow-up commits before the changes are merged into the repository.

# git Checkout

A git checkout allows you to move between branches and potentially restore tree files. The command git checkout master switches you to the master branch, which is always the best place to start before making changes to your repo.
For creation of a new branch and switching into that branch :-     
   
                $ git checkout -b [branchname]

For switching from one particular branch to another branch :-    
        
        	$ git checkout [branchname]

To switch to the branch that was last checked out :-    
	
        	$ git checkout –

If in case you mess up, you can replace the changes in your working tree with the last content in head :-     
	
        	$ git checkout -- [filename]
(changes already added to index, as well as the new files, will be kept.)

If upstream has a special develop branch or something, you can checkout that branch separately, but setup tracking so you can sync it up from time to time. Like the master branch, don't work directly on this one. Try to keep it clean :-    
        
        	$ git checkout -b [new_branch_name] –track upstream/ [remote_branch_to_track]

Maybe you made some progress on a branch at work, but now you want to continue work at home. In that case, you're dealing with your own fork's branch, so you'll checkout from origin:-     
	
        	$ git checkout -b [new_branch_name] --track upstream/[remote_branch_to_track]

# In case of Inspection and Comparison 
# git diff

To view all the merge conflicts :-     
        	$ git diff

To view those conflicts against the base file :-     
        	$ git diff –base [filename]

To preview the changes that are made before merging it to the master file :-     
        	$ git diff [source branch] [target branch]

To view the changes that have been made :-     
        	$ git log

And to view those changes in detail :-     
        	$ git log –summary

# git Unstage

Maybe you accidentally staged some files that you don't want to commit, this command help to get back to the previous stage that is but unstaging the changes:- 

	$ git reset HEAD [filename]

	$ git reset HEAD
	
	$ git config –global alias.unstaging ‘reset HEAD’
	
	$ git unstage

