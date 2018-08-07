# git-flow

## Init git-flow
```
$ git flow init

$ git branch
```

## Create a feature branch
```
$ git checkout develop
$ git checkout -b feature/feature_branch

$ git flow feature start feature_branch
```

## Finish a feature branch
```
$ git checkout develop
$ git merge feature/feature_branch
$ git branch -d feature/feature_branch

$ git flow feature finish feature_branch
```

## Release branch
```
$ git checkout develop
$ git checkout -b release/0.1.0

$ git flow release start 0.1.0
```

## Finish release branch
```
$ git checkout develop
$ git merge release/0.1.0

$ git checkout master
$ git checkout merge release/0.1.0
$ git flow release finish '0.1.0'
```

## Hotfix branch
```
$ git checkout master
$ git checkout -b hotfix_branch

$ git flow hotfix start hotfix_branch
```

## Finish hotfix branch
```
$ git checkout master
$ git merge hotfix_branch
$ git checkout deveop
$ git merge hofix_branch
$ git branch -D hotfix_branch

$ git flow hotfix finish hotfix_branch
```

## Reference
  * https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow
  * http://woowabros.github.io/experience/2017/10/30/baemin-mobile-git-branch-strategy.html
