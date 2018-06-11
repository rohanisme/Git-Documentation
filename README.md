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