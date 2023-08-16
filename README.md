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