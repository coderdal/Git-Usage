## Git Commit

*Since we have finished our work, we are ready move from `stage` to `commit` for our repo.*

Adding commits keep track of our progress and changes as we work. Git considers each `commit` change point or "save point". It is a point in the project you can go back to if you find a bug, or want to make a change.

When we `commit`, we should **always** include a **message**.

By adding clear messages to each `commit`, it is easy for yourself (and others) to see what has changed and when.


    git commit -m "First release of Hello World!"

The `commit` command performs a commit, and the `-m "example message"` adds a message.

The Staging Environment has been committed to our repo, with the message:
"First release of Hello World!"

### Git Commit without Stage

Sometimes, when you make small changes, using the staging environment seems like a waste of time. It is possible to commit changes directly, skipping the staging environment. The `-a` option will automatically stage every changed, already tracked file.

Let's add a small update to index.html.

And check the status of our repository. But this time, we will use the `--short` option to see the changes in a more compact way:

    git status --short

###

**Note:** Short status flags are:
- **??** - Untracked files
- **A** - Files added to stage
- **M** - Modified files
- **D** - Deleted files

###

We see the file we expected is modified. So let's commit it directly:

    git commit -a -m "Updated index.html with a new line"

###

**Warning:** Skipping the Staging Environment is not generally recommended.

Skipping the stage step can sometimes make you include unwanted changes.
