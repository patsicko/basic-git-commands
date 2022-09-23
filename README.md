
## BASIC GIT COMMANDS 

Prepared by: MANIBAHO Patrick

*Git* is a version control tool used widely by developers across the world. It helps individual developers keep track of changes as they work on different features in the same project, and helps teams organize their code. 


*A version control system,* or VCS, tracks the history of changes as people and teams collaborate on projects together. As developers make changes to the project, any earlier version of the project can be recovered at any time.
Developers can review project history to find out:
    • Which changes were made?

    • Who made the changes?

    • When were the changes made?

    • Why were changes needed?


GitHub can integrate with Git - it is a web application that allows users to host, explore, and collaborate on code with their teams and the wider developer community.

## Repositories
A repository, or Git project, encompasses the entire collection of files and folders associated with a project, along with each file's revision history. The file history appears as snapshots in time called commits. 

To use Git, developers use specific commands to copy, create, change, and combine code. These commands can be executed directly from the command line or by using an application like GitHub Desktop

`code` : open vs code through terminal
`google-chrome`: Open google chrome using terminal
### Shortcuts
Ctrl +\`: Shortcut to open terminal in vs code

`Ctrl+Q`: Shortcut to close VS code

`Ctrl + C`: close terminal 

`Ctrl+Alt+T`: Opening Terminal

`git init`: This command initializes the repository as a git repository which enables git’s powerful features. Notice that there is a .git directory in the created repository( you may need to enable hidden files to view this folder).
The .git folder is the only difference between a Git repo and an ordinary folder, so deleting it will turn your project back into an unversioned collection of files.


`git branch`: Shows the branches being worked on locally.


`git status`: view the status of a repository.

`git add`: The git add command adds a change in the working directory to the staging area. It tells Git that you want to include updates to a particular file in the next commit. However, git add doesn't really affect the repository in any significant way.
Changes are not actually recorded until you run git commit.
The easiest way to add all files to your Git repository is to use the “git add” command followed by the “-A” option for “all”.

In this case, the new (or untracked), deleted and modified files will be added to your Git staging area. We also say that they will be staged.
Alternatively, you can use the “git add” followed by a “.” which stands for “current directory”. However, using the “.” syntax implies that you are currently at the top of your project folder hierarchy. As a consequence, if you don’t use it at the top of your project hierarchy, you will only add files in the current working directory.


`git add -A`

`git add .`

(At the root of your project folder.)

Commit the Snapshot

A snapshot represents the state of your project at a given point in time.
git commit: Recording the staged snapshot with a descriptive message.


## Commit message template
### A good commit message has three parts:
1. Message title
2. Message body
3. Message footer
The message title starts by type of the task {feat, bug, chore} followed by colon and then a brief description of what changed in that commit, no more than 50 characters, the description must start with a capital letter, and use imperative model. No past, no future, just present tense as imperative model sounds.
You will describe all of changes you made in that commit in the body outlined as tasks, every task is started by a dash and a capital letter. Every task is in imperative mood. Remember that commit is like a small letter that you are communicating to other programmers, so that if they read it, they will undestand what you did in that commit, so try to express well what you have done. Don't hesitate to use techninal terms in it. Since it a message to other programmers, they understand what you want them to know.
The commit message footer, must be inside square bracket, and starts with {Finishes, Delivers}, followed by hash (#) followed by pivotal tracker ID
Note: The head is separated from the body with an empty space, and the body separated from the footer with empty space
## Example of the commit message

feat: User signup

\- Write signup failing test

\- Add signup controller

\- Add signup endpoint

[Finishes#1111111]

![image](https://user-images.githubusercontent.com/63926982/170967321-2a97e357-1c7a-429e-8e5b-cd78b82ac85b.png)



The git status command will only show us uncommitted changes. To view  the history of our project, we need a new command.

`git log`

When you execute this command, Git will output information about our one and only commit, which should look something like this:

![log](https://user-images.githubusercontent.com/63926982/170974127-c123533e-f69a-498f-95aa-eb7e634eb4fd.png)

The commit identified with a very large, very random-looking string *( 3db3351b538d2c9fe1df78ef5292fada3ab395db)* This is a SHA-1 cheksum of a commit’s contents, which ensures that the commit will never be corrupted without Git knowing about it.

Note: In cryptography, *SHA-1* (Secure Hash Algorithm 1) is a cryptographic hash function which takes an input and produces a 160-bit (20-byte) hash value known as a message digest – typically rendered as a hexadecimal number, 40 digits long. It was designed by the United States National Security Agency, and is a U.S. Federal Information Processing Standard.

   ## Configure Git
Before committing any more snapshots, we should probably tell Git who we are, we can do this with the git config command:

![image](https://user-images.githubusercontent.com/63926982/170967560-c837999a-4ed5-430c-892a-09be3889ab71.png)


Remember to replace Your Name and your.email@example.com with your actual name and email.

The -m option in commit command lets you specify a commit message on the command line instead of opening a text editor.
Thus, the commit command will look as follow.

git commit -m “feat/bug/chore:Title 
                                                  
 -Body(In imperative model) 
              
  [Finishes/Delivers#Pivot tracker]”       

`git merge`: Merges lines of development together. This command is typically used to combine changes made on two distinct branches. For example, a developer would merge when they want to combine changes from a feature branch into the main branch for deployment.

`git push`: updates the remote repository with any commits made locally to a branch.


 `git clone`: Creates a local copy of a project that already exists remotely. The clone includes all the project's files, history, and branches.

## How you can clone a remote repository

Login into  your *Github* account and go to Repository. Go to New on upper right corner.


                           

![image](https://user-images.githubusercontent.com/63926982/170967747-b465a535-cd7b-4849-b223-4f2c06fbcdd0.png)


![image](https://user-images.githubusercontent.com/63926982/170967935-2233607b-4e4c-42b6-8c3a-7d050210f494.png)




### Input Repository name 

For more information about the best practices for naming a git repository, go to 
[Nezago guidelines](https://github.com/nezago/nezago-guidelines/wiki/Convetions-and-bestpractices-used-at-nezago)

Add a README file and Create repository

When a repository is successfully created, you can clone it on your local computer.


![image](https://user-images.githubusercontent.com/63926982/170968184-70893d63-370e-41ff-8782-a2893fcb8a64.png)



Click on your repository name and on upper right corner, go to code.
Below HTTPS click on copy icon(two papers like image)
![image](https://user-images.githubusercontent.com/63926982/170976221-ddd863b4-d30c-4100-9e31-b033e4a15b3e.png)

  . The link will be immediately copied. Go to your local computer where you want to put a copy of your remote repository.
Open terminal and type git clone and immediately paste the copied link here.

### change into the `repo` directory

`cd repo`

### create a new branch to store any new changes

`git branch my-branch`

### switch to that branch (line of development)

`git checkout my-branch`

### make changes, for example, edit `file1.md` and `file2.md` using the text editor

### stage the changed files

`git add file1.md file2.md`

### take a snapshot of the staging area (anything that's been added)

`git commit -m "my snapshot"`

### push changes to github

`git push --set-upstream origin my-branch`

##Start a new repository and publish it to GitHub

First, you will need to create a new repository on GitHub. For more information, see "[Hello World](https://docs.github.com/en/get-started/quickstart/hello-world)." Do not initialize the repository with a README, .gitignore or License file. This empty repository will await your code.

### create a new directory, and initialize it with git-specific functions

`git init my-repo`

### change into the `my-repo` directory

`cd my-repo`

### create the first file in the project

`touch README.md`

### git isn't aware of the file, stage it

`git add README.md`

### take a snapshot of the staging area

`git commit -m "add README to initial commit"`

### provide the path for the repository you created on github

`git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY-NAME.git`

### push changes to github

`git push --set-upstream origin main`


![image](https://user-images.githubusercontent.com/63926982/170977284-f0f880d7-5f60-4ceb-8cb7-e0a711a951fd.png)

[Rys Git Tutorial.pdf](https://github.com/patsicko/basic-git-commands/files/8886136/Rys.Git.Tutorial.pdf)

[EMACS](/home/patsicko/Desktop/ALX/EMACS DOCUMENTATION.pdf)

