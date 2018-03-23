# Git_Training

## Purpose

The Git Training session started with a lesson of basics on Git and collaborative development. You can find the presentation [here](https://github.com/fmassonn/Git_Training/tree/master/slides/Git_ELIC.pdf).

The second part of the Git Training consists on a hands on. The objectives are to show how to use:

- Git on the command line OR TortoiseGit with Windows
- Gogs portal

We are going to do some exercises in a dummy project that you can find in this common Gogs [repository](https://github.com/fmassonn/Git_Training/tree/master/project).

## Getting started

First you may need to install the Git command-line tools.

### Linux

- With ubuntu: `sudo apt install git`
- With centos: `sudo yum install git`
- With suse: `sudo zypper --non-interactive install git`

Prepare your environment for the first use of Git.

For instance:

```
git config --global user.name "My name"
git config --global user.email "my_mail@uclouvain.be"
git config --global color.ui auto
git config --global color.diff auto
git config --global color.status auto
git config --global color.branch auto
git config --global core.editor "vim"
git config --global push.default simple
```

Clone the Git_Training repository

For instance:

```
[ ! -f ~/.ssh/id_rsa.pub ] && ssh-keygen -t rsa
cat ~/.ssh/id_rsa.pub | xclip -sel clip
```
1. Go to https://www.elic.ucl.ac.be/user/settings/ssh, 
2. click on the 'Add Key' button, 
3. enter the Key Name you want, 
4. and finally do a 'CTRL-V' in Content. 

And now:
```
git clone ssh://git@www.climate.be:3022/TECLIM/Git_Training.git
```

### Windows or Mac

[Download and Install Git](https://github.com/fmassonn/Git_Training/tree/master/resources/README.md)

Clone the Git_Training repository:

```
https://github.com/fmassonn/Git_Training.git
```

For instance, paste the URL into TortoiseGit and it will clone the repo locally on your computer:

![6.png](https://github.com/fmassonn/Git_Training/raw/master/resources/6.png)

## Tips and Tricks

#### How do I add an empty directory to a Git repository ?

 You can't. The design of the Git staging area only accounts for files (see below for the workaround).
 
#### And if I need an empty folder anyway ?

The solution to this Git empty directory problem is a simple workaround: just create a placeholder file in your empty Git directories to convince Git to put the empty directory into your Git repository. For instance:
 ```
touch .gitkeep
 ```
 
#### Git Auto-Completion

If you use the Bash shell, Git comes with a nice auto-completion script you can enable. Download it directly from the Git source code at https://github.com/git/git/blob/master/contrib/completion/git-completion.bash. Copy this file to your home directory, and add this to your ```.bashrc``` file:
 ```
source ~/git-completion.bash
 ```

In the same time, the following script allows you to see repository status in your prompt. Download it directly from the Git source code at https://github.com/git/git/blob/master/contrib/completion/git-prompt.sh. Copy this file to your home directory, and add this to your ```.bashrc``` file:
 ```
source ~/git-prompt.sh
PS1=$PS1'$(__git_ps1 "\[\e[0;32m\](%s) \[\e[0m\]")'
 ```


#### git-config

Tell Git which whitespace problems it should recognize, namely any whitespace at the end of a line, as well as mixed spaces and tabs:

 ```
git config --global core.whitespace trailing-space,space-before-tab
 ```
 
#### gitignore

You don’t want to commit all your files into your repository. Things like temporary files, logs, configurations that are specific to a computer, files that are for testing only, private keys for code signing or files that can be easily regenerated all don’t belong in your repository. However, they will still show up whenever you type ```git status```, even though they are purely noise at that point.

For this reason you can specify what files you want Git to ignore in a special file called ```.gitignore```. Placed at the root of the repository, it contains glob patterns specifying all the files you want Git to ignore. Any file (and directory) matched by these globs won’t show up in git status, and if you try to add them via ```git add```, Git will refuse to do so (you can still add them by specifying the ```-f``` flag when adding).

For example, Rails 3 projects use the following ```.gitignore by``` default:
```
.bundle
db/*.sqlite3
log/*.log
tmp/
```

This tells Git to ignore the ```.bundle``` directory, all files ending in ```.sqlite3``` in the db directory, all the logs in ```log```, and everything in the ```tmp``` directory.

#### Using an external diff viewer

The built-in diff viewer is great most of the time, but sometimes you want to diff non-text files, or simply need a better visualization of what’s going on.

For this reason, Git allows you to specify external diff viewers. For instance:
```
git config diff.tool vimdiff
```
Then, when you want to diff, just use ```git difftool``` instead of ```git diff```. It will work as you expect.

## Additional resources

[Git cheat sheet](https://github.com/fmassonn/Git_Training/tree/master/resources)

[Windows or MAC OS X](https://github.com/fmassonn/Git_Training/tree/master/resources)

[Tricky commands](https://github.com/fmassonn/Git_Training/tree/master/resources/tricky.md)

[Got 15 minutes and want to learn Git?](https://try.github.io)

[Version Control with Git](http://swcarpentry.github.io/git-novice/)

## Contributors

- ELIC members [@pbarriat](https://www.elic.ucl.ac.be/pbarriat)

## References

- http://nuclearsquid.com/writings/git-tricks-tips-workflows/
- [BSC-CNS](https://gateway.bsc.es/dana-na/auth/url_default/welcome.cgi)
- [Consortium des Équipements de Calcul Intensif](http://www.ceci-hpc.be/training.html#versioning)

## License

This project is under the Creative Commons CC0 1.0 Universal License. See the [LICENSE](https://github.com/fmassonn/Git_Training/tree/master/LICENSE) file for the full license text.
