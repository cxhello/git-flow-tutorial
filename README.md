# git-flow-tutorial

## 初始化&创建develop分支

```shell
mkdir git-flow-tutorial
cd git-flow-tutorial
git init
git checkout -b develop
git add README.md
git commit -m "Initial commit"
git remote add origin https://github.com/cxhello/git-flow-tutorial.git
git push -u origin develop
```

## 开始新feature开发

```shell
git checkout -b feature_git_flow_example develop
git add README.md feature_git_flow_example_1.txt
git commit -m "feature_git_flow_example_1 finished"
git push -u origin feature_git_flow_example
```

## 继续开发新feature

```shell
git add README.md feature_git_flow_example_2.txt
git commit -m "feature_git_flow_example_2 finished"
git push -u origin feature_git_flow_example
```

## 本次feature开发完成

```shell
git add README.md
git commit -m "feature_git_flow_example finished"
git push -u origin feature_git_flow_example

git pull origin develop
git checkout develop
git merge --no-ff feature_git_flow_example
git push origin develop
```

## 准备release分支

```shell
git checkout -b v0.1 develop
git push origin v0.1
```

## 将release分支合并到master主分支

```shell
git checkout -b master v0.1
git push origin master
```

## 打版本号标签

```shell
git tag -a v0.1 master
git push --tags
```

## 同时将release分支合并到develop主分支

```shell
git checkout develop
git merge --no-ff v0.1
git push origin develop
```

## 根据实际情况删除feature分支

```shell
git branch -d feature_git_flow_example
git push origin --delete feature_git_flow_example
```