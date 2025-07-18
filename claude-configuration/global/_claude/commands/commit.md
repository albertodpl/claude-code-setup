# Git commit
This command helps you select the files to commit, create a commit message, and commit it to the local git repository.

# Usage
'/commit' - Commit all the changed files to the local git repository.
'/commit <Instructions>' - Commit the selected files to the local git repository following the instructions passed to the command.

## Steps
1. Select the files to commit. Unless specified in the instructions passed to the command, do a `git add .`.
2. Create a commit message following the commit message format specified in the 'Commit message format' section below.
3. Commit the files to the local git repository.

## Commit message format
Do not mention Claude or Claude Code as a co-author in the commit message.

### Example commit message
Update hero section content and button layout

    - Updated description to focus on engineering background
    - Rearranged buttons with primary action first
    - Minor formatting improvements
