## How do you squash last N commits into a single commit?
To squash the last N commits of the current branch, run the following command (with {N} replaced with the number of commits that you want to squash):

    git rebase -i HEAD~{N}

Upon running this command, an editor will open with a list of these N commit messages, one per line. Each of these lines will begin with the word “pick”. Replacing “pick” with “squash” or “s” will tell Git to combine the commit with the commit before it. 

To combine all N commits into one, set every commit in the list to be squash except the first one. Upon exiting the editor, and if no conflict arises, _git rebase_ will allow you to create a new commit message for the new combined commit.
