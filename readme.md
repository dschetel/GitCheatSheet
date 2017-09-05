# Git Cheat Sheet
>Git Cheat sheet in all its glory..!

> [Download Cheat sheet](git_cheat_sheet.pdf)

## Table of contents
- [Create a repo](#create-a-repo)
  - [From existing project](#from-existing-project)
  - [From existing remote repo](#from-existing-repo)
- [Branching](#branching)
  - [Merge branch B1 into branch B2](#merge-branch-B1-into-branch-B2)
  - [How to resolve merge conflicts](#how-to-resolve-merge-conflicts)
- [Log](#log)
- [Diff](#diff)
  - [diff word-by-word](#diff-word-by-word)
  - [List every changed file between two commits](#list-every-changed-file-between-two-commits)
- [How to get private repos](#how-to-get-private-repos)


## Scenarios
Some scenarios with a bit more explicit commands

### Create a repo

#### From existing project

```bash
cd ~/projects/myproject
git init
touch .gitignore
> use http://www.gitignore.io
git add .gitignore
git commit -m 'added gitignore'
git add .
git commit -m 'initial commit'
```

#### From existing repo
```bash
git clone ~/existing/repo
git clone http://remoteRepository/project.git
```

### Branching

#### Merge branch B1 into branch B2

```bash
git checkout B2
git merge B1
```

#### How to resolve merge conflicts

- Start merge (git merge)
- Use editor to search for merge conflict (HEAD)
- Resolve conflicts
- git commit


### Log

```bash
git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit
```

```bash
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"
git lg
```

### Diff

#### Diff word-by-word

```bash
git diff --word-diff
```

#### List every changed file between two commits

```bash
git diff --name-only <commit-hash> <commit-hash>
```



### How to get private repos

1. Register at gitub using your @uke.de email
2. Go to https://education.github.com/discount_requests/new
3. Apply for a student pack
