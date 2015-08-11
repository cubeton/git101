# Git 101: Git and GitHub for beginners

Tutorial on git and GitHub for beginners, designed for the [Women Who Code meetup](http://www.meetup.com/Women-Who-Code-Boston/events/224072838/) held on August 12, 2015 at [HubSpot](http://www.hubspot.com). 

Any important git-related words are **bolded**

In this tutorial we're going to simulate what it would be like working on a big, collaborative project. This will involve making changes to the code base, opening up a **pull request (PR)** and **merging** your code into the master branch.

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

### Step 2: Checking our your project

Now that you have the project on your local machine, you can look at all the files and the changes that have been made to it. There's a couple things you can check out:

1. The history of the project.
Using the command ```git log``` you can see a list of all the changes made in the project. For instance here is a project that only has one commit so far:

<img width="342" alt="screen shot 2015-08-10 at 10 47 10 pm" src="https://cloud.githubusercontent.com/assets/5241432/9189084/cdffcbc0-3fb1-11e5-9aff-75bb7a4ae89d.png">

2. What branches exist in the project
Using the command ```git branch``` you can see what branches a project contains

<img width="319" alt="screen shot 2015-08-10 at 10 48 40 pm" src="https://cloud.githubusercontent.com/assets/5241432/9189095/f73abbd0-3fb1-11e5-8fac-ab3ef993a43c.png">

In the picture above you can see that this one project has three branches in it. The master branch (which is basically always there), and 'my-new-branch' and 'my-second-cool-feature'.

### Step 3: Creating a new branch

You can create a new branch to base your changes off of. What this will do is make a pointer to the current commit you're out, an start basing your code from those changes.

Let's say you are on the master branch (what you should be automatically), and want to create a new feature. What you do is run ```git checkout -b <my branch name>```. 

Now, if someone makes more changes to the master branch after you've made our branch, your new branch won't know about the changes unless you **merge** those changes into your branch.

So let's try it out!
Run ```git checkout -b <your name>```
What this does is say, "Hey git, I want to create a new branch (that's what the '-b' flag does) and then I want you to move me onto that branch (that's what the 'checkout' does)."

Afterwards you can use the ```git branch``` command to confirm that your branch really was created!

<img width="406" alt="screen shot 2015-08-10 at 10 52 54 pm" src="https://cloud.githubusercontent.com/assets/5241432/9189163/9375ea9c-3fb2-11e5-88e4-249c6ff3cce0.png">
 
You should notice that you're now pointed towards your new branch as well.

### Step 4: Adding a new file to the repo

Go ahead and add a new file to the project. You can use any text editor you like. Name it something like yourname.txt.
Once you add or modify files in a folder that contains a git repo, git notices it. But it won't add the file to a commit unless you tell it to.

After creating the new file, you can use the ```git status``` command to see what files it knows about.

<img width="547" alt="screen shot 2015-08-10 at 10 58 58 pm" src="https://cloud.githubusercontent.com/assets/5241432/9189214/6f61db42-3fb3-11e5-966a-5a7800a582e0.png">

What this is saying above is, 'hey, we noticed you created a new file mnelson.txt, but unless you use the ```git add`` command we aren't going to touch it.'

### Step 5: Creating a commit

Now we're going to tell git that we do want it to care about that file! 

Use the command ```git add <your file name```

What this does is put your file in the staging or index environment. It's saying, 'Hey, we're about to make a commit with this specific file'. This gives you the ability to not commit every single file you've changed.

If you run the ```git status``` command you'll see it looks a little different. Now it's saying that that given file is getting ready to be commited. To clarify, it has **not** yet been put into a commit, but it will be soon!

<img width="384" alt="screen shot 2015-08-10 at 11 08 32 pm" src="https://cloud.githubusercontent.com/assets/5241432/9189304/c2f7a290-3fb4-11e5-9562-23a5bf38cb57.png">

Now we'll make the commit! 
Run the command ```git commit -am "Your message about the commit"```


<img width="508" alt="screen shot 2015-08-10 at 11 17 24 pm" src="https://cloud.githubusercontent.com/assets/5241432/9189408/06e40e84-3fb6-11e5-9397-83ac0ef10736.png">


The message you put at the end of the commit should be something related to what the commit contains - maybe it's a new feature, maybe it's a bug fix, maybe it's just fixing a typo. It shouldn't be something like "asdfadsf" or "foobar". That makes the other people who see your commit sad.

### Step 6: Pushing a branch to the GitHub

### Step 7: Creating a Pull Request (PR)

### Step 8: Merging a PR

### Step 11: Basking in your git glory

Great job!
<img width="500" alt="octocat" src="https://assets-cdn.github.com/images/modules/logos_page/Octocat.png">


### Additional Information

Let's say you want to use git but not use GitHub, or want to start a new project (repo) on your computer locally before puttig on GitHub. Below is the process for creating a local git repository and pushing that repository onto GitHub.

#### Creating a git repo locally on your machine

To start a repository locally, you use ```cd``` to move into the folder you want to start the git repository in. 

Then you use the command
```git init```
which initalizes a repository in that given folder

#### Pushing a repo onto GitHub

Create a local repository using the ```git init``` command and create commits using the ```git add``` and ```git commit``` commands.

Then you can go into GitHub and create a new repository:
<img width="1005" alt="screen shot 2015-08-10 at 10 29 12 pm" src="https://cloud.githubusercontent.com/assets/5241432/9188864/4a7b13c4-3faf-11e5-87fb-a13f31db8803.png">


Once that onilne repository has been created, you can push to it by using the command:
```git remote add origin [remote repository URL]``` where the remote repository URL is the one as seen in Step 1 above.

Once your repo is set to be pushed onto GitHub, run:
```git remote add origin <remote repository URL>``` 

Then run ```git remove -v``` which verifies the remote repository exists

Finally you can push your code using ```git push origin master```


#### Cool features

#### The blame tool

Ever see a piece of completely incomprehensible code? Want to know who to complain to? **Git blame** is here to help!

When you click on a file on GitHub, there's a button that says 'Blame' on the top right:

<img width="952" alt="screen shot 2015-08-10 at 10 40 35 pm" src="https://cloud.githubusercontent.com/assets/5241432/9188987/e3ff9ed8-3fb0-11e5-8919-54b03e8a9119.png">

If you click it, it'll give you something that shows who made the change, and with what commit that changed happen. It can be very useful for debugging things!

<img width="938" alt="screen shot 2015-08-10 at 10 42 38 pm" src="https://cloud.githubusercontent.com/assets/5241432/9189022/25bd1260-3fb1-11e5-9862-47482a42b263.png">


Unfortunate side effect - I find that half the time when I use the blame tool to see who wrote a terrible piece of code, that it was me :(

#### A cautionary tale

Git is powerful. Git can do a lot of things. Git can also help you undo most changes and mistakes you've made (see 'reference log' or 'reflog').

There is one thing to keep in mind about git - it has access to your files and can modify them. With the wrong command, you can do really dangerous things. 

When I was starting to learn git, I did not know what I was doing. I used ```git init .``` in my home directory which initializes a git repo and adds all your files in it (recursively). Essentially I had put every file on my computer in a git repo.

Then, when I wanted to undo this I used the ```git rm . -r``` command. I thought this would only remove the files from git, but it actually recursively deleted all my files. There were some ways to recover from itit, but.... yeah. It was not good.

Be careful with any 'rm' command.

Learn from my mistake!


### Additional Resources

There's a lot of git tutorials out there, but here's some of the better ones:

[Official git site and tutorial](https://git-scm.com/)

[GitHub guides](https://guides.github.com) 

[Commands cheatsheet](https://training.github.com/kit/downloads/github-git-cheat-sheet.pdf)

[Interactive git tutorial](https://try.github.io/levels/1/challenges/1)

[Visual/interactive cheatsheet](http://ndpsoftware.com/git-cheatsheet.html)



