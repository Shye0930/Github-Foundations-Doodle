## Github Hidden Folder

There is a hidden folder called `.git` which tells you that our project is a git rpo.

If we wanted to create a git repo in a new project we create the folder and then initialize that ro using `git init`

```sh
mkdir /workspaces/tmp/new-project
cd /workspaces/tmp/new-project
git init
touch Readme.md
code Readme.md
git status
git add Readme.md
# makes changes to readme.md
git commit -a -m "add readme file"
```

## Cloning

3 ways to clone: HTTPS, SSH, Github CLI

Since we are using Github Codespaces we'll create tmp directory in our workspace
```sh
mkdir /workspaces/tmp
cd /workspaces/tmp
```

### HTTPS

```sh
git clone https://github.com/Random-Dump/Github-Foundations-Doodle.git
cd Github-Foundations-Doodle
```

## Commits

When we want to commit code we can write git commit which will open the commit edit message in the editor of choice

```sh
git commit
```

Set the global editor
```sh
git config --global core.editor emacs
```

Make a commit and commit message without opening an editor
```sh
git commit -m "add message here"
```

## Branches

## Stashing

## Merging

## Add 

When we want to stage changes that will be included in the commit we can use the `.` to add all the possible files

## Reset

Reset allows you to move Staged changes to be unstaged.
This is useful when you want to revert all files not to be committed

```sh
git add .
git reset
```

> git reset will revert a `git add .`

## Status

Git status shwos you what files will or will not be committed.

```sh
git status
```
## Git config file

The gitconfig file is what stores your global configurations for git such as email, name, editor, etc.

Showing the content of our .gitconfig file
```sh
git config --list
```

When you first install Git on a machine you are suppose to set up your name and email
```sh
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

## Log

git log will show recent git commits to the git tree

## Push

When we want to push a repo to our remote origin

```sh
git push
```