## About
This repository provides the workspace for an intro to Git and Source Control workshop for the class of IMGD 3000. This workshop will cover the following as they relate to Source Control.

1. What is Source Control?
2. Git Syntax & Desktop
3. Activity

## Downloads
Here is a list of downloads that will be needed to run the software as part of this activity. Please set these up before beginning the activity.

- [Git]([url](https://git-scm.com/downloads))
- [GitHub Desktop]([url](https://desktop.github.com/))

## What is Source Control?
Source control is an essential and commonly used tool in software development. Source control supports **Version Control**, sets up a **Remote Repository** as a shared instance of the codebase, and enables **Multi-Developer Collaboration.**

### Version Control
First and foremost, source control provides _versioning_, a concept used to track changes to a product over time. 

Consider that software, such as games, is an ever-changing product that commonly evolves from one version to another. Source Control tracks the difference between these versions and stores them in a linear history, provide a record of changes that are made across different versions.

    Version 1 -(save changes)-> Version 2 -(save changes)-> Version 3

The benefits of storing this history of changes are numerous: in most cases, the latest version of a software might be the most "up-to-date" instance of it, but consider that developers may want to revert changes and go back to a previous version of software.

    Version 1 -(save changes)-> Version 2 -(save changes)-> Version 3 -(revert changes)-> Version 2

Source control enables this, without us needing to store each version of the source code independently!

![image](https://github.com/NickFrangie/Workshop-Git/assets/51765298/8b4a6c9f-ef00-4d9e-9fff-ffa10ceb82fb)

### Remote Repositories
While the version control that source control systems provide is fully compatible with development to one local machine, its strengths lie in how it expands to multiple machines and cross-developer collaboration. Source control systems like Git allow developers to store and manage their code in **remote repositories**, enabling seamless collaboration and version control across teams.

![image](https://github.com/NickFrangie/Workshop-Git/assets/51765298/0db8e311-0def-4e87-a579-998357932df4)

A remote repository, also called the "origin" or "upstream," provides a centralized, shared instance of the codebase, ensuring that there is one single instance of the project that all developers can work from.

![image](https://github.com/NickFrangie/Workshop-Git/assets/51765298/3f46db10-b092-48c9-b7c6-0c480d9894b1)

The act of downloading the latest version of the remote repository is called **pulling.** The act of uploading changes from a local machine, where individual developers work, to the shared codebase, is called **pushing.** Developers consistently use both these actions as a means to collaborate with others.

### Multi-Developer Collaboration
Because source control tracks source code based on the changes we make to it, it enables multiple developers to collaborate on a project simultaneously!

The set of changes one developer makes (Changeset A), and set of the changes another development makes (Changeset B) can oftentime be worked on independently and then merged back into the shared codebase when they push. In cases where this is successful, it means that multiple developers can make changes to the same source code, merge them into the shared codebase in any order, and still end up with a shared codebase that reflects all of their work!

    Original Version -(Changeset A)-> Version A -(Changeset B)-> Version AB
    Original Version -(Changeset B)-> Version B -(Changeset A)-> Version AB

The one exception to this are **merge conflicts** - situations where multiple developers have edited the same line of code. These situations require developers to manually resolve the conflicts by deciding which of the two different lines of code (or both) to accept in the final version. We will review this as part of today's activity.

## Git Syntax & Desktop
Traditionally, Git is used via the command line, enabling developers on their local machines access to a number of commands made available through source control systems such as **git.** These commands provide a high level of control and options to developers while they work with versioning and resolving merge conflicts.

![image](https://github.com/NickFrangie/Workshop-Git/assets/51765298/dbcd4a0a-e1fe-4f2c-9884-2a3e742306ec)

Despite this, today's activity will focus on the basics of source control and how to use it. For this reason, Git Desktop will be more than powerful enough.

## Activity
1. **Forking:** Create your own version of this remote repository.

This task involves creating your own copy of the remote repository. By forking the repository, you duplicate the entire project into your GitHub account, allowing you to make changes without affecting the original repository. 

_Click on the "Fork" button at the top of the remote repository's [GitHub page]([url](https://github.com/NickFrangie/Workshop-Git)) to do this._

2. **Pulling:** Download the forked remote repository to your local machine.

This action synchronizes the code on your local machine with the code in your forked repository on GitHub, ensuring you have the latest version to work with. In the case of first downloading the project, this also pulls all the code currently on the remote repository to your local machine.

_Click on the green "Code" button at the top of the remote repository's [GitHub page]([url](https://github.com/NickFrangie/Workshop-Git)), and then select **Open with GitHub Desktop** to do this._

3. **Committing:** Make a change and save it to your local machine, creating a new version of the software called a **commit.**

By making a change on our local machine and _committing_ it, you'll be making creating a new version of the software with your changes. Commits are created every time you save your current changes to the local or remote repository, and utilizing them to track your changes is a crucial part of utilizing source control.

For this step, simply replace the {Your Name Here} and {Data Here} strings in the main.c file. Then, view the repository in GitHub Desktop. Take note of the changes to the files in the project on the left hand side of the application; notice how you can preview these changes by clicking on a file? Anything in red is a **deletion**, a line of code that has been removed; anything in green is an **addition**, a line of code that has been added. Even though you only changed part of those lines in the main.c file, the program still counts that as deleting and adding a new line.

_After you have reviewed the changes in GitHub Desktop, press the commit button in the bottom left hand corner. Make sure to add a Summary to the commit, indiciating what changes were made!_

4. **Pushing:** Upload your commit to the forked remote repository.

By pushing updates from your local machine to the remote repository, you can share the changes you've made with other collaborators, enabling them to pull from your code. Do so now!

_Simply press the push origin button in the top menu bar of GitHub Desktop to do this. Then, examine the GitHub page for your forked version of the remote repository. Notice any changes in the main.c file?_

5. **Branching:** Create a new branch, make a change, and push it.

Now, we're going to try a different feature called **branching.** Branching is an important tool for multi-developer colloboration, which allows developers to make multiple commits on a separate instance of the codebase without merging than back into the original shared version of the codebase called "main." This is important for when developers work on a long-term feature that requires a bit more work than simply changing some strings. To emulate this, we're going to make a new branch to implement the very complex and intricate addValues() function.

_Create a new branch called "adding." To do this in GitHub Desktop, simply click the **Current Branch** button and then select **New branch.** From here, implement the logic neccessary for addValues to function correctly. Then, commit your work on the "adding" branch and push it to the remote repository as we did before._

5. **Merging:** Merge that first branch into main.

To merge a branch back into main, the shared codebase that all the developers use, we'll need to switch back to main using the button at **Current Branch** dropdown and then selecting main. From there, simply select the **Choose a branch to merge into main** button on the bottom of the **Current Branch** dropdown, and then select your branch, _"adding."_ Then, push those changes.

_Examine the codebase on your GitHub page. Are your changes to addValues there?_

6. **Conflicts:** Merge the existing branch called _"conflicts"_ into your repository and resolve its merge conflicts.

Sometimes, when you merge branches or make commits, you will create merge conflicts that need to be resolved before the source control system will allow you to proceed. To experience this, merge the _"conflicts"_ branch into main, just as you did before with _"adding."_ 

Merging this branch will cause merge issues where you changed your name and date in step 3, as it attempts to place the name and date with another developer's. But the same branch also includes changes that we may want to keep, such as the new values for a and b. Keeping some changes while discarding others is a common situation when collaborating with source control.

_Resolve these conflicts by opening the conflicting file in a text editor and manually deleting which lines you don't want. Keep the changes to the a and b values, but make sure your name and the current date are still listed in the main() function. Once these conflicts are resolved, save the file, return to GitHub Desktop and complete the merge, pushing the commit back to the remote repository. Examine the repository online to ensure that the desired changes were made!_

### Conclusion
With this, you'll have effectively concluded the source control workshop! Hopefully, you can see how this useful tool can empower you as you collaborate with additional developers in you upcoming project!
