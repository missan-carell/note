[toc]

# git 学习

```bash
git clone ssh://hostname/repo.git　  # 从某个仓库拉下所有代码
git pull                            # 从远程仓库拉取变更到本地
git push                            # 推送变更到到远程仓库

git status                          # 查看当前变更
git checkout -- <filename>          # 撤销变更
git restore <filename>			    # 撤销变更
git add <filename>                  # 添加文件
git rm <filename>                   # 删除文件
git commit "变更说明"                 # 提交变更到本地仓库

git branch                          # 查看分支
git checkout <branch-name>          # 切换分支
git checkout -b <branch-name>       # 创建新分支

git log                             # 查看变更日志
git diff <filename>                 # 查看变更日志
```

