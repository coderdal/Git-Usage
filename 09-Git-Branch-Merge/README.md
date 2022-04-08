## Git Branch Merge

### Merge Branches

We have the emergency fix ready, and so let's merge the master and emergency-fix branches.

First, we need to change to the master branch:

    git checkout master

Now we merge the current branch (master) with emergency-fix:

    git merge emergency-fix

Since the emergency-fix branch came directly from master, and no other changes had been made to master while we were working, Git sees this as a continuation of master. So it can "Fast-forward", just pointing both master and emergency-fix to the same commit.

As master and emergency-fix are essentially the same now, we can delete emergency-fix, as it is no longer needed:

    git branch -d emergency-fix

### Merge Conflict

Now we can move over to hello-world-images and keep working. Add another image file (img_hello_git.jpg) and change index.html, so it shows it:

    git checkout hello-world-images

Now, we are done with our work here and can stage and commit for this branch:

    git add --all

We see that index.html has been changed in both branches. Now we are ready to merge hello-world-images into master. But what will happen to the changes we recently made in master?

    git checkout master

The merge failed, as there is conflict between the versions for index.html. Let us check the status:

    git status

This confirms there is a conflict in index.html, but the image files are ready and stagedto be committed.

So we fixed that conflict. 
Now we can stage index.html and check the status:

    git add index.html
    git status

The conflict has been fixed, and we can use commit to conclude the merge:

    git commit -m "merged with hello-world-images after fixing conflicts"

And delete the hello-world-images branch:

    git branch -d hello-world-images

Now you have a better understanding of how branches and merging works. Time to start working with a remote repository!