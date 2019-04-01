### This is an hotfix

### Flows

#### Using gitflow

```
# sync branches
git checkout staging
git pull
git checkout master 
git pull

# start the hotfix from master
git flow hotfix start <hotfix>

# fix your code
git commit -m "fix 1"

# fix your code 
git commit -m "fix 2"

# push the changes so they get reviewed
git push -u origin <hotfix>

# create PR to master to reviwe the change
# don't merge it on GitHub

# when it's reviewed, finish the hotfix. 
# you can use --squash to keep master clean
git flow hotfix finish --squash <hotfix>

# sync the remote branches 
git push 
git checkout master 
git push && git push --tags
```

#### Using GitHub
```
# sync branches
git checkout staging
git pull
git checkout master
git pull

# git checkout -b hotfix/<hotfix>

# fix your code
git commit -m "fix 1"

# fix your code 
git commit -m "fix 2"

# push changes
git push -u orign hotfix/<hotfix>

# create a PR to master so the code can be reviews

# merge the PR using a squash merge so master is kept clean

# create a new hotfix release from GitHub

# sync your local repoo
git checkout master && git pull
git checkout develop && git pull
git checkout staging && git pull
```
