## Git Adding New Files

*You just created your first local Git repo. But it is empty.*

*So let's add some files, or create a new file using your favourite text editor. Then save or move it to the folder you just created.*

I will create an `index.html` file for this example.

Let's go back to the terminal and list the files in our current working directory:

    ls

`ls` will list the files in the directory. We can see that index.html is there.

Then we check the Git status and see if it is a part of our repo:

    git status

Now Git is aware of the file, but has not added it to our repository!

### File states

Files in your Git repository folder can be in one of 2 states:

- Tracked - files that Git knows about and are added to the repository
- Untracked - files that are in your working directory, but not added to the repository
 
When you first add files to an empty repository, they are all untracked. To get Git to track them, you need to stage them, or add them to the staging environment.

I will cover the staging environment in the next chapter.

Next Lesson : https://github.com/coderdal/Git-Usage/tree/main/05-Staging-Environment#git-staging-environment
