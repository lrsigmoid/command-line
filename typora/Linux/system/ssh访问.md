##设置机器A访问机器B

- A机器生成公钥：ssh-keygen

- 两台机器用户名相同

- 将私钥id_rsa权限设置为你600（最少是600权限）

- 将A机器下的公钥（~/.ssh/id_rsa.pub）中的内容copy进B机器（~/.ssh/authorized_keys）

- 在A机器执行ssh B.IP

---

##批量获取公钥：

```shell
array_ip=('10.196.32.197' '10.196.33.4' '10.196.33.35' '10.196.33.67' '10.196.33.3' '10.196.33.66' '10.196.33.5' '10.196.32.164' '10.196.32.194' '10.196.32.228')
ip_cnt=${#array_ip[@]}
gpu_dir=/export/sdb/home/recpro/script/background_white
for ((i=0;i<$ip_cnt;i++))
{
    scp ${array_ip[$i]}:~/.ssh/id_rsa.pub ./
    cat id_rsa.pub >> authorized_keys
    /bin/rm id_rsa.pub
}
```













