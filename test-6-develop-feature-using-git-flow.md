Here's how to develop a new feature using git flow

### TODO
- Start a new feature (`git flow feature start <context>-<issue>-<description>`)
- Commit some code and push the branch
- Open a PR with base `develop` and assign a reviewer
- When reviewed, merge the changes
- Finish the feature (`git flow feature finish <context>-<issue>-<description>`)
- Wait until the `staging` QA phase is completed, then make a new release:
    ```
    git flow release start 2.0.0
    git flow release finish
    git push
    git checkout master
    git push && git push --tags
    ```

### git flow documetation
- repo: https://github.com/nvie/gitflow
- cheatsheet: https://danielkummer.github.io/git-flow-cheatsheet/
- tutorial: https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow

### git flow configuration

The only difference is that next release branch. Usually is mapped to `develop`. In our case we use `staging`.

```
Branch name for production releases: master
Branch name for "next release" development: staging
Feature branch prefix: feature/
Bugfix branch prefix: bugfix/
Release branch prefix: release/
Hotfix branch prefix: hotfix/
Support branch prefix: support/
Version tag prefix:
```
