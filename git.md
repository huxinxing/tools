# Git相关基本操作

- 创建版本库：

  git init

- 添加的文件到暂存区和提交到仓库

  git add、git commit -m "xxxx";

- 查看历史版本

  git log 或者 git log --pretty=oneline

- 版本回退

  git reset --hard HEAD^退回到上一个版本   HEAD^^表示上上个版本

  git reset --hard 3628164  表示退回到3628164这个版本号。查看版本号可以用git log

  git reflog 查看命令历史

- 丢弃工作区的修改

  git checkout -- file   比如：git checkout -- readme.txt 为丢弃readme.txt中的修改内容

  git reset HEAD file 可以把暂存区的修改撤销掉

- 删除一个文件git rm test.txt

- 和github关联

  关联github:git remote add origin "远程仓库地址"

  推送本地仓库至远程仓库：git push -u origin master    如果发生错误表示远程仓库和本地仓库不一样导致解决方式：git pull --rebase origin master

  注意:在关联本地仓库和远程仓库的时候需要在github中设置ssh，  命令如下:cd ~ ; vim .ssh; 

  从远程仓库克隆:git clone "远程仓库地址"