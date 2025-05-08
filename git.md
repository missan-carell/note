[toc]

# git 学习

```bash
git clone ssh://hostname/repo.git　  # 从某个仓库拉下所有代码
git pull                            # 从远程仓库拉取变更到本地
git push                            # 推送变更到到远程仓库
git 								# 缓存

git status                          # 查看当前变更
git checkout -- <filename>          # 撤销变更
git restore <filename>			    # 撤销变更
git add <filename>                  # 添加文件
git rm <filename>                   # 删除文件
git commit -m"变更说明"                 # 提交变更到本地仓库

git branch                          # 查看分支
git checkout <branch-name>          # 切换分支
git checkout -b <branch-name>       # 创建新分支

git log                             # 查看变更日志
git diff <filename>                 # 查看变更日志
```

## 1.1 上传笔记

上传笔记前先看[1.2 下载笔记](#1.2 下载笔记)前两步内容

1. 在typora的偏好设置-- 图像里勾选以下选项：

<img src="./.assets/image-20250507204946132.png" alt="image-20250507204946132" style="zoom: 50%;" />

注意，如果上传多个笔记，建议把图像上传到同一个文件夹

如果笔记内有图片不在指定的文件夹：

- ctrl+/ ，进入代码模式，把图片链接里的路径选择，修改成指定文件夹的路径
- 把错误文件夹里的图片剪切到目标文件夹，删除多余文件夹

2. 在gitbash里cd到笔记所在路径

   （注意gitbash切到盘内不需要加：）

3. `git status` 查看更改过的笔记（红色）

4. `git add 笔记名 ` 

   把红色的笔记名增加上去

   如果有多个图片，则通过：`git add .assets/*` 即可一起增加

5. 再次`git status` 检查是否有遗漏笔记

6. `git commit -m "修改内容"`

   此处如果是新电脑，则需要根据提示提供用户信息

   ```bash
   git config --global user.email "you@example.com"
   git config --global user.name "Your Name"
   ```

7. `git push `把新增笔记内容上传到github



## 1.2 下载笔记

1. 进入gitbash
2. ssh-keygen 获取本电脑公钥
3. 复制获取内容，登录到github上 -- setting --SSH and GPG keys ---选择new ssh key--- 将刚才复制内容黏贴进去

- 如果ssh-keygen获取的内容不是ssh-rsa开头，则cat ~/.ssh/id_ed25519.pub，复制内容，执行上述步骤

- RSA 生成的密钥长度比较长，而ECDSA 或 ECD2559 生成的会很短。所以现在很多系统都在用 ECDSA 或 ECD2559 

3. git clone git@github.com:

​	clone 后面的是自己的gihub链接，通过下图方式查看

![image-20250506175942116](.assets/image-20250506175942116.png)
