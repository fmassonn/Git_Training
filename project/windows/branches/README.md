# Managing conflicts

The previous example went smoothly, because the changes introduced by each of the project participants were well delimited in the common document.

We will now introduce changes that, potentially, can induce conflicts. For this we are going to work in the "styles" file `styles.css`. Here there an usefull link for [CSS Colors](https://www.w3schools.com/cssref/css_colors.asp). 

To do so, we divide the classroom in two sub-groups: the "left" branch, and the "right" branch. For both sub-groups the tutors are going to create a **branch** live in the classroom. A branch is a line of the development that can move forward independtly of the main line of the development ("the master"). Eventually, branches should be merged back to the master.

You can think of it like making an entire copy of your repository folder that you can edit, without affecting the original versions of your scripts.

## Exercise 7 – Create branch in Git_Training project

| If you belong to the left group | If you belong to the right group 
| -------- | -------- |
| Ceate a branch named `develop-red`. Then switch to the branch, make changes in the `styles.css` file. | Create a branch named `develop-green`. Then switch to the branch, make changes in the `styles.css` file. |
| `.master {` | `.master {` |
| `  background-color: red;` | `  background-color: green;` |
| `  color: white;` | `  color: white;` |
| `}` | `}` |
| `.item {` | `.item {` |
| `  background-color: orange;` | `  background-color: darkgreen;` |
| `  color: white;` | `  color: white;` |
| `}` | `}` |
| Your style changes will be to make things appear in reddish tones. | Your style changes will be to make things appear in greenish tones. |

Create a branch in your local copy: right-click, create branch:

|||
| -------- | -------- |
| ![Git-Bash-14.png](https://github.com/fmassonn/Git_Training/raw/master/resources/14.png) | ![Git-Bash-15.png](https://github.com/fmassonn/Git_Training/raw/master/resources/15.png) |

`<branch_name>` could be the name of the PC you are working on.

Switch to that branch

|||
| -------- | -------- |
| ![Git-Bash-16.png](https://github.com/fmassonn/Git_Training/raw/master/resources/16.png) | ![Git-Bash-17.png](https://github.com/fmassonn/Git_Training/raw/master/resources/17.png) |
| ![Git-Bash-18.png](https://github.com/fmassonn/Git_Training/raw/master/resources/18.png) | |


and then visualize the result.

As usual, commit your changes when you are satisfied, and push them.


## Exercise 8 – Merge branches back to the master: conflicts

The tutors - as supervisors of the project - will now merge the two branches back to the master. Follow their instructions.

## Exercise 9 - Solving conflicts while on the same branch
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
