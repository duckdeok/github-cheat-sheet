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

