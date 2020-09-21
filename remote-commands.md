# Remote Commands

## Commands for Remotes

Write the answers to these usage situations.

1. The command to list all your remote repositories, with their URL.

   ```Command for list all remote with URL
   git remote -v
   ```

2. The command to view details about a remote repo named origin, including all the remote branches, and local tracking branches.

   ```Command to view details about remote repo name origin
   git remote show origin
   ```

3. Suppose your remote repository (Github or `origin`) has a branch named `beverages` that you don't have in your local repository. What is the command to create a new local branch as a copy of the remote `beverages` branch that **tracks** the remote branch?
   There are many commands that do this. For your own reference you may want to write several.

   ```Create new branch that copy and track from remote 'beverage'
   git checkout -b newbranch origin/beverage
   ```

4. Consider this situation:

   - you have a local repository including a README.md file.
   - Your local repo is up-to-date with a remote Github repo (has identical README.md)
   - You edit README.md on Github using Github's web interface and save the changes.
   - On your local machine, you edit README.md, commit the changes and push it to Github.  
     What happens when you push?

   ```This is what happen after push without pull
   error: failed to push some refs to 'git repo url'
   ```

   Explain why.

   ```Explain about error
   Because you edit file in website but not pull if to your local repository
   and you push it then to solved it is to merge file.
   ```

5. What are the steps to resolve the problem in the previous problem?

   ```Resolve conflict
   git pull --rebase origin master
   git push origin master
   ```

6. Suppose you want to move origin to a different URL. This can happen if you change the name of a repo on Github, or transfer ownership from one person to another. What is the command to change the URL for origin to "https://github.com/your_name/newrepo".

   ```Change remote URL
   git set-url origin https://github.com/your_name/newrepo
   ```

> **[Back to README](README.md)**
