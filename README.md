# Git Extensions

This project contains some Git extensions I've found useful to expedite my daily Git workflow. I hope they'll be useful for you as well.

## Installation

1. Clone or download repository.
2. Add scripts folder to PATH.
3. From Git Bash, issue a command like:

```sh
$ git latest
```

## Commands

#### git latest

This command has been useful for me in updating pending pull requests when subsequent merges to the target branch have been made. This command attempts to merge the latest changes from the target branch and then pushes the source branch to remote. There are several checks to ensure we're not breaking anything along the way.

This will merge the latest target branch features into your current Git branch.

```sh
$ git latest
```

This will merge the latest target branch features into feature/some-branch, regardless of what branch you haver checked out.

```sh
$ git latest feature/some-branch
```

#### git tidy

This command has been useful in clearing old branches from my local machine. It will not delete branches named "master" or "development", and will not delete your currently checked out branch.

This is equivalent to running git branch -d feature/your-branch on all local branches.

```sh
$ git tidy
```

This is equivalent to running git branch -D feature/your-branch on all local branches. _Warning: It will force delete all branches._

```sh
$ git tidy -D
```
