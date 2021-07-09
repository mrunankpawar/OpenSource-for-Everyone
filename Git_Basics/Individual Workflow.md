# Individual Workflow
The workflow from the command line has a few added steps compared to using GitHub. 

- You can clone any repository you have access to using git clone. 
- **Key Terms:**
  - **clone:**  to copy a repository to your computer 
- Then, you create a branch with git branch "name-of-branch". 
- After you make changes, you'll use git add to stage your changes.
- **Key Terms:**
  - **stage:** saving your changes so they are ready to be added to your branch
- You'll use git commit -m "explain your changes" to add changes to your branch.  
- **Command Explanation :**
  - -m is a flag for message. That means that whatever comes after -m is a message explaining your commit. Your commit message doesn't have any effect on your code; it's like a comment. 
- When you're ready to push your local changes to your repository on GitHub, you'll use git push. 
- **Key Terms:**
  - push:  add the changes on your computer to your GitHub repository. 

You might feel a little confused by committing, staging, and pushing your changes. Let's explore a visual representation! 

![MLH Localhost - How to Collaborate with GitHub - Organizer Slides (1)](https://user-images.githubusercontent.com/71369943/125106312-1fcfec80-e0fd-11eb-9ef3-c5232c24832e.png)

Here's another visual representation of what you just saw. 

![MLH Localhost - How to Collaborate with GitHub - Organizer Slides (2)](https://user-images.githubusercontent.com/71369943/125106427-3ece7e80-e0fd-11eb-9990-601be6e3d36d.png)

Great! Let's try it. 

## Create a Repo
Let's create a new repository on GitHub and work with it locally. 

- From your profile or homepage on GitHub, click New.
- Name your repository (repo) whatever you want! We chose hello-world. 
- Write a sentence describing your repo.
- Select Initialize this repository with a README. 
- If this were a code project, you would usually add a .gitignore and/or a license but you don't need to. 
- Click Create repository.  
- You will be redirected to the homepage for your new repository!

## Clone your repo

- Click Clone or download. 
- Then click the clipboard symbol to copy the address of your repo. 
- Back in the terminal, type `git clone` then paste the address of your repo.

![MLH Localhost - How to Collaborate with GitHub - Organizer Slides (3)](https://user-images.githubusercontent.com/71369943/125107127-11360500-e0fe-11eb-9010-651bede01d1b.png)

## Explore Your Repo

It's important to note that you did not simply download the code. You cloned a Git repo. A git repo comes with a special folder called .git. You don't need to know a lot about this folder. Just keep in mind that it connects your local project to the project on GitHub.  

## Let's make a change! 

- Change directory into the repo you cloned by typing the command below.
- **Note:** If you did not name your repo hello-world, you should substitute hello-world with the name of your repo. 
- We're going to make some changes. You never want to commit directly to master, so let's checkout a new branch. You did this in the browser before. Use the command below to create a new branch. 
- Open your project folder in the code editor of your choice. For example, if you have Atom installed, you can use the command below to open the project in Atom. 
- Make any changes you want to your README and save them. 
- Return to your command line. Type the first command below.  You should see output like this. 
  - The output tells us that we have modified the README.md file. At the bottom, it tells us that we have not added any changes to commit. Let's do that now! 
- Type the command below. This command gets your changes ready to be committed. 
- If you enter `git status` again, you will see that now the changes you made to **README.md** are ready to be committed! 
- When you commit changes, you will include a commit message. This message should be descriptive of your changes. It's also a standard practice for your first commit to be "first commit." 
- Now for a cool GitHub trick. We want to push the changes that we have committed up to GitHub. Type `git push`. 
  - Git will tell you the correct command! Copy and paste the command to add your local branch to GitHub and commit your changes. 
- You'll need to enter your GitHub username and password. 
  - **Note:** When typing your password, you won't see anything. 
- Now you can create a pull request in the browser like you did before by going to the URL provided. 
- Select Compare & pull request.
- Name your pull request appropriately, then select Create Pull Request. 
- Finally, because you own the repo, you'll be able to merge your own pull request. 
- Now you want to make sure that your local master branch matches the master branch on GitHub. Return to your terminal and type the command below. 
- Finally, pull the changes on master down to your local repo with the command below. 
- Now you should be able to see your changes in the browser!

& That's it
Now, you are good to work with in your day to day life 🤩
