# saturday-test


Before starting with git and github:
  
open the terminal and try out some basic commands: 
try to locate where you are, create a file, rename it and move it to another folder.

  some basic commands:
  help <!-- shows a bunch of commands and definitions-->
  pwd <!-- tells you in which directory(folder) you are in-->
  cd  <!-- change directory. locates you back to the root of your computer-->
  cd filename <!-- just like you would click on a folder to enter it. it moves you up to the folder you type-->
      example:  cd Desktop <!--when you type this, now you are inside the Desktop-->
  ls <!--lists files inside directory you are currently at-->
  open . <!--it opens file in the finder on your computer-->
  cd .. <!--lets you go up one directory-->
  git log <!-- shows history of your commits-->
  ...

  ## Install Git 
  - two ways to install git:

  1. Go to git-scm/download and download the packade you need for your OS
  2. Open terminal and use following commands:
  sudo apt-get update 
  sudo apt-get upgrade
  sudo apt-get install git

  <!-- COMMANDS definition-->
  Sudo <!-- Means: superuser do. allows you to run  programs as a super user, aka root user, which is the most powerful user-->
  apt <!-- Advanced packaging tool. Allows to perfon installation of new software packages-->

  1. check if git is installed on your computer by using the command:
      git <!-- if git is installed you will get a lot of explantion-->
      git --version
  
  ## Configure git

  1. SSH key <!-- this will store pasword of github so you dont have to do it every time you want to push, pull,...-->
  open terminal and use following command to generate a ssh key:
  ssh-keygen -t rsa -b 4096 -C "your_email@example.com"


  ## Use git

  ### from github to git
  you need a repository to use git. 
  A repository is a folder in your local computer.
  On github you also work with repositories.

  1. got to your github account and create a new empty repository
     you can choose to create a readme.md file with it. 
     When you create the repository you create a URL. it can be http or shh.

  2. copy the URL link
  3. open terminal and use command:
      git clone (add url you want to clone) <!-- this will make a copy of the repository on github to your local computer-->
  4. command open . <!--this will open the file or folder you just cloned-->
  5. Make a change in the readme file and save>
  5. command git status
  if you made changes on git and hit save you still need to add and commit it. Use 
  git commit -a -m "message"<!--  commit saves changes and -a tells git to commit all changes and -m "" adds a message to the commit-->

  when you commit for the first time, the terminal will ask you who you are. Use following commands:

  git config --global user.name "your name"
  git config --global user.email "email adress" <!-- use same email as github account-->

  if you want to check if it worked

  git config --list <!-- this lists config settings for git on local computer-->

  if you type 
  git status
  it will make the commit <!--on your local computer, not on github-->

  <!--sometimes you can get into VIM (a terminal based text editor )
  to get out use :q to get out of it-->

#### Push to github

once you commit changes on your local files. you will want to have the same changes to your github repository. use following commands:

git push <!-- if this doesnt work you will have to specify which remote you want to push to on github-->
  git remote <!-- it lists remotes associated with project, usually github calls it origin--> 
  git remo -v <!-- verbose, it will show the url of the remote->
  git origin <!-- this will not be enough, you have to specify which maste-->
  git push origin master <!-- you have to specify in which branch you want to push. for now just use the master branch-->

  ### from git to github

  now we create a repository on the local computer.
  create a folder woth your documents.

  command
  cd (directory you want to want to turn into repository )
  git init <!--turns the folder into git repository-->
  git status<!--it will tell you that you have untracked files-->
  
  <!-- 
  you will have to save the file on file system 
  add the file (it adds the file to a staging area> this comes in handy when you have many changes)
  and commit it to gti
  -->
  git add (filename or folder)
  git commit -m "#"
  git status <!-- it will say "on branch master, nothing to commit..." when the commit succeded-->

  if we want to push to github:
  go to github and create a new empty repository (no readme file)
  command
  git remote add origin ( you dont have to call it origin) 'url of github repository'

  now if you:
  git push origin master <!--it will push the commits to github-->

  

