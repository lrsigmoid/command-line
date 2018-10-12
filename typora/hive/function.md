#Funtion

* bin

  bin(bigint)  返回string，将bigint转化成二进制字符串。

  ```sql
  select bin(123);
  ```

  1111011

* lpad

  lpad(string,int,string) 返回字符串，左补齐。

  ```sql
  select lpad('yanshebo',10,'a');
  ```

  aayanshebo

* rpad

  > 用法详见上

* get_json_object

  使用get_json_object函数解析json，字符串必须为标准json格式

  ```sql
  select get_json_object('{"content":{"img":"mobilecms/jfs/t2866/75/2672507126/159133/a6f9a7c2/576f69c6N85292901.jpg","price":"88.00","skuId":"1633829133","title":"倍晶 mac苹果macbook电脑air13笔记本pro13.3英寸外壳保护贴膜12贴纸 银上盖+底部+全托+键盘+高清+蓝膜+塞+清洁套装 老款15.4英寸Pro Retina"},"id":"332,333,0","type":"3"}','$.content.skuId');
  ```

  1633829133

* 

