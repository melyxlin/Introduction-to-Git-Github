# Introduction-to-Git-Github
A tutorial/repository for my Introduction to Git/Github workshop for the Spark! Freshmen Mini-Hack and MakeBU
## So...what is Git/Github and why should we use it?
- Presentation: https://docs.google.com/presentation/d/1dzt_jlaK71rOgcexW7Eh1M1N9cXP0PYB3K90Mv_pFOc/edit?usp=sharing
- Animation: 
## Initializing GitHub
### Step 0: Set up Git and GitHub
*Mingle and get into groups of 2+ people. You will do the next steps in groups.*
- Download and install Git [here](https://git-scm.com/)
- Create a GitHub account
### Step 1: Creating a new repository on GitHub
- If you only want to keep track of your code locally, you don't need to use GitHub. But if you want to work with a team, you can use GitHub to collaborate on the project.
1. To create a new repo on GitHub, log in and go to the GitHub home page. You should see a green '+ New repository' button. After clicking the button, fill out the information in boxes and click 'Create Repository' when you are finished
2. GitHub will ask if you want to create a new repo from scratch or if you want to add a repo you have created locally. Since we've already created a new repo locally, we want to push that onto GitHub so follow the '....or push an existing repository from the command line' instructions. 
### Step 2: Cloning the repository
1. Under the repository name, click on button that says **Clone or Download**. 
2. In the **Clone with HTTPs section**, click  to copy the clone URL for the repository.
3. Open Terminal and change to the location where you want the cloned directory to be made.
4. Type `git clone` and then paste the URL you copied. The command should look like this:
```
$ git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY
```
### Step 3: Adding and commiting a new file to the repo
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
- `git status` Asks Git to show you the status of your modified files (how many of them are staged vs. unstaged). This is an optional step.
3. To add a file to a commit, you first need to add it to the staging environment by typing `git add <filename>` or `git add *` (to upload all modified files"
    - If you rerun `git status`, you'll see that git has added the file to the staging environment
4.  To create your first commit:
```
$git commit -m "message about the commit here"
```
- The message at the end of the commit should be something related to what the commit contains. MAKE SURE THAT THE MESSAGE IS MEANINGFUL!
### Step 4: Push the code
- Now we'll **push** the commit in your branch to your new GitHub repo.
    - a **push** allows other people to see the changes you've made. 
1. To push the code on to the GitHub repository
```
$ git push origin [name_of_your_new_branch]
```
-  **_What is "origin"?_** When you initialize a remote repository to your local machine, git creates an **alias** for you. In nearly all cases this alias is called "origin." It's essentially shorthand for the remote repository's URL. 
    - If this is your first time using GitHub locally, it might prompt you to log in with your GitHub username and password.
2. If you refresh the GitHub page, you'll see note saying a branch with your name has just been pushed into the repository. Congratulations, you have just pushed your code!
## What next?
### Step 5: Clone the repository (again)
1. For the other people in the group, go to the main page of the repository and follow step 1 to clone the repository.
### Step 6: Create a branch
1. Before creating a new branch, **ALWAYS PULL** the changes from upstream. Your master on your local branch needs to be up to date.
2. Create the branch on your local machine and switch in this branch :
```
$ git checkout -b [name_of_your_new_branch]
```
3. Now to push the branch to GitHub:
```
$ git push origin [name_of_your_new_branch]
```
- When you want to commit something in your branch, be sure to be in your branch. 
### Step 7: Push content to the repository
1. Now go follow Step 2-4, but **REMEMBER** we are pushing to the **NEW BRANCH** not the `master`
### Step 8: Open a pull request
2. On GitHub, go to the main repository page and click on **New Pull Request**
3. Change the **compare** button to the branch you wish to merge into master
4. Enter a title and description for your pull request. Then click **Create Pull Request** You should now see an open pull request.
- It is important that you do pull request rather than push to master. This is so that people can check over your code before putting in into the master branch and that none of your code will mess up the already written code.
- Github has this check were if tells if a branch is okay to merge. 
5. Once it checks, go ahead on click on **Merge pull request**. You will now see that the code from your branch is added on to the master branch
## Done!
### MORE RESOURCES
- Git Cheatsheet: http://ndpsoftware.com/git-cheatsheet.html#loc=index
- Git Playlist: https://open.spotify.com/playlist/0MJBni0UzdnML1amikx0Rc?si=NlBOzomuQi2pkjzf3SngoA
- Animations: https://onlywei.github.io/explain-git-with-d3/

![Alt Text](https://media.giphy.com/media/xULW8v7LtZrgcaGvC0/giphy.gif)



