
# Resources

## git config

when first setting up git, you'll need to work with the config commands in order to set up your identity.
For example, your identity can be set up with the commands such as:
```
git config --global user.name "Arnold Shortman"
git config --global user.email arnoldshortman202@gmail.com
```
- [Git Config Documentation](https://git-scm.com/docs/git-config)
---

## git init

the "git init" command is used to create an empty git repository.

- [Git Init Documentation](https://git-scm.com/docs/git-init)
---

## git add

When changes have been made inside a git repository that you want to keep, you'll need to use the "git add" command. Items that have not been "tracked" before will start to be tracked and all other changes will be marked as modified. Generally, you can get away with the git command "git add  ." which will add All files and directories that were added, changed, or deleted. You can track changes to specific files using "git add file1 file2" which will track specifically file1 and file2. You can specify tracking directories with "git add DirectoryName".

- [Git Add Documentation](https://git-scm.com/docs/git-add)

## git commit

The command "git commit" will take all tracked changes (items added with [git add](./ADD)) and package them up in what is called a commit. Commits come with commit messages that are required for each commit. You add a message to a commit command by using the "-m" flag followed by a message in quotes. A commit message _can_ be anything, but best practice dictates that you should use that message to indicate the changes included in the commit.
For example, if we have an application we're working on where we just build out the ability to register neew accounts, then you might have some variation of the following:
```
git add . 
git commit -m "Added register functionality"
```
then when using the history of a git repository, you can pinpoint where the registration functionality was added.

- [Git Commit Documentation](https://git-scm.com/docs/git-commit)
---

## git remote

When working with git, a **remote** is any git repository that is not on the machine you're working on. The counterpart to this is the **local**, or the machine that is being developed on. Take GitHub for example. While git is the technology that allows you to create local repositories, Github is the site that will host your remote repositories. Once stored remotely, you can bring that repository back down or share it with others. **Note**: While the repositories (local and remote) are related and track the same project, they can have different states if changes are not shared between the two.

### Adding a remote

A remote can be added with the "git remote add" command, followed by the name and location of the remote. The name is a local name, meaning it's your label and does not impact the actual remote whatsoever.
```git remote add origin https://github.com/ElevenfiftyAcademy/GitFundamentals.git
```

### Removing a remote

A remote can be removed with the "git remote remove" command, followed by the name of the remote.
```
git remote remove origin
```

- [Git Remote Documentation](https://git-scm.com/docs/git-remote)
---

## git push

When you have a [remote](./REMOTE.md) set up you'll need to begin to move [commits](./COMMIT.md) to the remote. This can be done with the command "git push". You can attach a name to your command to specify where you're pushing to.
```
git push origin main
```
This command will push the **main** branch to the remote called **origin**. This means any commits that are in your local will be **pushed** to the remote.

### Upstream Tracking

Instead of including the name of the remote and the branch you're on every time, you can set local branches to track an upstream branch. This means you can tell the branch to push its assigned upstream remote branch by using the command "git push". Before doing so, you'll need to use the "-u" or "--set-upstream" flag.
```
git push -u origin main
```
After this command is used, you can just use "git push" and it will function the same way.

- [Git Push Documentation](https://git-scm.com/docs/git-push)
---

## git pull

Similiar to a [git push](./PUSH.md), a "git pull" will interact with a remote repository. Only this time it will **pull** the changes it does not have from the remote down to the local repository. This means any commits made that are on the remote repository will be pulled down and added to the local repository. This can be done by adding the remote name and branch name:
```
git pull origin main
```
If there is any upstream connection established, you can use "git pull" without specifying a remote or branch.

- [Git Pull Documentation](https://git-scm.com/docs/git-pull)
---

## git Status 

The command "git status" is extremely helpful when it comes to checking on the, you guessed it, staus of your repository. Using "git status" will show you what changes are veing tracked, aren't being tracked, what commits need to be pushed/pulled, etc. It is exactly what it sounds like, a status check. It's a command that is safe to use at any time. If you want to see what is going on it's good to use "git status" inbetween commands until you get to know the flow better.
```
git add .
git status

git commit -m "Modified landing page"
git status

git push
git status
```

-[Git Status Documentation](https://git-scm.com/docs/git-status)
---

## git clone 

Cloning a repository is the act of creating a new directory and an associated copy of the remote repository. It will be a clone, meaning it has all tracked commits and commit history. It will also be associated with the remote, meaning that you can use the "git pull" command to pull updated from the original repository. It can be done with the "git clone" command as seen here:
```
git clone https://github.com/ElevenfiftyAcademy/TerminalDungeon.git
```

-[Git Clone Documentation](https://git-scm.com/docs/git-clone)
---

## External Resources

- [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/)
- [git Documentation](https://git-scm.com/docs)
- [gitignore Documentation](https://git-scm.com/docs/gitignore)
- [git Branches](https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell)

























[Back to home](../README.md)

