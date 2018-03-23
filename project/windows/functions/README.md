# Welcome to the Git Training!

Our goal in this project is to design, all together and collaboratively, an HTML web page that will display all 25 things that each of us should do before turning 25. The contents of the webpage will be directly inspired from the list available [here] https://gentwenty.com/bucket-list-25-before-25/. Since nobody wants to enter all 25 items - a long and painful task - , each of us will be responsible for adding one item.

We are working on a common project, so the use of a versioning system like Git is appropriate. This will allow to keep track of everyone's contributions and ensure their smooth integration within the workflow.

Concretely, we will proceed in six steps:

1. We will retrieve the project from GitHub
2. We will let others know about your intention to add contents to the webpage
3. We will actually add contents to the page
4. We will distribute your changes publicly, so that anyone can see them.
5. We will retrieve changes by others, to benefit from their work too.
6. We will modify the style (colours) of the page, which will introduce conflits, and see how Git manages those.

Each of the five steps will correspond to one practical exercise, where you will familiarize yourself with basic Git commands.

#### Exercise 1 - Clone the project, play around and experiment
Right click in the Windows desktop. From the drop-down menu, look for TortoiseGit then "clone". Copy-paste the URL of the project (https://github.com/fmassonn/Git_Training.git) and clone it.

Enter the folder that has been created, and go to `./project/windows`. There you will find an HTML page named `twenty-five.html`. Visualize it with any browser.

#### Exercise 2 - Open an issue
Browse the Git project webpage (https://github.com/fmassonn/Git_Training). In the upper tab, click "Issues", then "New issues". Let the others know that you intend to modify the file `twenty-five.html` by posting an issue. Be explicit, and do not hesitate to play around, tag people (@...), use colors, flags, labels, etc. Once your issue is published, everyone else in the room will know about your intentions, which is one of the basics of collaborative work.

#### Exercise 3 - Add contents to the webpage
In your local copy of the project (that is, the one that you have on your Windows desktop), open the HTML webpage `twenty-five.html` with a text editor (right-click >> Notepad++ for example). You should see the HTML code that is used to display the webpage you visualized in Exercise 1. The text that appears in the webpage is coded as the last item of a long list to be filled by participants:

```
<!DOCTYPE html>
<html>
  <head>
    <link href="styles.css" rel="stylesheet" type="text/css">
    <title> Twenty-five things to do before you turn 25 </title>
  </head>
  <body>

    <div class="master">

      <h1> Here are the 25 things you should do before turning 25... 
           (from  <a href="https://gentwenty.com/bucket-list-25-before-25/">here</a>)
      </h1>
    </div>

    <div class="item">
      <ol>
        <!-- Item # 1  [CERES.01]-->

        <!-- Item # 2  [CERES.02]-->

        .
        .
        .
        .
        .

        <!-- Item # 22 [CERES.22]-->

        <!-- Item # 23 [CERES.23]-->

        <!-- Item # 24 [CERES.24]-->

        <!-- Item # 25 [EXAMPLE] -->
        <li>
          <b> Go a week without watching any TV. </b> Inspired by Natalee’s recent TV-free week, I’d like to attempt something similar. I’d like to at least go one week but maybe even attempt a month.
        </li>

     <!-- End of the section to edit -->

```

It's now your turn to add an item. Browse the webpage https://gentwenty.com/bucket-list-25-before-25/ and **copy-paste the item that corresponds to your CERES computed ID**. If you are using CERES.12, copy-paste the 12th item of the list ("Step out of my comfort zone..."). Follow the structure of the example given in the HTML file. You can at all times save the HTML page and visualize it by refreshing it in the browser. Once you are satisfied with your changes, you will need think think how you can integrate them to the project and let others know about your update.

Git has noticed that the file you edited has been modified: a red exclamation mark (<span style="color:red">!</span>) appears next to the file in the explorer. Git is supposed to keep track of `twenty-five.html`, but it hasn’t recorded your changes yet: we need to "commit" the changes:

- Right click the file `twenty-five.html`
- Click "commit --> master"

This will open a dialog where you can leave a message explaining what you did. **Take this step seriously!** Commits are the backbone a project: together, they define all the steps that the project has gone through, so it is important to document what each commit corresponds to. Producing clear documentation is another basics of collaborative work.

Note that you can do as many commits as you wish while developing your function. If you reach a point at which any of the open issues gets solved, you can make your commit message end with `Fixes #issue_number` ([Exercise 4 – Open new issue in Git_Training project](https://github.com/fmassonn/Git_Training/src/master/project/windows/issues)).

After the commit, the file should appear with a green "V". Congratulations, you did your first commit!

#### Exercise 4 - Push your changes
Your changes to `twenty-five.html` are saved and committed locally, but for now, nobody can benefit from your work and see these changes: your local copy of the project differs from the remote version that you initially cloned from. You want to let your collaborators know about your changes, don't you? For this, you need to "push" your local copy to the remote one.

Right-click on the main folder (`Git_Training`), go to TortoiseGit, and click "push". You will be asked to enter your credentials. Once your push is successful, your commit and the related changes will be publicly available for anyone. Congratulations!


#### Exercise 5 - Pull the project to benefit from updates by others
Just like you, people around you have added contents to `twenty-five.html`. Fortunately, in this first part of the training, all modifications could be done independently and there will be no conflicts. You can update your local copy of the project in order to see the other's additions, by doing a "pull".

Right-click no the main folder ('Git_Training'), go to TortoiseGit, and click "pull". Once the project is pulled, you will see everyone else's commits and everyone else's additions. Open the file `twenty-five.html`, it should now have plenty of new items.


#### Exercise 6 - Managing conflicts
The previous example went smoothly, because the changes introduced by each of the project participants were well delimited in the common document.

We will now introduce changes that, potentially, can induce conflicts. For this we are going to work in the "styles" file `styles.css`. Here there an usefull link for [CSS Colors](https://www.w3schools.com/cssref/css_colors.asp). 

To do so, we divide the classroom in two sub-groups: the "left" branch, and the "right" branch. For both sub-groups the tutors are going to create a **branch** live in the classroom. A branch is a line of the development that can move forward independtly of the main line of the development ("the master"). Eventually, branches should be merged back to the master.

Create a branch in your local copy: right-click, create branch.
* If you belong to the left group, create a branch named develop-red
Then switch to the branch, make changes in the styles.css file. If you belong to the "left" group, your style changes will be to make things appear in reddish tones. Edit the `styles.css` file to reach this:
```
.master {
  background-color: red;
  color: white;
}

.item {
  background-color: orange;
  color: white;
}
```
and then visualize the result.

* If you belong to the right group, create a branch named develop-green
Then switch to the branch, make changes in the styles.css file. Your style changes will be to make things appear in greenish tones. Edit the `styles.css` file to reach this:
```
.master {
  background-color: green;
  color: white;
}

.item {
  background-color: darkgreen;
  color: white;
}
```
and then visualize the result.

As usual, commit your changes when you are satisfied, and push them.

#### Exercise 7 – Merge branches back to the master: conflicts

The tutors - as supervisors of the project - will now merge the two branches back to the master. Follow their instructions.

#### Exercise 8 - Solving conflicts while on the same branch
It can happen that, when you pull the project, other users working in the same branch as you have introduced conflicting changes. Think for example at a simple text file that says
```
[file.txt]
a = 1
b = 3
```

Suppose that your colleague has modified the file into 
```
[file.txt]
a = 2
b = 3
c = 4
```
and has already pushed the changes to the remote. If you "pull" the project, Git will add the line "c = 4", but won't know what to do about the line "a = ...". It will notify conflicts, and you will be asked to manually decide how the final file should look like.

You can experiment this by changing the "styles.css" file and attempting to pull/push the results. With 24 people working on the same line of code, there will certainly be conflicts, but at least each of them can be solved cleanly.










