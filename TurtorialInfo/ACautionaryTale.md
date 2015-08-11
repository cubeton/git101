# A cautionary tale

Git is powerful. Git can do a lot of things. Git can also help you undo most changes and mistakes you've made (see 'reference log' or 'reflog').

There is one thing to keep in mind about git - it has access to your files and can modify them. With the wrong command, you can do really dangerous things. 

When I was starting to learn git, I did not know what I was doing. I used ```git init .``` in my home directory which initializes a git repo and adds all your files in it (recursively). Essentially I had put every file on my computer in a git repo.

Then, when I wanted to undo this I used the ```git rm . -r``` command. I thought this would only remove the files from git, but it actually recursively deleted all my files. There were some ways to recover from it, but... it was not good.

Be careful with any 'rm' command.

Learn from my mistake!
