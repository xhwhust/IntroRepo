# 创建本地仓库（工作区）
* 在仓库目录下启动git bash或者用cd命令使其在仓库目录下
* 使用命令git init初始化仓库，会生成隐藏文件夹.git
# 添加文件
* git add <filename> 把文件添加到暂存库
* git commit -m '备注' 把文件提交到仓库
# 版本回退
* git reset --hard HEAD^ HEAD指向的是当前版本的id
* git reset --hard commit_id 通用命令
# 撤销修改
* git checkout -- <filename>
* 命令git checkout -- readme.txt意思就是，把readme.txt文件在工作区的修改全部撤销，这里有两种情况：
* 一种是readme.txt自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；
* 一种是readme.txt已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。
* 总之，就是让这个文件回到最近一次git commit或git add时的状态
# 查询
* git status 当前状态
* git log 提交记录
* git reflog 版本回退记录
* git diff 
* cat <filename> 文件内容
