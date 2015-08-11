### Additional Git Techniques For Your Toolbelt

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
