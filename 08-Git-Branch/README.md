## Git Branch

### Working with Git Branches

In Git, a `branch` is a new/separate version of the main repository.

Let's say you have a large project, and you need to update the design on it.

How would that work without and with Git:

Without Git:

- Make copies of all the relevant files to avoid impacting the live version
- Start working with the design and find that code depend on code in other files, that also need to be changed!
- Make copies of the dependant files as well. Making sure that every file dependency references the correct file name
- EMERGENCY! There is an unrelated error somewhere else in the project that needs to be fixed ASAP!
- Save all your files, making a note of the names of the copies you were working on
- Work on the unrelated error and update the code to fix it
- Go back to the design, and finish the work there
- Copy the code or rename the files, so the updated design is on the live version
- (2 weeks later, you realize that the unrelated error was not fixed in the new design version because you copied the files before the fix)

####

With Git:

- With a new branch called new-design, edit the code directly without impacting the main branch
- EMERGENCY! There is an unrelated error somewhere else in the project that needs to be fixed ASAP!
- Create a new branch from the main project called small-error-fix
- Fix the unrelated error and merge the small-error-fix branch with the main branch
- You go back to the new-design branch, and finish the work there
- Merge the new-design branch with main (getting alerted to the small error fix that you were missing)

Branches allow you to work on different parts of a project without impacting the main branch.

When the work is complete, a branch can be merged with the main project.

You can even switch between branches and work on different projects without them interfering with each other.

Branching in Git is very lightweight and fast!

### New Git Branch

Let add some new features to our `index.html` page.

We are working in our local repository, and we do not want to disturb or possibly wreck the main project.

So we create a new `branch`:

    git branch hello-world-images

Now we created a new `branch` called "`hello-world-images`"

Let's confirm that we have created a new `branch`:

    git branch

We can see the new branch with the name "hello-world-images", but the `*` beside `master` specifies that we are currently on that `branch`.

`checkout` is the command used to check out a `branch`. Moving us **from** the current `branch`, **to** the one specified at the end of the command:

    git checkout hello-world-images

Now we have moved our current workspace from the master branch, to the new branch

Open your favourite editor and make some changes.

For this example, we added an image (img_hello_world.jpg) to the working folder and a line of code in the `index.html` file.

We have made changes to a file and added a new file in the working directory (same directory as the `main` `branch`).`

Now check the status of the current branch:

    git status

So let's go through what happens here:

- There are changes to our index.html, but the file is not staged for `commit`
- `img_hello_world.jpg` is not `tracked`

So we need to add both files to the Staging Environment for this `branch`:

    git add --all

Using `--all` instead of individual filenames will **Stage** all changed (new, modified, and deleted) files.

Check the `status` of the `branch`:

    git status

We are happy with our changes. So we will commit them to the `branch`:

    git commit -m "Added image to Hello World"

Now we have a new `branch`, that is different from the master `branch`.

###
**Note:** Using the -b option on checkout will create a new branch, and move to it, if it does not exist.
###

Next Lesson : https://github.com/coderdal/Git-Usage/tree/main/09-Git-Branch-Merge#git-branch-merge
