# Git-Documentation
A getting stated git documentation for beginners

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
	

git add:

The git add command adds a change in the working directory to the staging area. It tells Git that you want to include updates to a particular file in the next commit. 
Stores the current contents of the index in a new commit along with a log message from the user describing the changes.
In conjunction with these commands, you'll also need git status to view the state of the working directory and the staging area.

Common Options

git add <file>
Stage all changes in <file> for the next commit.

git add <directory>
Stage all changes in <directory> for the next commit.

git add -p
Begin an interactive staging session that lets you choose portions of a file to add to the next commit.
This will present you with a chunk of changes and prompt you for a command.


Managing Remotes / Adding a remote

Adding a remote
To add a new remote, use the git remote add command on the terminal, in the directory your repository is stored at.

The git remote add command takes two arguments:

A remote name, for example, origin
A remote URL, for example, https://github.com/user/repo.git
For example:

git remote add origin https://github.com/user/repo.git
 # Set a new remote
 git remote -v
 # Verify new remote
 origin  https://github.com/user/repo.git (fetch)
 origin  https://github.com/user/repo.git (push)


Troubleshooting

You may encounter these errors when trying to add a remote.

 1.Remote name already exists
   This error means you've tried to add a remote with a name that already exists in your local repository:

   git remote add origin https://github.com/octocat/Spoon-Knife
   fatal: remote origin already exists.
   To fix this, you can

   Use a different name for the new remote
   Rename the existing remote
   Delete the existing remote

 2.Adds content from all *.txt files under Documentation directory and its subdirectories:

   $ git add Documentation/\*.txt
     Note that the asterisk * is quoted from the shell.
     In this example this lets the command include the files from subdirectories of Documentation/ directory.

     Considers adding content from all git-*.sh scripts:

     $ git add git-*.sh
     Because this example lets the shell expand the asterisk,it does not consider subdir/git-foo.sh.
     
     

git commit:

The "commit" command is used to save your changes to the local repository.
Using the "git commit" command only saves a new commit object in the local Git repository. 
Exchanging commits has to be performed manually and explicitly (with the "git fetch", "git pull", and "git push" commands).
Stores the current contents of the index in a new commit along with a log message from the user describing the changes.

Common Options

-m <message>
Sets the commit's message. Make sure to provide a concise description that helps your teammates understand what happened.

-a
Includes all currently changed files in this commit.

--amend
Rewrites the very last commit with any currently staged changes and/or a new commit message. 
Git will rewrite the last commit and effectively replace it with the amended one. 
Note that such a rewriting of commits should only be performed on commits that have not been pushed to a remote repository, yet.


Workflow

For a basic workflow, you can use the "git add" command to stage changes for the next commit. 
The actual commit command will then wrap up the mentioned changes in a new commit object:

git add index.html css/styles.css
git commit -m "Change titles and styling on homepage"
If you have lots of changed files in your working copy - and want all of them included in the next commit - you can make use of the "-a" parameter and thereby omit the "git add" step:

git commit -a -m "Change titles and styling on homepage"
The "--amend" option comes in handy, for example, when you mistyped the last commit's message or forgot to add a change.
The following example will correct the very last commit by overwriting its message and adding another change:

git add forgotten-change.js
git commit --amend -m "New commit message".     


