# Git_Training

## Tricky commands

Here are a few commands that you may not know yet, or that offer options you haven’t been aware of so far.

### git-stash

```git stash``` is something that can be incredibly handy. What it does is very simple: If you run ```git stash save```, it will take all the changes you have in your working directory and the index, and save them away, leaving you with a clean working directory. Once you’ve done what you wanted to do, you can restore your changes by running ```git stash pop```.

But it gets better: since ```git stash``` saves your changes in a commit, you can stash more than once, and you’ll get a nice list of commits with your stashed changes. ```git stash``` will also keep track of what branch you stashed your changes on, so you’ll know later on what stashed change exactly you want to restore.

```git stash list``` will list all the stashes you’ve saved away, ```git stash apply``` will apply the topmost stashed commit onto your working directory, ```git stash pop``` will also remove the stashed commit in addition to applying it. ```git stash clear``` throws away all your stashes, and ```git stash drop``` allows you to remove a single stash.

### git-rebase

```git rebase``` can be a very tricky command, although its purpose is very simple: Given a range of commits as well as a starting point, it will port the given commits onto that starting point, preserving the commits themselves, but also allowing you to keep a linear history (that is, no merge commit).

Most of the time you’ll give it just one ref: The branch you’ll want your current branch to rebase onto. ```git rebase``` then figures out where those two branches diverged, and use that as the beginning of the commit range. If you pass it a second argument, ```git rebase``` will first switch to that branch before porting your commits.

It also has one very useful flag: ```--interactive```. If you pass this flag, Git will launch your favorite editor with a list of all the commits it is going to rebase. All commits are prefixed with ```pick``` by default, but you can either drop commits entirely (just delete their line), reorder them to your liking, or ```edit``` if you’d like to edit or amend the commit (note that this also allows you to split commits), ```reword``` if you’d just like to change the commit message, and ```squash``` or ```fixup``` if you want to squash the commit with the previous one. ```fixup``` will reuse the previous commit’s message, while ```squash``` allows you to edit the new commit’s message.

The interactive mode is very useful when you’re working on some idea you’ve had, make a commit, and later on realize that it isn’t quite working out that way. You commit a fix, but the commit it fixes is already buried in other commits, so you can’t simply amend. ```git rebase --interactive``` allows you squash those two commits together and make it look like you never made the mistake in the first place.

### git-push

This is a command that you’re probably using often already, but it gained a few more useful options in recent versions:

- ```-u``` or ```--set-upstream```: When doing ```git push <repo> local-branch:remote-branch```, you can use ```-u``` to tell Git to set up ```remote-branch``` as the default upstream branch, so you’ll only need to do ```git push``` in future.
- ```--delete```: Instead of pushing the specified refs, it will instead delete them from the remote repository.

### git-reflog

Whenever an operation changes the tip of a branch, the Reflog mechanism records the old and new locations. ```git reflog``` allows you to access and manage this information.

This is very useful and potentially life saving after any command that (seemingly) changes the history of your repository, like ```git rebase``` or ```git filter-branch```. While these commands do indeed change commits, the old commits aren’t deleted, they are merely unreachable by normal means (This is also the reason why Git will occasionally run ```git gc``` on your repo). However, using the Reflog mechanism you can find out the SHA1’s of these commits, and restore them if you need to.

```git reflog``` lists all the recorded reflog information, and you can then specify any point in the reflog using the syntax ```head@{0}``` (where ```head``` is any kind of ref, and ```0``` to specify the very first reflog entry). For example, if you just did a rebase, but decided that you messed up somehow, you can restore your branch to its state before the rebase by using this command:

```
git reset head@{1}
```
