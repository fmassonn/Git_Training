# Set up your working environment
## Exercise 1 – Git global configuration

First of all you will have to configure git locally in your laptop:

> Of course, you must have git installed. With ubuntu: **sudo apt-get install git**

Open a terminal and run the following git global commands (put your name and email):

```
git config --global user.name "My name"
git config --global user.email "my_mail@uclouvain.be"
git config --global color.ui auto
git config --global core.editor "vim"
git config --global push.default simple
```

## Exercise 2 – Gogs configuration

If it is the first time you try to enter in Gogs click on “Sign-in” and use your classical ELIC login.

After completing this step you will need to ask access to the repositories you want. Send an email to the Gogs administrators of this (these) project(s) asking access to.

## Exercise 3 – Clone into a working environment

To start working you need to create a clone, called afterward “working copy” of the git_tutorial project from Gitlab in your home (or folder of your choice):

```
git clone ssh://git@www.climate.be:3022/TECLIM/Git_Training.git
```

It will ask for your username and password and you will see output like this:

```
Cloning into 'Git_Training'...
remote: Counting objects: 3, done.
remote: Total 3 (delta 0), reused 0 (delta 0)
Unpacking objects: 100% (3/3), done.
Checking connectivity... done.
```

It has created a 'Git_Training' folder and you can browse into it:

```
cd Git_Training
```

Git clone allows you to specify parameters such as the target folder. If you don't specify it the working copy will be named as the project.

Hidden inside a 'working copy' resulting from a git clone there is a special '.git' directory that contains internal objects needed by git.

```
pbarriat@elixir:~/tmp/Git_Training> ls .git/
branches  description  hooks  info  objects      refs
config    HEAD         index  logs  packed-refs
```

It is hidden because you are not supposed to worry at all of internals of '.git'. When you type regular git commands like those in this tutorial, git, transparently writes stuff like indices, references, branch information there.

When you are in a working copy you can use regular unix-like commands such as ls, touch, cp, vi, etc. Additionally you can use whatever git commands, for instance:

#### git status

```
git status
```

The outputs tells you in what branch you are on. By default (if you have not specified in the clone) it clones the master branch.

On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working directory clean

Git status is very important. It's recommendable to use it every now and then to know the status of your branch.

Moreover you can check the history of changes by using git log command:
git log

#### git log

The outputs is a list of what has been changed recently, in reverse chronological order. It tells the author of the change, when it was made and the log message given.

```
commit eab1f5f77cc3c7041f6837ce15172f2be7a650b2
Author: Pierre-Yves Barriat <pierre-yves.barriat@uclouvain.be>
Date:   Fri Dec 4 15:19:11 2015 +0100

    Initial commit for greetings functions

commit 50920a3d04197bd4e52bbfdfdfefc56be23955c6
Author: Pierre-Yves Barriat <pierre-yves.barriat@uclouvain.be>
Date:   Thu Dec 3 19:04:16 2015 +0100

    Add readme
```

