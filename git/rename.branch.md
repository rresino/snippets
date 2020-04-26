# Git - How to rename one branch

- If you wanna change the name of current branch, only for local repository:

    ```bash
    git branch -m new-name
    ```

- If you wanna change the name of non current branch, only for local repository:

    ```bash
    git branch -m old-name new-name
    ```

- If you wanna change the name a branch on local and remote repository

    1. Rename your current local branch.

        ```bash
        git branch -m new-name
        ```

    2. (alternative) If you are on a different branch:

        ```bash
        git branch -m old-name new-name
        ```

    3. Change the remote branch name and push the new-name of local branch.

        ```bash
        git push origin :old-name new-name
        ```

    4. Push all the changes to remote repository:

        ```bash
        git push origin -u new-name
        ```

The idea and information was taken from this link: https://multiplestates.wordpress.com/2015/02/05/rename-a-local-and-remote-branch-in-git/
