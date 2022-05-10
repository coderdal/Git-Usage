## Git Amend

### Git commit --amend

`commit --amend` is used to modify the most recent `commit`.

It combines changes in the `staging environment` with the latest `commit`, and creates a new `commit`.
This new `commit` replaces the latest `commit` entirely.


### Git Amend Commit Message

One of the simplest things you can do with `--amend` is to change a `commit` message.

Let's update the `README.md` and `commit`:

    git commit -m "Adding somethings to readme"

Now let's check the log:

    git log --oneline

Oh no! the `commit` message is full of spelling errors. Embarrassing. Let's `amend` that:

    git commit --amend -m "Added lines to README"

And re-check the log:

    git log --oneline

We see the previous `commit` is replaced with our amended one!

# 

**Warning**: Messing with the commit history of a repository can be dangerous. It is usually ok to make these kinds of changes to your own local repository. However, you should avoid making changes that rewrite history to remote repositories, especially if others are working with them.

#

### Git Amend Files

Adding files with `--amend` works the same way as above. Just add them to the `staging environment` before committing.
