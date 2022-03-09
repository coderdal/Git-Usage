## Git Staging Environment

*One of the core functions of Git is the concepts of the Staging Environment, and the Commit.*

*As you are working, you may be adding, editing and removing files. But whenever you hit a milestone or finish a part of the work, you should add the files to a Staging Environment.*

**Staged** files are files that are ready to be **committed** to the repository you are working on. You will learn more about `commit` shortly.

For now, we are done working with index.html. So we can add it to the Staging Environment:

    git add index.html

The file should be **Staged**. Let's check:

    git status

Now the file has been added to the Staging Environment.

### Git Add More than One File

You can also stage more than one file at a time. Let's add 2 more files to our working folder. Use the text editor again.

A **README.md** file that describes the repository (recommended for all repositories).

A basic external style sheet **bluestyle.css**.

And update **index.html** to include the stylesheet.

Now add all files in the current directory to the Staging Environment:

    git add --all

Using --all instead of individual filenames will stage all changes (new, modified, and deleted) files.

Let's check status again:

    git status

Now all 3 files are added to the Staging Environment, and we are ready to do our first `commit`.

**Note:** The shorthand command for `git add --all` is `git add -A`

Next Lesson : https://github.com/coderdal/Git-Usage/tree/main/06-Git-Commit#git-commit
