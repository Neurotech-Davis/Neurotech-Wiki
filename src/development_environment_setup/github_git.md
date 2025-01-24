By Priyal Patel for _Neurotech@Davis_

# What is Github?

Github is a web application that stores multiple versions of a project. This allows multiple users to make changes to the project at the same time. The application also has features that allow users to easily integrate all of their changes into one project.

<img width="450" alt="Screenshot 2025-01-23 at 4 14 18 PM" src="https://github.com/user-attachments/assets/4e208c80-dff3-4d5e-85be-098ff67c6778" />


**Repository**

A repository stores all files and folders needed for a project. You can also see the project's revision history.

**Branches**

One way to maintain multiple versions of the project is by using separate branches. The branch that holds the desired version of the project is called Main; this will be automatically created when you create a repository.

Users are able to make a new branch that contains a copy of the content in the Main or any other branch. This also called forking a respository.

**Pull Request**

Users can integrate their changes in their branch into another branch by opening a pull request.

**Clone Repository**

To make changes, a user will need to clone the desired repository. This will create a copy of the repository on your device. You will need to use git (mentioned below) to download changes from other users and upload your changes.

**README**

Users will add any important information about your project using markdown to the README.md file.

# How to Use

**Creating an Account**

Follow Part 1 of this [guide](https://docs.github.com/en/get-started/onboarding/getting-started-with-your-github-account#part-1-configuring-your-github-account) to setup your github account.

See the 'Github Hello World' guide in Additional Resources to practice using the features mentioned above.

# What is Git?

Git is the version control software that interacts with Github (repository storing service). Git is a tool that allows users to interact with different versions of the project. Using Git, users can save the changes on their device, upload their changes to the Github repository, switch to another version of the project, and perform many more tasks.

<img width="375" alt="Git-Workflow" src="https://github.com/user-attachments/assets/06a3534f-a136-47af-b511-89f3084f665d" />


**Remote Repository**

The repository that appears on Github. This respository is stored on Github servers.

**Local Repository**

The repository that stored on your device. It consists of everything in the .git directory.

**Staging Area**

The staging area consists of the files you want git to track. You must explicitly add these files to the staging area each time you want git to know about new file edits.

**Working Directory**

This is the folder on your device that holds all files and folders in your local repository.

All of your changes are only stored here until you add them to the staging area, commit them to the local repository, or push them to the remote repository.

See 'Medium on Git' in Additional Resources for more information.

# Installing Git

Download the [git](https://git-scm.com/downloads) version that matches your device.

# How to Use

This tutorial will be using VSCode and show you how using VSCode will make the process of using git easier. The tutorial will be only using the MAIN branch, so see 'Git Branches' in Additional Resources for using multiple branches.

**Setting Credentials**

Follow this [guide](https://docs.github.com/en/get-started/getting-started-with-git/set-up-git#setting-up-git) to set up git and link your account.

**Create a Respository**

On Github:

1. Sign into your account
2. Click on your profile
3. Click on 'Your repositories'
4. Click on the green button 'New'
5. Give your repo a name
6. Select public or private
7. (Optional) Select 'Add a README file'
8. Click 'create repository'

**Cloning a Repository**

You can either clone an existing repository or create a new one and then clone this repo. For private repositories, you can only clone them if you are added as a contributer. See 'Adding Contributors' in Additional Resources.

<img width="300" alt="Screenshot 2025-01-23 at 2 52 39 PM" src="https://github.com/user-attachments/assets/f6c7c94f-e4a7-43e4-8f40-98cad868d85e" />

Go to your repository and click on the green 'Code' button. Copy the link under 'HTTPS'.

In VSCode terminal run:

```
$ git clone <https-repo-url>
```

**Git Changes Workflow**

After making changes to a file, the first step is to make sure you get any new changes another user has made on the same branch. If you do not do this, then you will overwrite the changes that other users have made. :(

```
$ git pull
```

If you have merge conflicts, then see 'Resolving Merge Conflicts' in Additional Resources.

Next, you will need to add the changes to the staging area. Make sure you are in the parent folder that has all your changes (hint: use cd terminal command to navigate to the correct folder).

```
$ git add .
```

(Optional) To what files have been added to the staging area you can run this command:

```
$ git status
```

Then, you will need to save a copy of all these changes to your local repository (.git).

```
$ git commit -m "<any-description-of-changes>"
```

Finally, you can move the changes from your local repository to the remote repository on Github.

```
$ git push
```

The first time you run this process you will need to run this command instead (default branch name is MAIN):

```
$ git push --set-upstream origin <branch-name>
```

See 'Git Workflow' in Additional Resources for more information about these steps.

# Additional Resources

- [Github Hello World](https://docs.github.com/en/get-started/start-your-journey/hello-world)
- [Medium on Git](https://medium.com/@lucasmaurer/git-gud-the-working-tree-staging-area-and-local-repo-a1f0f4822018)
- [Git Branches](https://www.educative.io/blog/git-branching-tutorial)
- [Git Cheat Sheet](https://about.gitlab.com/images/press/git-cheat-sheet.pdf)
- [Git Workflow](https://uidaholib.github.io/get-git/3workflow.html)
- [Adding Contributors](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-access-to-your-personal-repositories/inviting-collaborators-to-a-personal-repository)
- [Resolving Merge Conflicts](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/addressing-merge-conflicts/resolving-a-merge-conflict-using-the-command-line)

# Fun Fact

This WIKI is hosted in a remote repository called 'Neurotech-Wiki' and all my changes were added using git.
