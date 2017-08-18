# Git Cheat Sheet
Git Cheat sheet in all its glory..!

[Download Cheat sheet](git_cheat_sheet.pdf)

## Scenarios
Some scenarios with a bit more explicit commands

### Create a repo

#### From existing data

````
cd ~/projects/myproject
git init
git add .
git commit -m 'initial commit'
````

#### From existing repo
````
git clone ~/existing/repo
git clone http://remoteRepository/project.git
````

### Branching

#### Merge branch B1 into branch B2

````
git checkout B2
git merge B1
````
