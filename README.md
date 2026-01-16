This is a number guessing game. Branches and commits at the time of README creation are listed below. Note: After the tasks, this changed slightly.

Branches:

dev:
    commits: 
        add encouraging message for players
        Initial number guessing game

feature1:
    commits:
        Add version comment documenting quit feature
        Improve user feedback messages for guesses
        Add play-again loop functionality
        Add ability to quit game with negative number input
        (main) Initial Number guessing game

feature2:
    commits:
        Implement max attempts logic and game over condition
        Add maxAttempts constant and game over state
        (dev) Add encouraging message for players
        (main) Initial Number guessing game

feature3: 
    commits:
        (HEAD -> feature3, documentaion) done
        had to fix
        got it done
        started hint
        (main) Initial Number guessing game

hotfix:
    commits:
        Fix randomInt to properly include max value in range
        (main) Initial Number guessing game

main:
    commits: 
        Initial Number guessing game




Learning Summary: 

• Differences between merge, rebase, squash, and cherry-pick

    Merge brings changes from one branch into the current branch. This might result in conflicts if the two branches changed same lines in the code. If this is the case, you need to go into the code (code .), fix the conflicts, stage the changes (git add <file name or file path>), and commit (git commit -m "your message"). It's important to note merge is one-directional. Only the branch where you called git merge receives the combined changes. The other branch remains unchanged. Also, merge preserves exact commit history and branch structure. 

    To my understanding, rebase helps keep commit history linear by moving the current branches commit history on top of another branch. So if I have two branches, dev and feature1, I can call git rebase dev from feature1 and that will move all of feature1's commits on top of dev. So feature1 will have everything that was in dev plus feature1's own commits. Then you can switch to dev and merge with feature1 so that dev also moves up and has the feature1 changes. The biggest difference between merge and rebase is that rebase rewrites commit history so as to make it cleaner and linear. However, this can also be dangerous since old commit hashes are changed with new ones and it should therefore not be used on shared branches. 

    Note: Merge conflicts can be resolved in one go while rebase conflicts might need to be resolved multiple times as there might be multiple commits that introduce conflicts in the commit history. This brings us to squashing. 

    Squash basically combines multiple commits into a single commit. It's useful to squash commits before rebasing to avoid the issue mentioned earlier. This avoids having to resolve the same conflict multiple times in a rebase since there will only be one commit to resolve. 

    Finally, cherry picking is used to apply a SINGLE commit from one branch(usually a quick hotfix) into another branch without bringing in all of the branch's commit history, as a merge would. This is helpful because it allows you to fix a specific problem quickly without introducing unfinished features or other unintended changes. 
    
• What you observed in the git history for feature1 vs feature2 vs feature3

    
• When you would use each strategy in real projects