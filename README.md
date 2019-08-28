# Introduction-to-Git-Github
A tutorial/repository for my Introduction to Git/Github workshop for the Spark! Freshmen Mini-Hack and MakeBU
## So...what is Git/Github and why should we use it?
## Initializing GitHub
### Step 0: Set up Git and GitHub
*Mingle and get into groups of 2+ people. You will do the next steps in groups.*
- Download and install Git [here](https://git-scm.com/)
- Create a GitHub account
### Step 1: Create a local git repository
- When creating a new project on your local machine using git, you'll first create a new repository (a.k.a. *repo*). 
  - This will be done via terminal
1. One member of the team: open up a terminal and move to where you want to place the project on your local machine.
2. Type `git init` to initalize a new local git repository
### Step 2: Adding and commiting a new file to the repo
- Before we begin, here is a few concepts that you need to know:
  - Once you've added or modified files in a folder containing a git repo, git will notice that changes have been made inside the repo. But, git won't officially keep track of the file, unless explicitly told to (i.e. a commit)
  - A **commit** takes all currently-staged files and creates a new snapshot in time of your repository that includes modified files
    -  commits makes up essence of your project and allow you to go back to the state of a project at any point.
  - To tell git which files to put into a commit, you must you first need to add it to the staging environment. This tells Git that you would like to have a particular modified file or all modified files to be uploaded
  
1. Go ahead and add a new file to the project via your favorite text editor or the `touch` command.
2. After creating the file, type `git status` to see which files git knows exist.
    - `git status` Asks Git to show you the status of your modified files (how many of them are staged vs. unstaged). This is an optional step.
3. To add a file to a commit, you first need to add it to the staging environment by typing `git add <filename>` or or `git add *`
    - If you rerun `git status`, you'll see that git has added the file to the staging environment
4.  To create your first commit, type `git commit -m "message about the commit here"
    - The message at the end of the commit should be something related to what the commit contains. MAKE SURE THAT THE MESSAGE IS MEANINGFUL!
### Step 3: Creating a new repository on GitHub
- If you only want to keep track of your code locally, you don't need to use GitHub. But if you want to work with a team, you can use GitHub to collaborate on the project.
1. To create a new repo on GitHub, log in and go to the GitHub home page. You should see a green '+ New repository' button. After clicking the button, fill out the information in boxes and click 'Create Repository' when you are finished
2. GitHub will ask if you want to create a new repo from scratch or if you want to add a repo you have created locally. Since we've already created a new repo locally, we want to push that onto GitHub so follow the '....or push an existing repository from the command line' instructions. 
### Step 4: Push the code
- Now we'll **push** the commit in your branch to your new GitHub repo.
    - a **push** allows other people to see the changes you've made. 
1. Type `git push origin master` to push the code on to the GitHub repository
    -  **_What is "origin"?_** When you initialize a remote repository to your local machine, git creates an **alias** for you. In nearly all cases this alias is called "origin." It's essentially shorthand for the remote repository's URL. 
    - If this is your first time using GitHub locally, it might prompt you to log in with your GitHub username and password.
2. If you refresh the GitHub page, you'll see note saying a branch with your name has just been pushed into the repository. Congratulations, you have just pushed your code!
## What next?
### Step 5: Clone the repo
### Step 6: Create a branch
### Step 7: Push content to the repository
### Step 8: Open a pull request
## Done!




