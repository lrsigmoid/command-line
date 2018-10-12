#grep

##在某路径下递归搜索包含某字符串的文件

语法：

```shell
grep -ri --include="*.sh" "tmp_high_value_user_add_cart_new" ./
```

```shell
grep -ri --include="*.sh" "tmp_high_value_user_item_visit_new" ./
```

参数：

-r 是递归查找，查找所有文件包含子目录

-i 忽略大小写

-n 是显示行号

-l 只列出匹配的文件名

--include:查找文件类型


