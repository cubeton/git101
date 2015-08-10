# Git 101: Git and GitHub for beginners

Tutorial on git and GitHub for beginners, designed for the [Women Who Code meetup](http://www.meetup.com/Women-Who-Code-Boston/events/224072838/) held on August 12, 2015 at [HubSpot](http://www.hubspot.com). 

Any important git-related words are **bolded**


### Step 1:  Cloning from a remote server to your local machine 

The process of downloading a **repo** from a remote server to your local machine is known as **cloning**.

To clone a repo, first you need to copy the repo's URL as seen below.

<img width="1053" alt="screen shot 2015-08-10 at 3 45 53 pm" src="https://cloud.githubusercontent.com/assets/5241432/9182147/309ee5bc-3f77-11e5-9a62-4db7fbb83485.png">

Move to where you want to place the project. For instance if you have a 'projects' folder on your desktop, you'd do something like 
```cd ~/Desktop/projects```

When you clone a repo, it downloads a brand new folder which contains all the files inside of it (so you don't need to make a specific folder for the project)

Once you're in the location you want to be, in the terminal, use the command:

```git clone https://github.com/cubeton/git101.git```

It should look something like:

![screen shot 2015-08-10 at 3 52 09 pm](https://cloud.githubusercontent.com/assets/5241432/9182329/0e8ee4bc-3f78-11e5-8467-5bf4be3fe914.png)

It may prompt you to log in with your GitHub information.

### Alternative Step 1: Creating a git repo locally on your machine

To start a repository locally, you use cd to folder you want to start the git repository in. 

Later on you can upload your local repository to GitHub or another 

### Step 2: Checking our your project

Now that you have the project on your local machine, you can look at all the files and the changes that have been made to it 

### Step 3: Creating a new branch

### Step 4: Adding a new file

### Step 5: Creating a new commit

### Step 6: Pushing a branch to the GitHub

### Step 7: Creating a Pull Request (PR)

### Step 8: Merging a PR

### Step 9: Cool features: the blame tool


Ever see a piece of completely incomprehensible code? Want to know who to complain to? **Git blame** is here to help!



Unfortunate side effect - I find that half the time when I use the blame tool to see who wrote a terrible piece of code, that it was me :(

### Step 10: A cautionary tale

Git is powerful. Git can do a lot of things. Git can also help you undo most changes and mistakes you've made (see 'reference log' or 'reflog').

There is one thing to keep in mind about git - it has access to your files and can modify them. With the wrong command, you can do really dangerous things. 

When I was starting to learn git, I did not know what I was doing. I used ```git init .``` in my home directory which initializes a git repo and adds all your files in it (recursively). Essentially I had put every file in a git repo.'

Then, when I wanted to undo this I used the ```git rm . -r``` command. This recursively whiped my entire computer. There were some ways to recover it, but.... yeah

Be careful with any 'rm' command.

Learn from my mistake!

### Step 11: Basking in your git glory

Great job!
<img width="500" alt="octocat" src="https://assets-cdn.github.com/images/modules/logos_page/Octocat.png">



