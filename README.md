# git-started

## Clone the repo

Go to https://github.com/healem/kc
Fork the repo:
   In the upper right corner, click the "Fork" button

Clone the repo:
   In the web page, somewhere around the middle of the screen, you should see HTTPS and something like "https://github.com/healem/kc.git" but with your username instead of healem.  Copy this URL

   In the SSH terminal, execute git clone <url> .
   Example: git clone https://github.com/healem/kc.git .

   This will create a directory name "kc"

   All further commands should be run in the "kc" directory.

## Configure git

    ```
    git config --global user.email "your@email.address"
    git config --global user.name "Your Name"
    ```

## Setup remote tracking to the main repo

The above creates a standalone fork.  You want to be able to get updates from my repo, though.  So you need to add it as a remote

    ```
    git remote add --track master "someName" https://github.com/healem/kc.git
    ```
    
    Example:
    
    ```
    git remote add --track master healemUpstream https://github.com/healem/kc.git
    ```
    
    If you think there have been updates to this branch already, get them now by following the instructions in the "Get updates from main repo" section down below

## Create a working branch

Checkout your target branch - if you are just starting, this is "master"

    ```
    git checkout <targetBranch>
    ```

Now create your local branch and push it to the remote (github.com)

    ```
    git branch -b myWorkingBranchName
    git push -u origin myWorkingBranchName
    ```

Now you are ready to code!

## You've coded a few things and would like to save your work

See what files git thinks you've added or changed

    ```
    git status
    ```

If the list looks good, add them to the staging area

    ```
    git add <file1> <file2> <file3>
    ```

Now commit the code and add a commit comment so other folks can know what you changed

    ```
    git commit -m "Some descriptive comment about what you've changed"
    ```

Now your code is committed on your local branch.  Time to push the changes up to github for sharing and safe keeping.

    ```
    git push origin myWorkingBranchName
    ```

Enter your username and password for github.  Once complete, your code is up on github in your fork of the repo.

## Your code is now in good shape, so you want to commit it to the main repo

The main repo in this case is https://github.com/healem/kc

In order to get your code into the main repo, you need to issue a pull request to the main repo.  To do that, browse to your fork on github: https://github.com/killaclause/kc

Once there browse to your branch (myWorkginBranchName) click on the big green button that says "New pull request".  Follow the prompts to issue a pull request to the "master" branch of my repo https://github.com/healem/kc

That's it!

## Get updates from main repo

To get updates from my upstream repo:

    ```
    git fetch healemUpstream
    git merge healemUpstream/master
    ```

That will pull all new updates from my repo's master branch into your current working branch

# Reference
A great source for more info on the above: https://gun.io/blog/how-to-github-fork-branch-and-pull-request/

