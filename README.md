## 在Windows环境中安装git

网址：https://git-for-windows.github.io/ ，一路默认OK即可。



## 配置身份

首先第一件事打开Git Bash, 输入一下命令，提交的时候识别身份

```bash
git config -global user.name "Jingwei Zhang"
git config -global user.email "zhangjingwei@seu.edu.cn"
```



## Github上的准备工作

在Github上新建一个仓库（Repository），注意不要带有README.md的



## 常用git命令

- git clone git地址

  指定branch

  git clone -b zjw https://github.com/seujingwei/DPU-PYNQ.git

- git add 文件或目录

  把所有文件都加进去

  git add .

- git rm 文件或目录

  删除所有文件

  git rm -r .

  删除暂存区的文件

  git rm --cached 文件

- git checkout -- 文件

  回退文件

- git commit -m '备注说明'

  修改暂存区的文件，并打上备注

- git reset HEAD或版本号

  版本号看 reflog的记录，并且reset之后，数据是存在暂存区的，需要重新commit

- git reflog  

  看记录

- git log

- git status

  看暂存区的修改文件 

- git branch 分支名称

  新建branch

  git branch zjw

  删除branch

  git branch -d zjw

  查看所有的branch包含远程仓库的

  git branch -a

- git branch --set-upstream-to=origin/分支名称 分支名称

- git checkout 分支名称

  跳转到对应分支

  git checkout zjw

- git checkout -b 分支名称 origin/分支名称

- git diff 版本1 版本2

- git merge 分支名称

  把分支合并

- git pull  从服务器获取代码

  相当于fetch + merge

  fetch是可以指定分支存到temp

  git fetch origin master:temp

- git push origin 分支名称

  -f可以强推但不推荐，最好使用其他分支保存，然后再推 

- git tag 标签名称

- git stash

- git remote -v  查看当前远程库的地址

- git remote set-url origin ip地址  修改远程本地仓库的仓库地址



## 参考网址

同步项目到远程并解决冲突：

https://www.cnblogs.com/yehaia1/archive/2019/04/16/10715741.html

远程同步到本地：（是周期性同步而不是每次都clone，做法是通过fetch到temp，然后对操作分支进行merge）

https://blog.csdn.net/s740556472/article/details/80087026?utm_medium=distribute.pc_aggpage_search_result.none-task-blog-2~all~first_rank_v2~rank_v28-1-80087026.nonecase&utm_term=github%E6%8B%89%E5%8F%96%E5%85%B6%E4%BB%96%E5%88%86%E6%94%AF%E6%9C%80%E6%96%B0%E4%BB%A3%E7%A0%81&spm=1000.2123.3001.4430

Git简单教程：

https://blog.csdn.net/qq_30848071/article/details/79460081