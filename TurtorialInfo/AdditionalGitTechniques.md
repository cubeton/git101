# Additional Git Techniques For Your Toolbelt

Let's say you want to use git but not use GitHub, or want to start a new project (repo) on your computer locally before puttig on GitHub. Below is the process for creating a local git repository and pushing that repository onto GitHub.

### Creating a git repo locally on your machine

To start a repository locally, you use ```cd``` to move into the folder you want to start the git repository in. 

Then you use the command
```git init```
which initalizes a repository in that given folder

## Pushing a repo onto GitHub

Create a local repository using the ```git init``` command and create commits using the ```git add <your file name>``` and ```git commit -m "your commit message"``` commands.

Helpful tip: If you wanted to add all your changed files to the staging environment, you can use the ```git add .``` command (the period indicates to add all files).

Then you can go into GitHub and create a new repository:
<img width="1005" alt="screen shot 2015-08-10 at 10 29 12 pm" src="https://cloud.githubusercontent.com/assets/5241432/9188864/4a7b13c4-3faf-11e5-87fb-a13f31db8803.png">


Once that online repository has been created, you can push your changes to it by using the command:
```git remote add origin [remote repository URL]``` where the remote repository URL is listed on the new repository page.

Once your repo is set to be pushed onto GitHub, run:
```git remote add origin <remote repository URL>``` 

Then run ```git remove -v``` which verifies the remote repository exists

Finally you can push your code to GitHub using ```git push origin master```

## Merging your changes locally

Let's say you're working on a project completely locally. What do you do if you want to merge a branch locally into master, since you don't have the handy 'Merge pull request' button?

To do this, you'll want to use the ```git merge <branch name>``` command.

Specifically, you want to have git focused on the branch you want to merge _into_. Let's say you have a new feature on a branch named **my_feature** and want to merge it into your master branch. You would want to make sure you're currently pointed on the master branch (you can use the ```git branch``` command to check this out!)

To perform the actual merge, the command you'd want to run is:
```git merge my_feature``` 

## The catch: merge conflicts!

Git is pretty fancy in that it can usually automatically merge files for you. But sometimes it can't!

In these situations, what happens is that multiple people have been working on a specific portion of a file at once. When multiple people modify similar portions of code, you may end up running into a **merge conflict**. When this happens, someone has to manually decide, "Am I going to use their change, or mine?"

A merge conflict will look something like:
```
<<<<<<< HEAD:index.html
<div id="footer">contact : email.support@github.com</div>
=======
<div id="footer">
 please contact us at support@github.com
</div>
>>>>>>> iss53:index.html
```

(code taken from the [Git Book](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging))

In this example, the top portion is saying, "This is what your HEAD looks like." (i.e., what the file looks like on the branch you're currently on. The bottom part is saying "This is what your changes you're trying to merge look like." You'll have to delete a certain portion (up to the ====== part) in order to solve the merge conflict.

When you've fixed the merge conflict and saved the file, you'll need to do ```git add <filename>``` and ```git commit -m "merge conflict"``` to completely finish the merge conflict process.
