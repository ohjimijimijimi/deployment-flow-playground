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
git commit 

# fix your code 
git commit

# push the changes so they get reviewed
git push -u origin <hotfix>

# create PR to master to reviwe the change
# don't merge it on GitHub

# when it's reviewed, finish the hotfix. 
# you can use --squash to keep master clean
git flow hotfix finish --squash <hotfix>

# sync the branches 
git push 
git checkout master 
git push && git push --tags
```

