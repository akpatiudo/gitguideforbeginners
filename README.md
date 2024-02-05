![image](https://github.com/akpatiudo/gitguideforbeginners/assets/118566096/ef6bcebe-de92-48fe-8d60-eb895892ddab)

# Beginner's Guide to Git and Version Control

## Introduction:
Version control is a critical aspect of modern software development, enabling developers to collaborate effectively, track changes, and manage codebases efficiently. Simply put, Version control is a system that records changes to a set of files over time so that you can track specific versions later. Git is one of the most popular version control systems used by developers worldwide. This beginner's guide will walk you through the basics of Git, from installation to common commands, helping you kickstart your journey with version control. GitHub and GitLab are online servers and websites that are used to store code with Git online.

## Installing Git on Windows, macOS, and Linux:
- **Linux:** Install the program from the terminal with the command: `sudo apt-get install git`
- **Windows:** Download the Windows tool [here](https://git-scm.com/downloads)
- **Mac:** Download the macOS tool [here](https://git-scm.com/downloads)

## Your Identity Setup:
The first thing you should do when you install Git is to set your user name and email address. This is important because every Git commit uses this information, marking your activity specifically to the Git repository. You can set your identity using the following commands:

git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"

If the --global option is used, you only need to set up your identity once. However, if you want to override this with a different name or email address for specific projects, you can run the command without the --global option when you’re in that project.

## Common Git Commands:
One of the most used commands in Git is git clone. This command allows you to get code that is online onto your local machine. You don’t have to initialize the repository when you clone, but if you are to start building from scratch, you will have to initialize a Git repository on your local machine.

cd desktop  this will put your directory on your desktop

git clone https://github.com/akpatiudo/dotnetdevops

![image](https://github.com/akpatiudo/gitguideforbeginners/assets/118566096/bad7527c-d271-4df4-b48a-57de98a9181f)

cd dotnetdevops/     this gets you into the working directory 

ll      calls up the content of the dotnetdevops repository

![image](https://github.com/akpatiudo/gitguideforbeginners/assets/118566096/0923cfc2-6e99-4c6b-9d24-7cc6f83d7658)

If you want to view the contents of a specific file within the Home/ directory, you can use any od these command: "ls, Cat nano or vi"

ls Views/  This command will list the files and directories inside the Views/ directory.

![image](https://github.com/akpatiudo/gitguideforbeginners/assets/118566096/a8f2dde6-fbf0-44a2-b3e9-45a52f713a2e)

ls Views/Home/  This command will list the files inside the Home/ directory.

![image](https://github.com/akpatiudo/gitguideforbeginners/assets/118566096/72e9b3fd-101c-4be9-88e9-153b63d4ac59)

Alternatively, if you just want to quickly view the contents of a file without editing it, you can use the cat command: cat Views/Home/index.cshtml, however, if  vi Views/Home/Index.cshtml command is used. you will have to Press i to enter insert mode and start editing the file. Press Esc to exit insert mode and return to command mode

nano Views/Index.cshtml if you want to view the contents of a file named index.cshtml

![image](https://github.com/akpatiudo/gitguideforbeginners/assets/118566096/686e931b-e0ce-4a27-9904-4e518d322f86)

## Git Branch

It is a good practice to work on your branch this we ensure quality control of the codebase, each branch is a version of the software and when a branch is affected it will not affect the whole code base. to start my editing I will first create a branch.

git branch featuredotnet01:  Creates a new branch named featuredotnet01

![image](https://github.com/akpatiudo/gitguideforbeginners/assets/118566096/853ec30c-8cf3-48bd-b101-62957fba272c)

git checkout featuredotnet01:  Switches to the  featuredotnet01 branch.

![image](https://github.com/akpatiudo/gitguideforbeginners/assets/118566096/20d9291d-140e-4333-a347-34a110a0a1bf)

## Edithing and Uploading Using Git

When you edith your code you are in the process of improving the version of your softwere, this improvment is what births a new version of the software and when you upload using Git, a new version of the software is added to the history of the project that can be used to revert to, keep track of changes, and many other things.

nano Views/Home/Index.cshtml

![image](https://github.com/akpatiudo/gitguideforbeginners/assets/118566096/b64af836-2da5-415b-92e1-f924dd88c03a)

I want to edith the h1 to h3 block of the index.cshtml file,  for h1. I will increase  font-size: 2.5rem;  margin-bottom: 20px; I will do same to h2 and h3 which you will see later line 109

Use Ctrl + O to save the changes.   Use Enter to confirm.      Use Ctrl + X to exit Nano.

git add  Index.cshtml   this will add the file to be uploaded if it is more than one files you use git add .

![image](https://github.com/akpatiudo/gitguideforbeginners/assets/118566096/adbcd706-d0d6-49ca-b5c2-b6b026e19cae)

git commit -m"index.cshtml file, block h1 to h3 was updated"     this describe what change has been made

![image](https://github.com/akpatiudo/gitguideforbeginners/assets/118566096/06a76239-d09d-4a40-b8e5-d2d5fa406ba6)

A file was change and 12 insertion was made

By pushing your branch working branch before merging to master or main, all you are doing is updating the remote's knowledge of which commit the working branch should be pointing to. If you merge to master and then push only master, the remote's copy of the working branch won't be updated

git push origin main

![image](https://github.com/akpatiudo/gitguideforbeginners/assets/118566096/88d7a7ef-5ef7-4d65-abd4-a5148c62e02b)

The command git push origin main is used to push your local changes to the remote repository's main branch. Here's what each part of the command does:
git push: This command is used to upload local repository content to a remote repository.
origin: This is the name of the remote repository where you want to push your changes. origin is the default name Git gives to the remote repository from which the local repository was cloned.

## Git Merge
Git merge is a command that combines two or more development histories (branches). You can encounter it when deciding to merge some experimental branch back into the main branch, To merge two branches, first checkout the branch you want to merge into, then merge in the other branch

git checkout main

![image](https://github.com/akpatiudo/gitguideforbeginners/assets/118566096/d02afd8f-cfbc-4e8d-823a-dc1175fd1c8c)

git merge featuredotnet01  this will merge the featuredotnet01 branch into main

![image](https://github.com/akpatiudo/gitguideforbeginners/assets/118566096/8e4a7eb5-7c34-46cf-956f-a70e09564178)

git show fd0fe3c..6ff0eecthis shows the activies that was commited with that commit id 

![image](https://github.com/akpatiudo/gitguideforbeginners/assets/118566096/2a312faf-f186-4d46-9cb7-a2167a562cd1)

## Push To A New Repository

First, create a new empty repository on GitHub where you want to push your Git work. Make sure not to initialize it with a README, license, or .gitignore file, as these may conflict with your existing repository.

git remote set-url origin <new_repository_url>

git remote set-url origin https://github.com/akpatiudo/gitguideforbeginners.git

git push origin main

![image](https://github.com/akpatiudo/gitguideforbeginners/assets/118566096/61abcecb-5892-4f76-bcfa-4132c6016212)


git log   is the history log of all the commit that has ben carried out
![image](https://github.com/akpatiudo/gitguideforbeginners/assets/118566096/175b4acf-c857-489f-a8a3-f68c9db1f653)

## Viewing Git Diffs 
To see the changes you've made to your files before committing them, you can use the git diff command.

## Git Hooks
Git hooks are scripts that Git executes before or after events such as commit, push, and receive. You can create custom hooks to automate tasks or enforce policies in your Git workflow. To create Git hooks, you can add executable scripts to the .git/hooks directory in your Git repository.

## Things to Note

This work is just a guide for beginners it is not in any way to exhaust all git command, below is some of the command you might find handle 
To see which remote servers you have configured, you can run the git remote command. git remote, If you’ve cloned your repository, you should at
least see *origin* however, if you specify -v, it shows you  the URLs that Git has stored for the shortname to be used
when reading and writing to that remote:

git remote -v

![image](https://github.com/akpatiudo/gitguideforbeginners/assets/118566096/beb55f55-1655-4192-a770-889461ef28fc)

git branch -d   featuredotnet01      Deletes the  featuredotnet01 branch.

git branch -m   feature-B Renames the current branch (featuredotnet01) to feature-B.

git branch -a   Lists all local and remote branches.

git branch -b    featuredotnet01: Creates and switches to a new branch named  featuredotnet01.

git mkdir amazonbooks  will create a new directory

git init   will initialize your working repository

touch index.html    will create the file index.html

git status        Check the Status of the Git Repository

git remote add origin url     Link the Local Repository to a Remote Repository 

If you encounter merge conflicts during a merge operation, Git provides a merge tool to help resolve them. You can invoke the merge tool using

git mergetool -t vimdiff

rm -findex.html .orig    this will remove the  backup files created by the merge tool

sudo git config --list    it will list your Git configuration

vi ~/.gitconfig       This will open the .gitconfig file in the Vim text editor



:wq and Enter: This command in Vim saves changes to the file and exits the editor, it puts Vim in command mode, w stands for write (save), and q stands for quit. So, :wq means write changes and quit.

:q!: This command in Vim quits the editor without saving any changes. The : puts Vim in command mode, q stands for quit, and ! forces the command, ignoring any warnings about unsaved changes. So, :q! means quit without saving changes.

## Conclusion:
Congratulations! You have completed the beginner's guide to Git and version control. By following this guide, you have learned the fundamentals of Git, including installation, identity setup, common commands, and branching. You now have the skills to start managing your projects effectively using Git.

Remember, version control is an essential tool for every developer, enabling collaboration, tracking changes, and managing codebases efficiently. Whether you're working on personal projects or collaborating with a team, Git empowers you to keep track of your code's history and seamlessly work on multiple features simultaneously.

Continue exploring Git and version control to deepen your understanding and discover advanced features that suit your workflow. With practice and experience, you'll become proficient in using Git to streamline your development process and contribute to successful projects.

Happy coding!













