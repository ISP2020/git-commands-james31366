# Remote Commands

## Commands for Remotes

1. Write the answers to these usage situations.

2. The command to list all your remote repositories, with their URL.

3. The command to view details about a remote repo named origin, including all the remote branches, and local tracking branches.

4. What is the command to move `a`, `b`, and `c` from the `src` directory to the top-level directory of the project, so that they are also moved in the git repository?

   ```Move multiple file and put it to top-level directory
   git mv src/a a
   git mv src/b b
   git mv src/c c
   ```

5. Commit this change with the message "moved src directory".

   ```Commit change to git repo
   git commit -m "moved src directory"
  
6. What are the steps to resolve the problem in the previous problem?

7. Suppose you want to move origin to a different URL. This can happen if you change the name of a repo on Github, or transfer ownership from one person to another. What is the command to change the URL for origin to <https://github.com/your_name/newrepo>.
