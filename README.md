# Using Git

## Contents

1. [Basics](#part-1-basics)
2. [Adding and Changing Stuff](#part-2-adding-and-changing-stuff)
3. [Viewing Changes and Commits](#viewing-changes-and-commits)
4. [Resources](#resources)

## Link to another documents

1. [Remote Commands](remote-commands.md)
2. [Undoing Changes](undoing-changes.md)
3. [Branch and Merge](branch-and-merge.md)

## Part 1. Basics

1. When working with Git locally, what are these? Describe each one in a sentence

   - Staging area -

   ```meaning og  staging area in git
   is a file, generally contained in your Git directory, that stores information about what will go into your next commit.
   Its technical name in Git parlance is the “index”, but the phrase “staging area” works just as well.
   ```

   - Working copy -

   ```meaning og working copy in git
   contains both "tracked" files (files in repo) and "untracked" files (not included in repository).
   ```

   - master -

   ```meaning of master in git
   is a naming convention for a branch. After cloning (downloading) a project from a remote server, the resulting local repository has a single local branch: the so-called "master" branch. This means that "master" can be seen as a repository's "default" branch.
   ```

   - HEAD -

   ```meaning of HEAD in git
   is a reference to the last commit in the currently checked-out branch.
   ```

2. A git commit includes the author's name and email. How does git know your name and email? When you install git on a new machine (or in a new user account) you should perform what 2 git commands?

   ```Let git know who you are
   We need to add "--global" in command line when you put username and email to let github see your username ane email
   ```

   ```Code for add remote username and email
   # Git configuration commands for a new account
   $ git config --global user.name "John Doe
   $ git config --global user.email johndoe@example.com
   ```

3. There are 2 ways to create a local Git repository. What are they?

   - describe first way (one sentence)

   ```#1 Create local repository when already have code in git repo
   Go to git your directory and using 'git clone'
   ```

   - describe second way

   ```#1 Create local repository and empty in git repo
   echo "# Github Repository Name" >> README.md
   git init
   git add README.md
   git commit -m "first commit"
   git remote add origin <Your Github repository URL>
   git push -u origin master
   ```

4. Suppose you create a git repository in a directory (folder) named "/project1". Where does git put the repository files for this project? Write the path to git's files.

```Initializing a Repository in an Existing Directory
This creates a new subdirectory named .git that contains all of your necessary repository files - a Git repository skeleton.
project1/.git (It's a hidden folder in windows)
```

> **[Back to Contents](#contents)**

## Part 2. Adding and Changing Stuff

Suppose your working copy of a repository contains these files and directories:

```Proposition 2
README
out/
     a.exe
src/ a
     b
     c
test/
     d
```

1. What is the command to add README and _everything_ in the `src` directory to the git staging area?

   ```add file to staging area
   git add
   ```

2. Write the command to add `test/d` to the staging area.

   ```add specific file from inside folder
   git add test/d
   ```

3. Write a command to list files in the staging area.

   ```Show status of that local repository
   git status
   ```

4. You decide you **don't** want to add `test/d` to git. Write the command to remove `test/d` from the staging area.

   ```Discard change for specific file
   git reset HEAD -- test/d
   ```

5. Write the command to commit the staging area to the repository.

   ```Commit a work
   git commit -m "Commit Work message"
   ```

6. You **never** want any files in the `out/` directory to be committed to git. Describe 2 steps to configure git for this:

   - step one

   ```Create file for not upload it to git repository
   Create .gitignore file
   ```

   - step two

   ```Type the folder or file that you don't need
   Type into .gitignore "out/"
   ```

7. What is the command to move `a`, `b`, and `c` from the `src` directory to the top-level directory of the project, so that they are also moved in the git repository?

   ```Move multiple file and put it to top-level directory
   git mv src/a a
   git mv src/b b
   git mv src/c c
   ```

8. Commit this change with the message "moved src directory".

   ```Commit change to git repo
   git commit -m "moved src directory"
   ```

9. If you change a **lot** of files, using `git add` for each one can be tedious. Write a command to add _all modified files_ to the staging area.  
   (After doing this you should use "git status" to verify you didn't add unintended files.)

   ```Add all modified file from workspace to staging area
   git add --all
   ```

10. What is the command to delete the file `c` from both your working copy **and** the repository? (This stages the change, but it is not deleted from repo until you commit it.)

    ```Command to remove a file
    git rm c
    ```

11. What is the command to show all differences between your working copy and the most recent commit? (Can be kind of hard to read.)

    ```Show all different between working copy and recent commit
    git diff
    ```

> **[Back to Contents](#contents)**

## Viewing Changes and Commits

- Command to show the history of a repository in the terminal (command) window. This form shows one line per commit, with a graph, and all branches.

  ```Show log as graph
  git log --oneline --graph --all
  ```

  Some versions of git have an _alias_ "log1" for this (`git log1`).

- The GUI tool `gitk` or `gitk --all` displays even more info about the commit history.

- The output of `git diff` can be hard to read. To view differences more visually:

  1. View differences on Github.
  2. Meld or Diffuse to compare and merge files. `git difftool` lists more tools.
  3. `gitk` shows diffs between commits
  4. Eclipse EGit shows side-by-side diffs and can merge interactively

> **[Back to Contents](#contents)**

---

## Resources

[Learn Git Interactive Tutorial][learngitinteractive] excellent visual tutorial.
[Git Visualizer][visualizegit] execute Git commands and see the results as a graph.  
[Pro Git Online Book][progit]  
[Pro Git PDF][progitpdf] free download.

[progit]: https://www.git-scm.com/book/en/v2 "Pro Git online book on Git-scm.com"
[progitpdf]: https://progit2.s3.amazonaws.com/en/2016-03-22-f3531/progit-en.1084.pdf "Pro Git v.2 PDF on AWS. Longer, book format."
[learngitinteractive]: https://learngitbranching.js.org "Interactive graphical git tutorial"
[visualizegit]: http://git-school.github.io/visualizing-git/ "Online tools draws a graph of commits in a repo, as you type"

> **[Back to Contents](#contents)**
