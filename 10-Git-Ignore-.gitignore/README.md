## Git Ignore and .gitignore

### Git Ignore

When sharing your code with others, there are often files or parts of your project, you do not want to share.

Examples:
- log files
- temporary files
- hidden files
- personal files
- etc.

Git can specify which files or parts of your project should be ignored by Git using a `.gitignore` file.`

Git will not track files and folders specified in `.gitignore`. However, the `.gitignore` file itself IS tracked by Git.

### Create .gitignore

To create a `.gitignore` file, go to the root of your local Git, and create it:

    touch .gitignore

Now open the file using a text editor.

We are just going to add two simple rules:

- Ignore any files with the `.log` extension
- Ignore everything in any directory named `temp`

Now all `.log` files and anything in `temp` folders will be ignored by Git.

**Note**: In this case, we use a single `.gitignore` which applies to the entire repository.

It is also possible to have additional `.gitignore` files in subdirectories. These only apply to files or folders within that directory.

Next Lesson : https://github.com/coderdal/Git-Usage/tree/main/11-Git-Security-SSH#git-security-ssh
