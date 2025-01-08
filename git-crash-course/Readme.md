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

> You'll need to generate a Person Access Token (PAT)
https://github.com/settings/personal-access-tokens

You will use the PAT as your password when you login

- Give it access to Contents for Commits

### SSH

```sh
git@github.com:Random-Dump/Github-Foundations-Doodle.git
cd Github-Foundations-Doodle
```

We will need to create our own SSH rsa key pair
```sh
ssh-keygen -t rsa
eval `ssh-agent`
ssh-add /home/codespace/.ssh/id_rsa
```

We can test our connection here:
```sh
ssh -T git@github.com
```

### Github CLI

Install the CLI
eg. Linux (Ubuntu)
```sh
(type -p wget >/dev/null || (sudo apt update && sudo apt-get install wget -y)) \
	&& sudo mkdir -p -m 755 /etc/apt/keyrings \
        && out=$(mktemp) && wget -nv -O$out https://cli.github.com/packages/githubcli-archive-keyring.gpg \
        && cat $out | sudo tee /etc/apt/keyrings/githubcli-archive-keyring.gpg > /dev/null \
	&& sudo chmod go+r /etc/apt/keyrings/githubcli-archive-keyring.gpg \
	&& echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null \
	&& sudo apt update \
	&& sudo apt install gh -y
```

```sh
gh auth login
gh repo clone Random-Dump/Github-Foundations-Doodle
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

List of branches
```sh
git branch
```

Create a new branch
```sh
git branch branch-name
```

Check out (switch) the branch
```
git checkout dev
```

## Remotes 

We can add remote but often you will just add remote via upstream when ading a branch

```sh
git remote add ...
git branch -u origin new-feature
```

## Stashing

```sh
git stash list
git stash
git stash save my-name
git stash apply
git stash pop
```

## Merging

```sh
git checkout dev
git merge main 
```

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