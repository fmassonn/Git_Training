# Add new functions

In this chapter we will create the functions to say Hello in the different languages from the table above.

In the beginning you will modify the file `greetings.sh` by adding your function e.g. `say_hello_catalan()`.

Then you will modify `../run.sh` to call your function.

In a further chapter of this tutorial, we will merge all the calls in the same file `run.sh` and we will see how git helps on the process of resolving conflicts.

#### Exercise 6 – Perform function commit

Now you have time to make changes in Git_Training project, i.e. modify 'greetings.sh' file and develop your function. After that, if we check the status of our project again, Git tells us that it’s noticed a new file. We can tell Git to track a file using git add.

```
git add .
```

Git now knows that it’s supposed to keep track of 'greetings.sh', but it hasn’t recorded these changes as a commit yet. To get it to do that, we need to run one more command:

```
git commit -m "message explaining what you have done. Fixes issue #issue_number"
```

When we run `git commit`, Git takes everything we have told it to save by using `git add` and stores a copy permanently inside the special `.git` directory. This permanent copy is called a commit (or revision) and its short identifier is `f22b25e` (Your commit may have another identifier.)

You can do as many commits as you wish while developing your function. If you reach a point at which any of the open issues gets solved, you can make your commit message end with `Fixes #issue_number` ([Exercise 4 – Open new issue in Git_Training project](https://www.elic.ucl.ac.be/TECLIM/Git_Training/src/master/project/linux/gogs_issues)).

If you don't specify the `-m` parameter a text editor will open automatically to allow you to write the commit message.

You can now ask Git to show the project history to check that the commit was successful by using:

```
git log
```

#### Exercise 7 – Perform run script commit

You can now modify `run.sh` script to add the call to your newly created function (do not forget to source the file containing the function).

Test it:

```
bash run.sh
```

When you are sure it works (it greets you in english and in your choosen language), perform a separate commit by following similar steps as in previous exercise:

```
git add run.sh
git commit
```

#### Exercise 8 – Push git_tutorial project branch

```
git push origin <branch_name>
```

where `<branch_name>` is the name used in the previous step.