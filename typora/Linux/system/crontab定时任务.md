#Linux crontab定时任务

*[Linux定时任务](https://www.cnblogs.com/mingforyou/p/3930636.html)*

为当前用户创建**cron**服务

* crontab -l

显示定时任务

* 键入 crontab  -e 编辑**crontab**服务文件

​      *例如* 文件内容如下：

```shell
0 9 * * * /home/recpro/chengsujun/search_index_builder/Data/index.sh >> /home/recpro/chengsujun/search_index_builder/Data/index.log 2>&1
```

```shell
30 3 * * * /home/recpro/on_line/script/background_white/fortress_run.sh >> /home/recpro/on_line/script/background_white/log/bgw.log 2>&1
```

​      **/bin/sh /home/admin/jiaoben/buy/deleteFile.sh** 这一字段可以设定你要执行的脚本，这里要注意一下**bin/sh** 是指运行  脚本的命令  后面一段时指脚本存放的路径



