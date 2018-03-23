# Set up your working environment

## Exercise 1 – Git global configuration and Github configuration

First of all you will have to configure git locally in your desktop:

You must have git installed. See the instructions [here](https://github.com/fmassonn/Git_Training/tree/master/resources/README.md)

Then, go to [https://github.com/](https://github.com/) and "Sign-in" (or "Sign up" if you don't have a valid Github account).

When your account is created, let us know about your username by sending an e-mail. This allow us to grant you access to the files that we will work on during the training.

## Exercise 2 – Clone the project, play around and experiment

To start working you need to create a clone, called afterward “working copy” of the Git_Training project from Github in your home.

Right click in the Windows desktop. From the drop-down menu, look for TortoiseGit then "clone". Copy-paste the URL of the project (https://github.com/fmassonn/Git_Training.git) and clone it.

![6.png](https://github.com/fmassonn/Git_Training/raw/master/resources/6.png)

Enter the folder that has been created, and go to `./project/windows`. There you will find an HTML page named `twenty-five.html`. Visualize it with any browser.

#### git tips

Hidden inside a 'working copy' resulting from a git clone there is a special '.git' directory that contains internal objects needed by git.

```
branches  description  hooks  info  objects      refs
config    HEAD         index  logs  packed-refs
```

It is hidden because you are not supposed to worry at all of internals of '.git'. When you type regular git commands like those in this tutorial, git, transparently writes stuff like indices, references, branch information there.

When you are in a working copy you can use regular windows operations such as create file/folder, copy/paste, etc. Additionally you can use whatever git commands.
