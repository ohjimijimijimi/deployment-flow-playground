### Description 

To keep a clean `staging` branch we can squash the merges we do on it. 

The operation flows is the following:

### Flows

#### Using gitflow

```
# align the branches
git checkout master && git pull
git checkout develop && git pull
git checkout staging && git pull

# starting a new feature branch
git flow feature start <feature>

# work...
git commit -m "message 1"
# work...
git commit -m "message 2"
# work...
git commit -m "message 3"
# work...
git commit -m "message 4"
# work...
git commit -m "message 5"

# push the feature branch to remote
git push

# create PR for develop so the code can be reviewed

# merge the PR using a normal merge. This allows to keep the full history on develop

# wait for QA

# finish the feature squashing the changes
git flow feature finihsh --squash <feature>

# sync staging branch
git push

# release if requested
```

#### Without gitflow

```
# align the branches
git checkout master && git pull
git checkout develop && git pull
git checkout staging && git pull

# starting a new feature branch
git checkout -b feature/<feature>

# work...
git commit -m "message 1"
# work...§
git commit -m "message 2"
# work...
git commit -m "message 3"
# work...
git commit -m "message 4"
# work...
git commit -m "message 5"

# push the feature branch to remote
git push

# create PR for staging so the code can be reviewed

# merge the PR using a normal merge. This allows to keep the full history on develop

# create a new PR with base staging

# wait for QA

# finish the feature by using the squash merge feature of GitHub

# release if needed.
```
