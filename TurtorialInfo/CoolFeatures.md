# Cool features

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
