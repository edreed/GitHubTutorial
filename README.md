# Newport Robotics Group GitHub Tutorial

This is a tutorial introducing GitHub and the standard open source software
development workflow.

## Prerequisites

In order to do the tutorial, you will need to have a GitHub account and install
the WPILib software development tools and Git source code control.

1. If you do not already have one, [create a GitHub account][L001].
2. Follow the instructions at [WPILib Installation Guide][L002] to install the FRC
   development environment.
3. Install [Git][L003].

## Tutorial

### 1. Fork the project repository

The first step to becoming a contributor to an open source project is to fork
the project repository into your own GitHub account. This can be done from the
project repository's main GitHub page. To clone this repository:

1. Go to [`https://github.com/NRG948/GitHubTutorial`][L004].
2. Click on the drop down arrow on the Fork button.
3. Select "Create new fork".
4. Ensure that your GitHub account is selected under Owner and that the
   repository name is available. If not, it's likely you already cloned the
   repository and don't need to again.
5. Press the "Create fork" button.

### 2. Clone the project repository

To begin working on your own fork, you wil need to clone it to your computer.
You can do this from within WPILib Visual Studio Code. You'll need to know the
Git URL to your fork which can be derived from you GitHub user name. For
example, my fork is at:

`https://github.com/edreed/GitHubTutorial.git`

To clone your repository in VS Code:

1. Type Ctrl-Shift-P (Command-Shift-P on MacOS) to get the Command Palette.
2. Type "Git Clone" into the search box.
3. Select the "Git: Clone" item.
4. In the following prompt, type or paste in the project repository URL and
   press Enter.
5. Select the folder in which to clone the project.

### 3. The `main` a branch

Each project has a `main` branch which contains the official version of the
code. It is good practice to keep the `main` branch of your fork an exact mirror
of the project's `main` branch. To enable keeping the `main` branch in sync, you
will first need to create an `upstream` remote. To add the `upstream` remote in
VS Code:

1. Type Ctrl-Shift-P (Command-Shift-P on MacOS) to get the Command Palette.
2. Type "Git Add Remote" into the search box.
3. Select the "Git: Add Remote..." item.
4. Type or paste the Git URL to the project repository and press Enter. For
   example, this repository's Git URL is
   `https://github.com/NRG948/GitHubTutorial.git`.
5. Type "upstream" into the remote name prompt and press enter.

### 4. Preparing to make a change

Since you want to keep the `main` branch of your fork an exact copy of the
project repository's `main` branch, you should avoid making changes directly on
it.

To prepare for making a change to the main project, you will pull the current
state of the project repository's `main` branch from the `upstream` remote we
added in the previous step into the `main` branch of your clone.

First, ensure you are currently on the `main` branch of your clone:

1. Type Ctrl-Shift-P (Command-Shift-P on MacOS) to get the Command Palette.
2. Type "Git Checkout" into the search box.
3. Select the "Git: Checkout" item.
4. Select the `main` branch.

Then, sync the `main` branch of your clone in VS Code:

1. Type Ctrl-Shift-P (Command-Shift-P on MacOS) to get the Command Palette.
2. Type "Git Pull" into the search box.
3. Select the "Git: Pull from..." item.
4. Select `upstream`.

Finally, push your clone's `main` branch to your fork's GitHub repository:

1. Type Ctrl-Shift-P (Command-Shift-P on MacOS) to get the Command Palette.
2. Type "Git Push" into the search box.
3. Select the "Git: Push" item.

### 5. Making a change

After syncing the your fork's `main` branch, create a new branch in your clone
before beginning to make changes. To create a new branch in VS Code:

1. Type Ctrl-Shift-P (Command-Shift-P on MacOS) to get the Command Palette.
2. Type "Git Create Branch" into the search box.
3. Select the "Git: Create Branch..." item.
4. Type in your new branch name and press Enter.

It is a good practice to prefix the branch name with your GitHub user name to
make it easy to identify the author. You should also choose a descriptive name
for your branch so that you can easily identify the work you're doing later.
As an example I would create a branch named `"edreed/add-swerve-drive"` if I
were adding the Swerve drive implementation to the robot code.

You are now ready to begin making changes.

### 6. Committing the change

Once your change is complete and ready for review, you first need to commit your
changes and push it to your fork's GitHub repository. To commit your changes in
VS Code:

1. Switch to the GitHub sidebar.
2. Press the `+` symbol next to the "Changes" bar to stage all changes for
   commit. (You can also choose a subset of files to stage by pressing `+`
   symbols next to their names.)
3. Type a descriptive message into the Message box.
4. Press the "Commit" button.

This will commit all of the staged changes to you clone's branch. You'll need to
push it to your fork's repository. To push the changes to your fork in VS Code:

1. Type Ctrl-Shift-P (Command-Shift-P on MacOS) to get the Command Palette.
2. Type "Git Push" into the search box.
3. Select the "Git: Push" item.

### Creating a Pull Request

To have your changes reviewed and merged into the `main` branch of the project
repository, you need to create a Pull Request. To create one:

1. Go to the project repository's main GitHub page (e.g.
   `https://github.com/NRG948/GitHubTutorial`).
2. Switch to the "Pull requests" tab.
3. Press the "New pull request" button.
4. Ensure the base branch is `main` and the `compare` branch is the one from
   your fork's repository.
5. Enter a brief but descriptive title. You can provide additional details in
   the "Add a description" box. The more detail you provide, the better
   understanding a reviewer will have of your change.
6. Press the "Create pull request" button.

### Responding to feedback

Often times, reviewers will make helpful suggest to improve the code or identify
things that may have been overlooked. You can make additional changes, commit
and push them to your fork's repository to automatically update the Pull Request
in response to feedback.

### Merging your changes

Once the Pull Request has been approved, you can merge your changes to the
`main` branch of the project repository simply by clicking on the "Merge pull
request" button.

### Cleaning up

To clean up, follow the steps in the "4. Preparing to make a change" section.
Since your changes have now been merge, you no longer need the branch. After
switching back to the `main` branch, you can delete the now obsolete branch in
VS Code:

1. Type Ctrl-Shift-P (Command-Shift-P on MacOS) to get the Command Palette.
2. Type "Git Delete Branch" in the search box.
3. Select the "Git: Delete Branch..." item.
4. Select your obsolete branch.

Now, you're ready to make more changes!

[L001]: https://github.com/signup
[L002]: https://docs.wpilib.org/en/stable/docs/zero-to-robot/step-2/wpilib-setup.html
[L003]: https://git-scm.org
[L004]: https://github.com/NRG948/GitHubTutorial
