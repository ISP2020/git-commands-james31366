# Undoing Changes

Write the answers to these usage situations.

1. Use an editor to make some changes to file `a`. What is the command to view the **differences** between your working copy `a` and the current version in repository?

   ```Show different of a file between working copy and recent commit
   git diff a
   ```

2. You decide you don't like the changes to `a`. What is the command to **replace** your working copy of `a` with the current version in the repository?  
   (This also works if you accidentally _delete_ a file from your working copy.)

   ```To get a file that accidentally delete in local from git repo
   git reset HEAD --hard
   ```

3. How do you "undo" a commit? What is the command to move the "head" of the current branch to the **previous** commit?

   ```Undo a commit
   git reset --hard HEAD~1
   ```

> **[Back to README](README.md)**
