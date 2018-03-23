# Review and test others' functions

In this chapter we are going to go through the review and test procedure. You might have received notifications from your colleagues asking to test their branch. So the first you need to do is to checkout their branch.

To know what branches are available you can use:

#### git branch

```
git branch -a
```

The outputs tells what branch you are on, marked with an asterisk. By default (if you have not created any branch) you are in the master branch.

```
* master
```

## Exercise 10 – Checkout a branch from git_tutorial project

Since others might have asked you to review and test new branches at this stage you would like to have a look at the code and test it. To review a code may be enough to browse it in a Gogs window.

But in order to test it you have to checkout it to your `working copy` from the command line:

```
git fetch
```

(this will detect all the branches that others pushed)

```
git checkout <other_branch_name>
```

And it will update the contents of your directory giving an output similar to this:

```
Branch greetings_spanish set up to track remote branch greetings_spanish from origin.
Switched to a new branch 'greeting_spanish'
```

**CAUTION**: If you have uncommited changes in your project and you perform a `checkout` all your changes will be dragged into the other branch. You will see a `'M'` after the checkout. To avoid that it is preferable to do always `git commit` before doing a checkout.

```
M	README.md
Switched to branch 'master'
Your branch is up-to-date with 'origin/master'.
```

Additionally if you have files not added happens more or less the same.

**HINT**: It is very recommendable to use `git status` before a checkout. In case there is something wrong or potentially dangerous you will see a message describing the problem and suggestions to overcome it:

```
Your branch is up-to-date with 'origin/master'.
Untracked files:
  (use "git add <file>..." to include in what will be committed)

  greetings_catalan.sh

nothing added to commit but untracked files present (use "git add" to track)
```

## Exercise 11 – Review and test

Once you have checked out to the branch you have to test you can open the files in your preferred text editor and review them.

To test it you only have to do:

```
bash run.sh
```

If the program does the right thing you can express your approval to the merge request:

## Exercise 12 – Approve a pull request

* Open the browser and go to the Gogs project Git_Training main page.
* Pull requests.
* Choose the pull request you are willing to approve.
* Go to “Write” in the tab discussion, and say you are right with the pull.
* Click on “Add comment”.

After that, the project coordinator will accept the pull requests and a new version of the software will be released.
