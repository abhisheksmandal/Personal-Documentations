## **Basic Git Operations**

### **Check Git Version**

```bash
git --version
```

Displays the installed Git version.

### **Check Repository Status**

```bash
git status
```

Shows the working directory status and staged changes.

### **Initialize a Git Repository**

```bash
git init
```

Creates a new Git repository and a **`.git`** folder in the current directory. Run this command once per project.

### **Add Files to Staging Area**

```bash
git add filename
```

Stages the specified file for the next commit.

```bash
git add .
```

Stages all changes in the current directory for the next commit.

### **Commit Changes**

```bash
git commit -m "Message"
```

Records the staged changes in the local repository with a descriptive message.

### **View Commit History**

```bash
git log
```

Displays the commit history.

```bash
git log --oneline
```

Shows the commit history in a simplified, single-line format.

### **Configure Git User Information**

```bash
git config --global user.name "Firstname Lastname"
```

Sets the global Git username.

```bash
git config --global user.email "example@example.com"
```

Sets the global Git email address.

```bash
git config --global core.editor "code --wait"
```

Sets Visual Studio Code as the default text editor for Git.

### **Create a .gitignore File**

```bash
touch .gitignore
```

Creates a **`.gitignore`** file to specify files and directories for Git to ignore.

The **`.gitignore`** file tells Git which files (or patterns) it should ignore. This is useful for files that are generated during the build process, temporary files, and sensitive information like configuration files containing credentials.

### **Common .gitignore Entries**

Here are some common entries you might include in a **`.gitignore`** file:

- **Operating System Files**

  ```
  # macOS
  .DS_Store

  # Windows
  Thumbs.db
  desktop.ini
  ```

- **Programming Languages and Tools**
  - **Node.js**
    ```
    node_modules/
    npm-debug.log
    ```
  - **Python**
    ```
    __pycache__/
    *.pyc
    ```
  - **Java**
    ```
    *.class
    ```
  - **Visual Studio Code**
    ```
    .vscode/
    ```
- **Environment Files**
  ```
  .env
  ```

## **Branching and Merging**

### **List Branches**

```bash
git branch
```

Lists all branches in the repository.

### **Create a New Branch**

```bash
git branch new-branch
```

Creates a new branch called **`new-branch`**.

### **Switch to a Branch**

```bash
git checkout new-branch
```

Switches to the **`new-branch`**.

```bash
git switch new-branch
```

An alternative to **`checkout`**, switches to the **`new-branch`**.

### **Create and Switch to a New Branch**

```bash
git checkout -b new-branch
```

Creates and switches to a new branch called **`new-branch`**.

```bash
git switch -c new-branch
```

Creates and switches to a new branch called **`new-branch`**.

### **Merge a Branch into the Current Branch**

```bash
git merge new-branch
```

Merges the changes from **`new-branch`** into the current branch.

### **Delete a Branch**

```bash
git branch -d new-branch
```

Deletes the **`new-branch`**. This command only works if the branch has been fully merged.

## **Differences Between Commits**

### **Show Unstaged Changes**

```bash
git diff
```

Displays changes between the working directory and the staging area.

### **Show Staged Changes**

```bash
git diff --staged
```

Displays changes between the staging area and the last commit.

### **Compare Two Branches**

```bash
git diff branch1 branch2
```

Shows differences between **`branch1`** and **`branch2`**.

### **Compare Two Branches (Alternative Syntax)**

```bash
git diff branch1..branch2
```

Another way to show differences between **`branch1`** and **`branch2`**.

## **Stashing**

### **Stash Uncommitted Changes**

```bash
git stash
```

Saves your uncommitted changes and reverts the working directory to match the HEAD commit.

### **Apply Stashed Changes**

```bash
git stash pop
```

Applies the most recent stashed changes and removes them from the stash list.

### **List Stashed Changes**

```bash
git stash list
```

Displays a list of all stashed changes.

## **Navigating Commits**

### **Switch to Master Branch**

```bash
git checkout master
```

Switches back to the **`master`** branch if you are lost in previous commits.

### **View Reflog**

```bash
git reflog
```

Shows a log of all actions and changes in the repository, useful for recovering lost commits.

### **Rebase on Master**

```bash
git rebase master
```

Rebases the current branch onto **`master`**. This should not be used on **`master`** itself.

## **SSH Key Setup for GitHub**

**Generate a New SSH Key and Add It to the SSH Agent**
Follow the [GitHub documentation](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) for detailed steps:

- Generate an SSH key.
- Add the SSH key to the SSH agent.

## **Repository Management**

### **Create a New Repository**

### **On the Command Line**

```bash
echo "# RepositoryName" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin "repo link"
git push -u origin main
```

### **Add an Existing Repository**

### **From the Command Line**

```bash
git remote add origin "repo link"
git branch -M main
git push -u origin main
```

### **View Remote Repositories**

```bash
git remote -v
```

Displays the URLs of remote repositories associated with the local repository.

### **Push Changes**

```bash
git push
```

Uploads local repository changes to a remote repository.

### **Clone a Repository**

```bash
git clone "repo link"
```

Creates a copy of an existing repository.

### **Pull Changes**

```bash
git pull
```

Fetches and merges changes from the remote repository to the local repository.

### **Fetch Changes**

```bash
git fetch
```

Downloads objects and refs from another repository.

Note: **`git fetch`** is equivalent to **`git pull`** followed by **`git merge`**.

## **Summary**

This documentation provides a comprehensive guide to using various Git commands for basic operations, configuring user information, branching, merging, viewing differences, stashing changes, navigating commits, setting up SSH keys, managing repositories, and performing essential Git operations. These commands form the foundation for effective Git version control.
