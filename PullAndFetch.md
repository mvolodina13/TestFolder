# GIT FETCH vs. GIT FETCH


| Feature        | `git fetch`                                            | `git pull`                                                              |
|----------------|--------------------------------------------------------|-------------------------------------------------------------------------|
| Workflow       | Retrieves changes from remote repository               | Retrieves and merges changes from remote repository into current branch |
| Local Changes  | Does not modify working directory or current branch    | Automatically integrates fetched changes into current branch            |
| Safety         | Safer as it does not automatically modify local branch | Riskier as it directly modifies working directory and branch            |
| Flexibility    | More flexible, allows reviewing changes before merging | Less flexible, merges changes automatically                             |


![Not available!](https://itknowledgeexchange.techtarget.com/coffee-talk/files/2023/05/git-fetch-vs-merge.gif)

*A git pull operation is equivalent to a git fetch and merge*

# Documentation
* [Git Fetch](https://git-scm.com/docs/git-fetch)
* [Git Pull](https://git-scm.com/docs/git-pull)

# Amending Commit
The `git commit --amend` command is a convenient way to modify the most recent commit. It lets you combine staged changes with the previous commit instead of creating an entirely new commit. It can also be used to simply edit the previous commit message without changing its snapshot. But, amending does not just alter the most recent commit, it replaces it entirely, meaning **the amended commit will be a new entity with its own ref**. To Git, it will look like a brand new commit. There are a few common scenarios for using `git commit --amend`:

* **Change most recent Git commit message**
`git commit --amend`
Let's say you just committed and you made a mistake in your commit log message. Running this command when there is nothing staged lets you edit the previous commit’s message without altering its snapshot.

Premature commits happen all the time in the course of your everyday development. It’s easy to forget to stage a file or to format your commit message the wrong way. The `--amend` flag is a convenient way to fix these minor mistakes.

`git commit --amend -m "an updated commit message"`
Adding the `-m` option allows you to pass in a new message from the command line without being prompted to open an editor.

* **Changing committed files**
The following example demonstrates a common scenario in Git-based development. Let's say we've edited a few files that we would like to commit in a single snapshot, but then we forget to add one of the files the first time around. Fixing the error is simply a matter of staging the other file and committing with the `--amend` flag:

`# Edit hello.py and main.py
git add hello.py
git commit 
`# Realize you forgot to add the changes from main.py 
git add main.py 
git commit --amend --no-edit`

The `--no-edit` flag will allow you to make the amendment to your commit without changing its commit message. The resulting commit will replace the incomplete one, and it will look like we committed the changes to `hello.py` and `main.py` in a single snapshot.

