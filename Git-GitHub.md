# Git and GitHub

### Intro
- **How do software development teams work together to build projects in a distributed and async manner?** 
- **Teams need to keep track of project versions both for further development and for potential rollbacks and recovery.** 

#### What is Git
- **Distributed version control system**
- Allows you to backup your code and keep your project's code safe from local device issues (ALWAYS PUSH YOUR CODE)
- Allows multiple devs to work on a project simultaneously and asynchronously without conflicting their changes
- Allows for version tracking over time as well as reverting to prior versions of the project
- Git enables teams to work together on different aspects of the project utilizing branches
- Without Git, there would be significantly more friction building and managing software between teams and projects

#### Key Concepts and Terms
- **Repository (Repo)** - The storage space for your project that contains all the files and complete version and revision history
    - **Local Repository** - The complete repository of source code and project files stored locally on your device.
    - **Remote Repository** - The copy of the source code stored on a server, usually GitHub.
- **Commit** - A record of what you changed at a moment in time as well as a message associated with what you changed.
- **Branch** - A version of the project codebase existing in parallel with the *main* codebase that allows features to be developed without affecting the main codebase.
- **Merge** - Combines changes from different branches and enables new code to be integrated into the project.

---

### What is GitHub
- **GitHub** - A web-based version control platform that uses Git for collaboration and project management.

#### Key Features
- **Collaboration Tools**
    - **Pull Request** - Allows a user to propose a change to the project and then decide via discussion and review before merging the modification.
    - **[Code Review](https://github.com/features/code-review)** - GitHub allows for code reviews that let team members review changes.
- **[Issue Tracking](https://github.com/features/issues)**
    - GitHub allows for teams to manage tasks, bugs, and feature requests that are linked directly to the code.
    - Can track progress on issues directly on the platform via progress indicators.
- **Project Management**
    - Has project management features like boards, milestones, labels, etc.
    - **[Actions](https://github.com/features/actions)** - Allows for workflow automations for projects large and small.

---

## Git Commands (Its Terminal Time 🎉)

### Installing Git and Setting up GitHub

#### Git
- **NOTE: If you use a \*nix based system like MacOS or Linux, Git is usually installed by default. In case it is not, we'll go over it here.**

    - **Linux**
        - Open terminal and check if Git is installed using `$ git --version`. If it is, congrats! If it's not, run the command `$ sudo apt install git-all` for debian-based distros or `$ sudo dnf install git-all` for RPM-based distros like Fedora.

    - **MacOS**
        - Open terminal and run `$ git --version`. If Git is not installed, run `$ xcode-select --install`, and Git will be installed.

    - **Windows**
        - **Why would you ever use Windows?**
        - Click [here](https://git-scm.com/download/win) and the download will start automatically. Then install Git using that program.

#### GitHub
- Navigate to [Github.com](https://github.com) and set up an account. Your account is now good to go, and you can begin creating repos, searching repos, and starring and contributing to projects.

### Basic Git Commands

#### Workflow
- `$ git init` - Initializes a new Git repository in the current directory. The default branch will be named `main`.

- `$ git add <file>` - Adds the specified files in the local repository and stages it to be committed. **NOTE: replace <file> with the file name you want to be added.**
    - Can also use `$ git add .` to add all files in the directory.

- `$ git clone <repo url>` - Copies the remote repository on GitHub to the local machine.
   - Try this command out by cloning the repo for this project. URL: https://github.com/alewtschuk/Terminal-and-Github-lesson.git

- `$ git commit -m "Message"` - Commits the tracked changes with the associated message.

- `$ git status` - Displays the status of the working directory.

- `$ git log` - Displays the list of all commits in the current branch.

#### Branching
- `$ git branch` - Displays the current branch you're in.

- `$ git checkout -b <branch name>` - Creates a new branch with your chosen name and switches to it.
    - Usually done to create a new feature or fix a bug without conflicting with the main codebase.

- `$ git merge <branch name>` - Merges the changes from the specified branch to the one you're currently in.

## Using GitHub

### Creating a Repository
- Go to GitHub and click the + in the top right-hand corner, then select "New repository".

- Fill in the name, description, and choose visibility (public/private). You can initialize with a README if wanted.
    - A README is a markdown file that explains the project. It's standard for all repos to have this.

- At this point, you can upload files or navigate to the green Code button on the main page of the repo, copy the URL, and clone the repo.

### Creating and Using Pull Requests (PRs)

#### Creating a Pull Request
Once you have pushed your changes to a branch on GitHub, you can create a pull request to propose merging those changes into another branch (usually the main branch). Here’s how to do it:

- **Navigate to the Repository:**
   - Go to the GitHub repository where you pushed your branch.

- **Open the Pull Requests Tab:**
   - Click on the "Pull requests" tab at the top of the repository page.

- **Click on New Pull Request:**
   - Click the "New pull request" button.

- **Select the Branches:**
   - In the "base" dropdown, select the branch you want to merge into (e.g., `main`).
   - In the "compare" dropdown, select the branch that contains your changes.

- **Review Changes:**
   - Review the differences between the two branches to ensure everything is correct.

- **Create the Pull Request:**
   - Click the "Create pull request" button.
   - Add a title and description for your pull request. Be clear about what changes are being proposed and why.

- **Submit the Pull Request:**
   - Click "Create pull request" again to submit it.

#### Reviewing Pull Requests
Once a pull request is created, team members can review the proposed changes. Here’s how the review process works:

- **Notification:**
   - Team members will receive notifications about new pull requests. They can also see open pull requests in the repository.

- **Review the Changes:**
   - Click on the pull request to view it. GitHub provides a "Files changed" tab where reviewers can see the specific changes made.

- **Commenting:**
   - Reviewers can leave comments on specific lines of code by clicking the "+" icon next to the line number.
   - General comments can be added in the "Conversation" tab.

- **Requesting Changes:**
   - If a reviewer finds issues, they can request changes by clicking the "Request changes" button. This indicates that the author needs to make specific adjustments before merging.

- **Approving the Pull Request:**
   - If the reviewer is satisfied with the changes, they can approve the pull request by clicking the "Approve" button.
   - They may also leave a comment indicating their approval.

- **Merging the Pull Request:**
   - Once the pull request has been approved (and all checks have passed), the author or a designated team member can merge it into the base branch by clicking the "Merge pull request" button.
   - After merging, the author may delete the branch if it's no longer needed.

## Resources and Docs
- [GitHub Guides](https://docs.github.com/en)
- [Git Docs](https://git-scm.com/doc)