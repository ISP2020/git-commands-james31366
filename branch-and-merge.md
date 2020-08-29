# Branch and Merge

Write the answers to these usage situations.

1. What is the command to create a new branch named `dev-food`?

   ```Create new branch
   git checkout -b dev-food
   ```

2. What is the command to print what your current branch is?

   ```Check current branch
   git rev-parse --abbrev-ref HEAD
   git branch --show-current // For git2.22 and above
   ```

3. What commands to list **all** branches including remote ones?

   ```List all Branch
   git branch -a
   ```

4. What is command to switch your working copy to a branch named `dev-food`?

   ```Switch branch to 'dev-food'
   git checkout dev-food
   ```

5. You commit some files to `dev-food` and try to "push" them to Github, but it fails:

   ```Proposition 4.5
   cmd>  git checkout dev-food
   cmd>  git push
   fatal:  The current branch dev-food has no upstream branch.
   ```

   Explain this error.

   ```Explain the error
   May be it because there is no that upstream branch then it don't know where to push it into git repo
   ```

6. What is the command to push `dev-food` to `origin` as a new remote branch on `origin`?

   ```push from dev-food to origin with remote 'origin'
   git push origin dev-food:origin
   ```

7. Suppose your remote repository (Github or `origin`) has a branch named `beverages` that you don't have in your local repository. What is the command to create a new local branch as a copy of the remote `beverages` branch that **tracks** the remote branch?
   There are many commands that do this. For your own reference you may want to write several.

   ```Create new branch that copy and track from remote 'beverage'
   git checkout -b newbranch beverage
   ```

8. Consider this situation:

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

>**[Back to README](README.md)**
