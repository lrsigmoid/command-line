#git remove file 

$ git rm test.txt
rm 'test.txt'

$ git commit -m "remove test.txt"
[master d46f35e] remove test.txt
 1 file changed, 1 deletion(-)
 delete mode 100644 test.txt

$git push




#git add file

简要步骤如下：

登陆github，创建git仓库。或者github中已经有了一个git仓库（之前创建的，或者是从别人那fork出来的）。 
记此git仓库的地址为[github_repository_url]。

执行git clone [github_repository_url]，将github上的仓库克隆到本地。

进入到克隆的仓库目录 
注：如果进入的目录是很久之前克隆出来的，此时要先git pull以更新到github中的最新文件。

将修改的或者新加的文件放入克隆的仓库目录中

执行git add .将改动添加到本地仓库。

执行git commit -m [your_comment]将改动提交到本地仓库。

执行git push origin [your-branch]将本地的改动提交到github中。如果提交到主分支上，则[your-branch]为master。即执行git push origin master


#fatal: Not a git repository

我用git add file添加文件时出现这样错误：

fatal: Not a git repository (or any of the parent directories): .git

提示说没有.git这样一个目录，解决办法如下：

git init就可以了！


