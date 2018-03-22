# Add new content

Our goal in this project is to design, all together and collaboratively, an HTML web page that will display all 25 things each of us should do before turning 25. The contents of the webpage will be directly inspired from the list available [here] https://gentwenty.com/bucket-list-25-before-25/

Since we are working on a common project, the use of a versioning system like Git is appropriate. This will allow to keep track of everyone's contributions and ensure their smooth integration within the workflow.

Concretely, we will proceed in five steps:

1. You will retrieve the project from GitHub
2. You will let others know about your intention to add contents to the webpage
3. You will actually add contents to the page
4. You will distribute your changes publicly, so that anyone can see them.
5. You will retrieve changes by others, to benefit from their work too.
4. You will modify the style (colours) of the page

Each of the five steps will correspond to one practical exercise, where you will familiarize yourself with basic Git commands.

In this chapter we will fill the HTML file to see different sections in different styles.


#### Exercise 1 - Clone the project, play around and experiment
Right click in the Windows desktop. From the drop-down menu, look for TortoiseGit then "clone". Copy-paste the URL of the project (https://github.com/fmassonn/Git_Training.git) and clone it.

Enter the folder that has been created, and go to `./project/windows`. There you will find an HTML page named `twenty-five.html`. Visualize it with any browser.

#### Exercise 2 - Open an issue
Browse the Git project webpage (https://github.com/fmassonn/Git_Training). In the upper tab, click "Issues", then "New issues". Let the others know that you intend to modify the file by posting an issue. Do not hesitate to experiment, tag people (@...), use colors, flags, labels, etc. 

#### Exercise 3 - Add contents to the webpage
In your local copy of the project (that is, on your Windows desktop), open the HTML webpage `twenty-five.html` with a text editor (right-click >> Notepad++ for example). You should see the HTML code that is used to display the first item you saw on the webpage:

```
      <!-- First item -->
      <li>
        <b> Run a half marathon. </b> Even for a non-runner, a half marathon is a manageable distance. It’s only running one mile 13 times. We can do it!
      </li>
```

It's now your turn to add an item, below that first item. Browse the webpage https://gentwenty.com/bucket-list-25-before-25/ and **copy-paste the item that corresponds to your CERES computed ID**. If you are using CERES.12, copy-paste the 12th item of the list ("Step out of my comfort zone..."). Follow the structure of the example.

You can at all times save the HTML page and visualize it by refreshing it in the browser.

Once you are satisfied with your changes, you can start to think how you will integrate them to the project and let others know about them. 

Git has noticed that the file you edited has been modified: a red cross appears next to the file in the explorer. Git knows that it’s supposed to keep track of 'tenty-five.html', but it hasn’t recorded your changes yet. To get it to do that, we need to "commit" the changes:

- Right click the file `twenty-five.html`
- Click "commit --> master"

This will open a dialog where you can leave a message explaining what you did. Take this step seriously! Commits are the backbone a project: together, they define all the steps that the project has gone through, so it is important to document what each commit corresponds to.

After the commit, the file should appear with a green "V". Congratulations, you did your first commit!

#### Exercise 4 - Push your changes
Your changes to `twenty-five.html` are saved and committed locally, but your local copy of the project differs from the remote project that you initially cloned. You want to let your collaborators know about your changes, don't you? For this, you need to "push" your local copy to the remote one.

Right-click on the main folder ('Git_Training'), go to TortoiseGit, and click "push". Git will ask you to enter your credentials. Once your push is successful, your commit and the related changes will be publicly available for anyone. Congratulations!



In the beginning you will modify the file `styles.css` by adding your own style. Here there an usefull link for [CSS Colors](https://www.w3schools.com/cssref/css_colors.asp)

Then you will modify `branching-website.html` to apply your style to your own section.

In a further chapter of this tutorial, we will merge all the styles in the same file `branching-website.html` and we will see how git helps on the process of resolving conflicts.

#### Exercise 6 – Perform function commit

Now you have time to make changes in Git_Training project, i.e. modify 'styles.css' file and develop your style. After that, if we check the status of our project again, 

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
