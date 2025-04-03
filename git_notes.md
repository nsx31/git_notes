# Configuring Username and Email : 
First step of getting started with git is to setup the usename and useremail, which will be used to identify who made what changes. 

```sh
git config --global user.name "nikhil kumar"
git config --global user.email "nikhilkumar31@outlook.com"
```

# Initializing Git : 
Second step involves initializing git inside the project directory so that git can track the changes made in the project and maintain multiple versions of it. 

```sh
git init
```

# Git Important Areas : 
1. Working directory.
2. Staging area.
3. Comment history.
4. Local repository.

<br>

- **Working directory :** Contains all the project files and folders, basically its our workbench. 
- **Staging area :** Its a place where we add or remove files, when we are preparing what we want to include in the next saved version of our project (next commit).
- **Commit history :** A commit in Git is basically one version of a project. The commit history is where you can think of your commits existing.
- **Local repository :** Place for storing the files with maintaining the versions of development.

# Making A Commit : 
Making a commit in Git is a two-step process. First, we add the files to the staging area, then we run the commit command and provide a commit message.

```sh
# to add all files to the staging area
git add -A 

# add specific files to the staging area
git add file1 file2 files3

# making a commit
git commit -m "enter commit message here inside the double quotes"
```

# Status & Log : 
To check the current status of staging area and working directory we ue below command : 

```sh
git status
```

To check the commit history we use this command :
```sh
git log
```

# Git Branch :
**List all local branches :**

```sh
git branch
```

**Create a new local branch :**

```sh
git branch <branch_Name_Here>
```

**Switch to different local branch :**

```sh
git switch <enter_branch_name_you_want_to_switch_to>
```

**Renaming a local branch :** First switch to that branch you want to rename and then run this command :
```sh
git branch -m <enter_new_name_here>
```

# Merging :
There are two types of merge in git : 
1. Fast forward merge 
2. Three way merge

To perform both types of merges, we first need to switch to the branch that we want our feature branch to merge into. In the case of a fast-forward merge, we don’t need to write a merge message whereas in the case of a three-way merge, we have to write a merge message. When performing a three-way merge, you typically don’t need to run `git add` manually unless there are conflicts.

**Fast forward merge :** no new commits were made on the main branch since the feature branch started.

```sh
git switch main
git merge features
```

**Three way merge :** Occurs when both the main branch and the feature branch have diverged (i.e., new commits exist in both branches)

```sh
git switch main 
git merge features

# if confict arises resolve that conflict then run
git add -A
git commit -m "merged feature branch with main branch"
```

# Pushing to Remote Repository :
A local repository can communicate with a remote repository when the local repository has a connection to the remote repository stored within it.

```sh
git remote add <enter_short_name> <enter_remote_repo_address>

# Example 
git remote add rb https://github.com/gitlearningjourneyrainbow-remote.git
```

To push a local branch to your remote repository, you will use the `git push` command and pass in the shortname for the remote repository and the name of the branch that you want to push

```sh
git push <enter_short_name_here> <branch_name>

# Example 
# here i am pushing my feature branch to remote repo
git push rb feature
```