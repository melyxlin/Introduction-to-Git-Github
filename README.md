# Introduction-to-Git-Github
A tutorial/repository for my Introduction to Git/Github workshop for the Spark! Freshmen Mini-Hack and MakeBU
## So...what is Git/Github and why should we use it?
- Presentation: https://docs.google.com/presentation/d/1dzt_jlaK71rOgcexW7Eh1M1N9cXP0PYB3K90Mv_pFOc/edit?usp=sharing
- Animation: 
## Initializing GitHub
### Step 0: Configuring Git and GitHub
*Mingle and get into groups of 2+ people. You will do the next steps in groups.*
- Download and install Git [here](https://git-scm.com/)
- Create a GitHub account
-  Now that we've installed git on our computer, we will need to add some quick configurations, particularly with our username and email. 
```
$ config --global user.name "My Name"
$ config --global user.email myEmail@example.com
```
Every action we do in Git will now have a stamp with our name and address on it. This way users always know who did what and everything is way more organized.
### Step 1: Initializing a git repository
- Git stores its files and history directly as a folder in your project. To set up a new repository, we need to open a terminal, navigate to our project directory and run
```
$ git init
```
The command line should response should be:
```
$ Initialized empty Git repository in /home/user/Desktop/git_exercise/.git/
```
Which means that our repo has been successfully created but is still empty.
### Step 2: Adding and commiting a new file to the repo
- Before we begin, here is a few concepts that you need to know:
  - Once you've added or modified files in a folder containing a git repo, git will notice that changes have been made inside the repo. But, git won't officially keep track of the file, unless explicitly told to (i.e. a commit)
  - A **commit** takes all currently-staged files and creates a new snapshot in time of your repository that includes modified files
    -  commits makes up essence of your project and allow you to go back to the state of a project at any point.
  - To tell git which files to put into a commit, you must you first need to add it to the staging environment. This tells Git that you would like to have a particular modified file or all modified files to be uploaded
  
1. Go ahead and add a new file to the project via your favorite text editor or the `touch` command.
2. After creating the file, to see which files git knows exist, type
```
$ git status
```
- `git status` Asks Git to show you the status of your modified files (how many of them are staged vs. unstaged). This is an optional step (but highly recommended).
3. To add a file to a commit, you first need to add it to the staging environment by typing `git add <filename>` or `git add *` (to upload all modified files)
    - If you rerun `git status`, you'll see that git has added the file to the staging environment
4.  To create your first commit:
```
$git commit -m "message about the commit here"
```
- The message at the end of the commit should be something related to what the commit contains. MAKE SURE THAT THE MESSAGE IS MEANINGFUL!
### Step 3: Creating a new repository on GitHub
- If you only want to keep track of your code locally, you don't need to use GitHub. But if you want to work with a team, you can use GitHub to collaborate on the project.
1. To create a new repo on GitHub, log in and go to the GitHub home page. You should see a green '+ New repository' button. After clicking the button, fill out the information in boxes and click 'Create Repository' when you are finished.
2. GitHub will ask if you want to create a new repo from scratch or if you want to add a repo you have created locally. Since we've already created a new repo locally, we want to push that onto GitHub so follow the '....or push an existing repository from the command line' instructions.
### Step 4: Push the code
- Now we'll **push** the commit to Git.
    - a **push** allows other code to be saved to Git. 
1. To push the code on to the Git, we first have to link the GitHub repository to your local Git environment. Go to your
```
$ git push origin master
```
-  **_What is "origin"?_** When you initialize a remote repository to your local machine, git creates an **alias** for you. In nearly all cases this alias is called "origin." It's essentially shorthand for the remote repository's URL. 
    - If this is your first time using GitHub locally, it might prompt you to log in with your GitHub username and password.
2. If you refresh the GitHub page, you'll see note saying a branch with your name has just been pushed into the repository. 
### Step 6: Create a README
A README is a file that describes the functionaity of the project, tech stack, etc. Its highly recommended that you create one so that people viewing your project can understand the intent and tech behind it. 
1. On your github repository page, there will be an area that something like "initialize a README". Click on that button, and edit the text screen to say whatever you like. This is what your README will be. Then commit changes (and add a message while you are at it)
### Step 7: Pulling the code
So, now that you have a created a README file, you have a new file on your GitHub, but it is not on your local repository. 
1. Go to the terminal and run
```
$ git fetch origin master
```
The run 
```
$ git pull origin master
```
This get the README from the project. Now you will have it in your own repository!
## Done!
### MORE RESOURCES
- Git Cheatsheet: http://ndpsoftware.com/git-cheatsheet.html#loc=index
- Git Playlist: https://open.spotify.com/playlist/0MJBni0UzdnML1amikx0Rc?si=NlBOzomuQi2pkjzf3SngoA
- Animations: https://onlywei.github.io/explain-git-with-d3/

![Alt Text](https://media.giphy.com/media/xULW8v7LtZrgcaGvC0/giphy.gif)



