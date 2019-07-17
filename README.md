# 简易流程总结
1. 在 github上新建一个仓库，并添加README.md
2. 在本地新建一个文件夹
3. 使用 git init 初始化本地仓库
4. 使用 git remote add origin git@github.com:xhwhust/(仓库名).git 连接到远程仓库
5. 使用 git pull origin master --allow-unrelated-histories 把远程仓库同步到本地
6. git add *
7. git commit -m 'info'
8. 使用 git push -u origin master首次推送
9. 使用 git push origin master推送

# 创建本地仓库（工作区）
* 在仓库目录下启动git bash或者用cd命令使其在仓库目录下
* 使用命令git init初始化仓库，会生成隐藏文件夹.git
# 添加文件
* git add (filename) 把文件添加到暂存库
* git commit -m '备注' 把文件提交到仓库
# 版本回退
* git reset --hard HEAD^ HEAD指向的是当前版本的id
* git reset --hard commit_id 通用命令
# 撤销修改
* git checkout -- (filename)
* 命令git checkout -- readme.txt意思就是，把readme.txt文件在工作区的修改全部撤销，这里有两种情况：
* 一种是readme.txt自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；
* 一种是readme.txt已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。
* 总之，就是让这个文件回到最近一次git commit或git add时的状态
# 删除文件
* rm (filename) 删除本地文件
* git rm (filename)
* git commit -m '备注'
# 远程仓库
* git remote add origin git@github.com:xhwhust/(filename).git
* git push -u origin master 首次推送
* git push origin master 以后每次推送可以使用这个命令
   ## 问题
   * 如果新建仓库有README.md,本地仓库没有,推送之前需要先拉取
   * git pull origin master --allow-unrelated-histories
   * 再使用git push origin master
# 克隆仓库
* git clone git@github.com:xhwhust/(filename).git  通过ssh支持的原生git协议速度最快
* git clone https://github.com/xhwhust/(filename).git https协议速度慢
* 克隆后会在当前git bash路径下生成本地仓库
# 分支管理
* git checkout -b (branchname) 产生并切换至分支等于以下两条命令
* git branch (branchname) 产生分支
* git checkout (branchname) 切换分支
* git merge (branchname) 合并分支成果到master
* git branch -d (branchname) 删除分支
* git branch 查询分支
# 查询
* git status 当前状态
* git log 提交记录
* git reflog 版本回退记录
* git diff 
* cat (filename) 文件内容
