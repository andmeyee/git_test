# git_test

## Create new dev branch and use master as github status branch

Create dev branch from master branch

```shell
git checkout -b dev
```

Push branch to remote origin

```shell
git push origin dev
```

Make dev your default branch (in Bitbucket)

Delete master branch (in Bitbucket and local)

```shell
git branch -d master
```

Create new master branch without history and commit it

```shell
git checkout -b master <SHA from initial commit>
git merge --squash <branch>
git commit -m "your merge message"
```

Push new master

```shell
git push origin master
```

Set master to your default branch (in Bitbucket)

Add Github as remote target to master branch

```shell
git remote add -t master github_origin url
```

Push to Github

```shell
git push github_origin master
```

## merging with single commit



```shell
git checkout master
git merge --squash <feature branch>
git commit -m "your message"
```

