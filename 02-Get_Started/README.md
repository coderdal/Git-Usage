## Get Started

*To start using Git, we are first going to open up our Command shell.*

*For Windows, you can use Git bash, which comes included in Git for Windows. For Mac and Linux you can use the built-in terminal.*

*The first thing we need to do, is to check if Git is properly installed:*

    git --version

If Git is installed, it should show something like `git version X.Y`

## Using Git with Command Line

### Configure Git

*Now let Git know who you are. This is important for version control systems, as each Git commit uses this information:*

    git config --global user.name "coderdal"
    git config --global user.email "test@coderdal.com"

Change the user name and e-mail address to your own. You will probably also want to use this when registering to GitHub later on.

**Note:** Use global to set the username and e-mail for every repository on your computer.

If you want to set the username/e-mail for just the current repo, you can remove `--global`

Next Lesson : https://github.com/coderdal/Git-Usage/tree/main/03-Create-Initialize