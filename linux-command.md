#通过inum删除文件（文件名出现乱码时用inum删除）
[yanshebo@BJHC4-Client-176119 nrt]$ ls -li
total 21584
3560352 -rw-r--r-- 1 yanshebo yanshebo 22098742 Nov 30  2017 nrt-up-result-reader.jar
[yanshebo@BJHC4-Client-176119 nrt]$ find . -inum 3560352
./nrt-up-result-reader.jar
[yanshebo@BJHC4-Client-176119 nrt]$ find . -inum 3560352|xargs rm


