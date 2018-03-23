# Manage new content

- We will actually add contents to the page.
- We will distribute your changes publicly, so that anyone can see them.
- We will retrieve changes by others, to benefit from their work too.

## Exercise 4 - Add contents to the webpage
In your local copy of the project (that is, the one that you have on your Windows desktop), open the HTML webpage `twenty-five.html` with a text editor (right-click >> Notepad++ for example). You should see the HTML code that is used to display the webpage you visualized in Exercise 1. The text that appears in the webpage is coded as the last item of a long list to be filled by participants:

```html
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

![7.png](https://github.com/fmassonn/Git_Training/raw/master/resources/7.png)

This will open a dialog where you can leave a message explaining what you did. **Take this step seriously!** Commits are the backbone a project: together, they define all the steps that the project has gone through, so it is important to document what each commit corresponds to. Producing clear documentation is another basics of collaborative work.

Note that you can do as many commits as you wish while developing your function. If you reach a point at which any of the open issues gets solved, you can make your commit message end with `Fixes #issue_number` ([Exercise 3 – Open new issue in Git_Training project](https://github.com/fmassonn/Git_Training/tree/master/project/windows/issues)).

After the commit, the file should appear with a green "V". Congratulations, you did your first commit!

## Exercise 5 - Push your changes
Your changes to `twenty-five.html` are saved and committed locally, but for now, nobody can benefit from your work and see these changes: your local copy of the project differs from the remote version that you initially cloned from. You want to let your collaborators know about your changes, don't you? For this, you need to "push" your local copy to the remote one.

Right-click on the main folder (`Git_Training`), go to TortoiseGit, and click "push". You will be asked to enter your credentials. Once your push is successful, your commit and the related changes will be publicly available for anyone. Congratulations!


## Exercise 6 - Pull the project to benefit from updates by others
Just like you, people around you have added contents to `twenty-five.html`. Fortunately, in this first part of the training, all modifications could be done independently and there will be no conflicts. You can update your local copy of the project in order to see the other's additions, by doing a "pull".

Right-click no the main folder ('Git_Training'), go to TortoiseGit, and click "pull". Once the project is pulled, you will see everyone else's commits and everyone else's additions. Open the file `twenty-five.html`, it should now have plenty of new items.
