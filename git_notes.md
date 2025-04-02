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

**Working directory :** Contains all the project files and folders, basically its our workbench.
**Staging area :** Its a place where we add or remove files, when we are preparing what we want to include in the next saved version of our project (next commit).
**Commit history :** A commit in Git is basically one version of a project. The commit history is where you can think of your commits existing.
**Local repository :** Place for storing the files with maintaining the versions of development.