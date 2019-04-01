### Descritption 

We want to keep the changes to `staging` so we navigate easily the history from our IDEs.
We want to keep master clean so we squash the release/hofixes.

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

# finish the feature 
git flow feature finish <feature>

# align the branches
git checkout master && git pull
git checkout develop && git pull
git checkout staging && git pull

# release if requested
git checkout staging
git flow release start <release>
git flow release finish --squash <release>

git push 
git checkout master 
git push && git push --tags
```
