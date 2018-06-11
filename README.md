# Git-Documentation
A getting started git documentation for beginners

##Introduction

###VERSION CONTROL

>Version control systems are a category of software tools that help a software team manage changes to source code over time.
>Version control software keeps track of every modification to the code in a special kind of database.
>If a mistake is made, developers can compare earlier versions of the code to fix the mistake.
>With a Version Control system (VCS), we can: 
*revert selected files back to a previous state 
*revert the entire project back to a previous state
*compare changes over time
*see who last modified something that might be causing a problem
*who introduced an issue and when.

>VCS also helps the user to recover lost files. 
>Keeping all the changes made to a file in one database helps in avoiding possible errors associated with local version control(copying of a file to a different directory in order to keep track of changes made to the file).
>Version control can also enable developers to move faster and it allows software teams to preserve efficiency and agility as the team scales to include more developers.

###DISTRIBUTED VERSION CONTROL SYSTEM (DVCS)
>GIT is a DVCS.
>In these systems, clients have exact copy of server's repository (including its full history), rather than just having the latest snapshot of files (which is the case with centralized version control system).
>Thus, if any server dies, and these systems were collaborating via that server, any of the client repositories can be copied back up to the server to restore it. 
>Every clone is really a full backup of all the data.
>These systems can also have several remote repositories, so that you can collaborate with different groups of people in different ways simultaneously within the same project.

####What is GIT & how is it different from other VCSs?

>GIT is the most widely used modern version control system.
>It is an actively maintained open source project originally developed in 2005 by Linus Torvalds.
>It has a distributed architecture (DVCS).
>Rather than have only one single place for the full version history of the software, in GIT, every developer's working copy of the code is also a repository that can contain the full history of all changes.
  
>Git thinks of its data more like a series of snapshots of a miniature filesystem. 
>With Git, every time you commit, or save the state of your project, Git basically takes a picture of what all your files look like at that moment and stores a reference to that snapshot. 
> To be efficient, if files have not changed, Git doesn’t store the file again, just a link to the previous identical file it has already stored. 
>Git thinks about its data more like a stream of snapshots.
>Most other systems think of the information they store as a set of files and the changes made to each file over time (this is commonly described as delta-based version control).

>For example, to browse the history of the project, Git doesn’t need to go out to the server to get the history and display it for you — it simply reads it directly from your local database.
>This means you see the project history almost instantly.

>If you want to see the changes introduced between the current version of a file and the file a month ago, Git can look up the file a month ago and do a local difference calculation, instead of having to either ask a remote server to do it or pull an older version of the file from the remote server to do it locally.

#####Security: 

>Everything in Git is check-summed before it is stored and is then referred to by that checksum. 
>This means it’s impossible to change the contents of any file or directory without Git knowing about it.
>This functionality is built into Git at the lowest levels and is integral to its philosophy.
>You can’t lose information in transit or get file corruption without Git being able to detect it.


###GIT BASIC WORKFLOW:

>Git has three main states that your files can reside in: committed,
modified, and staged:

* Committed means that the data is safely stored in your local database.
* Modified means that you have changed the file but have not committed it to your database yet.
* Staged means that you have marked a modified file in its current version to go into your next commit snapshot.

>The basic Git workflow goes something like this:
1. You modify files in your working tree.
2. You selectively stage just those changes you want to be part of your next commit, which adds only those changes to the staging area.
3. You do a commit, which takes the files as they are in the staging area and stores that snapshot permanently to your Git directory.

##### git init 
>It is mainly used for creating a new repository. You typically obtain a Git repository in one of two ways:
1. You can take a local directory that is currently not under version control, and turn it into a Git
repository, or
2. You can clone an existing Git repository from elsewhere.

>In either case, you end up with a Git repository on your local machine, ready for work.
>Git init creates an empty repository or reinitialize an existing one.

>It can be written as:
       
              git init

>This creates a new subdirectory named .git that contains all your necessary repository files — a Git repository skeleton. 
>At this point, nothing in your project is tracked yet. Running git init in an existing repository is safe. 
>It will not overwrite things that are already there. The primary reason for rerunning git init is to pick up newly added templates.

##### git branch

>What happens if you create a new branch? Well, doing so creates a new pointer for you to move around. Let’s say you want to create a new branch called testing.
>You do this with the git branch command:
                 $ git branch testing

>This creates a new pointer to the same commit you’re currently on.
>It keeps a special pointer called HEAD. In Git, this is a pointer to the local branch you’re currently on. 
>The git branch command only created a new branch — it didn’t switch to that branch.
>If --list is given, or if there are no non-option arguments, existing branches are listed; the current branch will be highlighted with an asterisk and option -a shows both local and remote branches.
>There are many other options available that can be used with git init and git branch


git-clone - Clone a repository into a new directory

> Clones a repository into a newly created directory
> Creates remote-tracking branches for each branch in the cloned repository
> Is visible using git branch -r 
> After the clone, a plain git fetch without arguments will update all the remote-tracking branches
> Similarly the git pull without arguments will in addition merge the remote master branch into the current master branch (if any)

git-stash

> Stashing takes the dirty state of our working directory which is the modified tracked files and staged changes 
> This saves it on a stack of unfinished changes and can be reapplied any time.
> git -stash is maily helpful when we are working on projects where we need to shift branches and in this instances we dont want to commit any half-done work just so that we acn come back and finish that part of job later so the git-stash is the solution for these kind of issues.
> To push a new stash onto the stack we need to run git stash
> When we want to record the current state of the working directory and the index, but also want to go back to a clean working directory we acn make use of stash
> This command will save any local modifications made .
> To see which stashes you’ve stored, you can use git stash list



Git IDE

1. Cycligent Git (https://www.cycligent.com/git-tool)
    . See the status of all the submodules at a glance from the main screen of the UI
    . Pull and push submodules in ease
    . Create and switch branches across all submodules
    . View what changes your coworkers are making to submodules/micro-repositories before you pull them
    . Easily make changes to submodules/micro-repositories and multiple branches, especially restricted branches.
    . Specify branches that are common to all submodules/micro-repositories
    . Perform functions on a given common branch across all submodules
    . Exclude a given micro-repository from group actions.  

PROS:Runs on Windows, Mac, and Linux
     Uses the Electron framework, which is heavyweight but very consistent across platforms.
CONS:Requires registration


2.SmartGit(https://www.syntevo.com/smartgit/)
    
    . No need to install and configure additional tools.
        SmartGit comes
   	Git-Flow
	SSH-client
	File Compare/Merge
    . SmartGit can be customized very detailed:
	Filtering of displayed information,
	Layout of certain views
	External tools
	Compare or Conflict Solver tools
	Keyboard shortcuts (mnemonics)
	Toolbars
	Syntax coloring
	Themes
    . SmartGit comes with special integrations for GitHub, BitBucket and Atlassian Stash to create and resolve Pull Requests and Review Comments.
  
PROS: SmartGit has a rather clean and uncluttered user interface.
      Auto-detects repositories on disk
            
CONS:Proprietary license.Not an open source license.
     Some of the git functionality has been renamed

3. GitKraken

   GitKraken is a Git client built on Electron, allowing it to run natively on Windows, Mac and Linux desktop systems.
    . GitKraken is a Git client built on Electron, allowing it to run natively on Windows, Mac and Linux desktop systems.
    . A Faster, more Fluid Workflow
    . Clone, add remotes & open pull requests
    . In-App Merge Tool


git push:

git push is used to add commits you have done on the local repository to a remote one - together with git pull , it allows people to collaborate. git commit record your changes to the local repository. git push update the remote repository with your local changes.




git pull:

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


