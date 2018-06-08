1、需要记住所需恢复文件的名字和版本号(commit id)

     git checkout commit_id -- file_name

如果不加commit_id，那么git checkout -- file_name 表示恢复文件到本地版本库中最新的状态。

2、不需要记住所需恢复的文件名字。

采用git ls-files命令

要查看删除的文件： git ls-files --deleted

使用命令checkout来恢复：git checkout -- file_name

如果要恢复多个被删除的文件，可以使用批处理命令：

git ls-files -d | xargs git checkout --

如果要恢复被修改的文件，命令：git ls-files -m | xargs git checkout --


#Tips

1.git pull会使用git merge导致冲突，需要将冲突的文件resolve掉 git add -u, git commit之后才能成功pull.

2.如果想放弃本地的文件修改，可以使用git reset --hard FETCH_HEAD，FETCH_HEAD表示上一次成功git pull之后形成的commit点。然后git pull.

