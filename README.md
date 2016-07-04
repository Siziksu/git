# GIT

GIT quick reference.

## Configuration

#### Core editor

Install `Notepadd++` and set the core editor.

```
$ git config --global core.editor C:/Utils/Notepad++/notepad++.exe
```

#### Diff and Merge tool

Install `Meld` and edit the `.gitconfig` global file.

```
$ git config --global --edit
```

Add these entries.

```
[diff]
    tool = meld
    guitool = meld
[difftool "meld"]
    path = C:/Utils/Meld/Meld.exe
[difftool]
	prompt = false
[merge]
	tool = meld
[mergetool "meld"]
	path = C:/Utils/Meld/Meld.exe
```

Or execute this lines.

```
$ git config --global diff.tool "meld"
$ git config --global diff.guitool "meld"
$ git config --global difftool.meld.path "C:/Utils/Meld/Meld.exe"
$ git config --global difftool.prompt false

$ git config --global merge.tool "meld"
$ git config --global mergetool.meld.path "C:/Utils/Meld/Meld.exe"
```

To use this tool.

```
$ git difftool
```

#### Abort Command

To abort a command use `CTRL + C`.

#### Global user details

Display the global user name and email.

```
$ git config --global user.name
$ git config --global user.email
```

Set the local user name and email.

```
$ git config --global user.name "User Name"
$ git config --global user.email "user@email.com"
```

#### Local user details

Display the local user name and email.

```
$ git config user.name
$ git config user.email
```

Set the local user name and email.

```
$ git config user.name "User Name"
$ git config user.email "user@email.com"
```

## Commands

Display the config file.

```
$ git config --list

or

$ cat .git/config
```

See the changes.

```
$ git status
```

See the differences.

```
$ git diff
```

Add all the changes to be committed.

```
$ git add .
```

Revert changes made to your working copy.

```
$ git checkout .
```

Revert changes made to the index (i.e., that you have added). Warning this will reset all the unpushed commits to master.

```
$ git reset
```

Revert a change that have been committed.

```
$ git revert ...
```

Remove untracked files (e.g., new files, generated files).

```
$ git clean -f
```

Remove untracked directories (e.g., new or automatically generated directories).

```
$ git clean -fd
```

Apply the changes added with a description message.

```
$ git commit -m "first commit"
```

Send the changes to the remote repository.

```
$ git push origin master
```

List the existing branches.

```
$ git branch
```

Switch to a branch.

```
$ git checkout master
```

## Simple GIT workflow

```
$ git pull
    get all the changes from the remote repository
```
```
$ git checkout -b branch-name
    create a new branch to work in
```
```
$ git status
    see the changes
```
```
$ git diff
    see the differences in detail
```
```
$ git add .
    add all the changes to be committed
```
```
$ git commit -m "message"
    make the commit with a description message
```
```
$ git checkout master
    switch back to the master branch
```
```
$ git merge branch-name
    update the master branch with the branch-name work
```
```
$ git push origin master
    send the changes to the remote repository
```
