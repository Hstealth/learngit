git  可以知道系统有没有安装git。                   
sudo apt-get install git 可以安装git
git config --global user.name "Your Name"
git config --global user.email "email@example.com"
注意git config命令的--global参数，用了这个参数，表示你这台机器上所有的Git仓库都会使用这个配置，当然也可以对某个仓库指定不同的用户名和Email地址
创建一个版本库非常简单，首先，选择一个合适的地方，创建一个空目录：
$ mkdir learngit
$ cd learngit
$ pwd
/Users/michael/learngi
瞬间Git就把仓库建好了，而且告诉你是一个空的仓库（empty Git repository），细心的读者可以发现当前目录下多了一个.git的目录，这个目录是Git来跟踪管理版本库的，没事千万不要手动修改这个目录里面的文件，不然改乱了，就把Git仓库给破坏了。
如果你没有看到.git目录，那是因为这个目录默认是隐藏的，用ls -ah命令就可以看见
运行git status命令看看结果：
git status命令可以让我们时刻掌握仓库当前的状态，上面的命令告诉我们，readme.txt被修改过了，但还没有准备提交的修改。
第一天上班时，已经记不清上次怎么修改的readme.txt，所以，需要用git diff这个命令看看：
$ git diff readme.txt 

$ git add readme.txt
同样没有任何输出。在执行第二步git commit之前，我们再运行git status看看当前仓库的状态：
git status告诉我们，将要被提交的修改包括readme.txt，下一步，就可以放心地提交了：提交后，我们再用git status命令看看仓库的当前状态：
Git告诉我们当前没有需要提交的修改，而且，工作目录是干净（working directory clean）的。
要随时掌握工作区的状态，使用git status命令。

如果git status告诉你有文件被修改过，用git diff可以查看修改内容。

