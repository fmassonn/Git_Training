# Add new content

In this chapter we will fill the HTML file to see different sections in different styles.

In the beginning you will modify the file `styles.css` by adding your own style. Here there an usefull link for [CSS Colors](https://www.w3schools.com/cssref/css_colors.asp)

Then you will modify `branching-website.html` to apply your style to your own section.

In a further chapter of this tutorial, we will merge all the styles in the same file `branching-website.html` and we will see how git helps on the process of resolving conflicts.

#### Exercise 6 – Perform function commit

Now you have time to make changes in Git_Training project, i.e. modify 'styles.css' file and develop your style. After that, if we check the status of our project again, Git tells us that it’s noticed a modified file. We can tell Git to track a file using git add.

```
git add .
```

Git now knows that it’s supposed to keep track of 'styles.css', but it hasn’t recorded these changes as a commit yet. To get it to do that, we need to run one more command:

```
git commit -m "message explaining what you have done. Fixes issue #issue_number"
```

When we run `git commit`, Git takes everything we have told it to save by using `git add` and stores a copy permanently inside the special `.git` directory. This permanent copy is called a commit (or revision) and its short identifier is `f22b25e` (Your commit may have another identifier.)

You can do as many commits as you wish while developing your function. If you reach a point at which any of the open issues gets solved, you can make your commit message end with `Fixes #issue_number` ([Exercise 4 – Open new issue in Git_Training project](https://www.elic.ucl.ac.be/TECLIM/Git_Training/src/master/project/windows/issues)).

If you don't specify the `-m` parameter a text editor will open automatically to allow you to write the commit message.

You can now ask Git to show the project history to check that the commit was successful by using:

```
git log
```

#### Exercise 7 – Perform run script commit

You can now modify `branching-website.html` file to add the section `div` to your newly created style.

Test it by opening the html file in a web browser.

When you are sure it's fine, perform a separate commit by following similar steps as in previous exercise:

```
git add branching-website.html
git commit
```

#### Exercise 8 – Push git_tutorial project branch

```
git push origin <branch_name>
```

where `<branch_name>` is the name used in the previous step.
