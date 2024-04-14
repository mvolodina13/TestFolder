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