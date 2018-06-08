#通过inum删除文件（文件名出现乱码时用inum删除）
[lrsigmoid@BJHC4-Client-176119 nrt]$ ls -li
total 21584
3560352 -rw-r--r-- 1 lrsigmoid lrsigmoid 22098742 Nov 30  2017 nrt-up-result-reader.jar
[lrsigmoid@BJHC4-Client-176119 nrt]$ find . -inum 3560352
./nrt-up-result-reader.jar
[lrsigmoid@BJHC4-Client-176119 nrt]$ find . -inum 3560352|xargs rm


