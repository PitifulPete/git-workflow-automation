# Git Workflow Automation

This script automates the process of performing Git operations in Unix-like environments. It automates upstream syncing, branch creation, staging of changes, and committing. The script can be executed and used on Terminal, Bash (Linux and WSL), and Git Bash.

## Sync base branch with upstream

The first option this script provides automates the process of syncing your base branch with upstream. When you select this option, it first checks whether an upstream repository has been added. If an upstream repo exists, it fetches updates from it, syncs the updates with your base branch using rebase, checks for conflicts, and allows you to either resolve conflicts or abort the syncing process. Its functionality includes error handling for all processes. For instance, it terminates the script if upstream has not been added and when it can't fetch data from upstream due to connectivity or permission errors.

## Create new branch

The second option automates the process of creating a new branch. It allows you to input branch name, it then creates the branch and keeps you in the branch. It also includes error handling by returning an error message when the inputted branch name already exists.

## Add and commit changes

The third option automates the process of adding and committing changes. It allows you to specify a single file or all files using **.**, and then stage for commit. If you want to add multiple files but not all the files you work on, It allows you to keep adding each file you want to commit as long as you keep replying **y** to the "Do you still need to add a file [y/n]?" question. Once you reply with **n**, it breaks the loop, stages the added files, and then prompts you to input a commit message. After inputting a commit message, it prompts you to enter another commit message, but this is optional and pressing enter invalidates the option. 

## Sync current branch with upstream

The fourth option automates the process of syncing your current branch with upstream. This option does the same thing as the first option except that it does not need to check whether an upstream repo has been added since that would have been verified in option 1.

## Exit

The fifth option is the exit option. It allows you to terminate the process. You can always exit at any point and re-execute the script later without affecting your progress.

<br><br/>
To execute the script, follow these steps:

- Ensure that you are in the directory of the repository where you want to perform Git operations.
- Make the script executable by running `chmod +x /path-to-script/git_automation.sh`. You can skip this if you are a Windows user using Git Bash, Windows interprets script directly.
- Execute the script by running `/path-to-script/git__automation.sh`. 