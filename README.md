# github-cheat-sheet

## submodule
```
$ git submodule add <repo> <destination-dir>

Ex. Under "pose_estimation/" directory
$ git submodule add https://github.com/SeoHyeonDeok/caffe2tf.git ./caffe2tf
```

## revert push(origin), commit(local)
```
Undo <commit_id> and go to before(^) push of <commit_id> on remote repo, not local
$ git push -f origin <commit_id>^:master  # commit ID (SHA-1 hash)

Get back to previous commit on local (preserving working tree)
# git reset --soft <commit_id>

Get back to previous commit on local (remove working tree)
git reset --hard HEAD^
```

## branch management
* See all branches
```
$ git branch
```
* Create a branch 
```
$ git checkout -b develop
```
* Change working branch
```
$ git checkout <branch-name>
```
* Push the new branch to github
```
$ git push <remote> <branch-name>
```
* Update branch from remote repo
```
$ git fetch <remote> <branch-name>
$ git checkout FETCH_HEAD
$ git merge <remote>/<branch-name>
or 
$ git pull <remote> <branch-name>
```
* Remove local brach
```
$ git checkout test
$ git checkout develop
$ git branch -d test

$ git branch
```
* Remove remote branch
```
$ git branch -d <branch-name>

$ git push origin :<branch-name>
or
$ git push origin --delete <branch-name>
```
* Merge branch
```
$ git checkout master
$ git pull origin master
$ git merge --no-ff  develop
$ git push
```
