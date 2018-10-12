# awk

*[内容摘自网络](https://www.cnblogs.com/emanlee/p/3327576.html)*

**变量名    含义** 
ARGC   命令行变元个数 
ARGV   命令行变元数组 
FILENAME   当前输入文件名 
FNR   当前文件中的记录号 
**FS**   输入域分隔符，默认为一个空格 
RS   输入记录分隔符 
NF   当前记录里域个数 
NR   到目前为止记录数 
**OFS**   输出域分隔符 
ORS   输出记录分隔符

##分割列

```shell
awk -F '\t' '{print $1,$2}' file
```

用*TAB*分割后打印第一、二个域.

##if判断

```shell
date +%m | awk '{if($1=='03' || $1 == '04' || $1 == '05') {print 1} else if ($1=='06' || $1 == '07' || $1 == '08') {print 2} else if ($1=='09' || $1 == '10' || $1 == '11') {print 3} else {print 4}}' 
```

用日期月份判断季度

## print域及参数

```shell
awk '{print NR,NF,$1,$NF}' file
```

显示文件file的当前记录号、域数和每一行的第一个和最后一个域。

##匹配行

````shell
awk '/101/' file
````

显示文件file中包含101的匹配行.

##filter

```shell
df | awk '$4>1000000 ' 
```

通过管道符获得输入，如：显示第4个域满足条件的行.





