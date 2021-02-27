## IK分词器

https://www.cnblogs.com/flower-dance/p/13645576.html

什么是IK分词器?

分词:即把一段中文或者别的划分成一个个的关键字,我们在搜索时候会把自己的信息进行分词,会把数据库中或者索引库中的数据进行分词,然后进行一个匹配操作,默认的中文分词器是将每个字看成一个词,比如"我爱技术"会被分为"我","爱","技","术",这显然不符合要求,所以我们需要安装中文分词器IK来解决这个问题

IK提供了两个分词算法:ik_smart和ik_max_word

其中ik_smart为最少切分,ik_max_word为最细粒度划分





## 安装 IK:

同样下载不说直接安装.记得版本相同

解压缩后拷贝到ElasticSearch的plugins文件夹下

![image-20210227155322989](C:\Users\19802\AppData\Roaming\Typora\typora-user-images\image-20210227155322989.png)



![image-20210227155342642](C:\Users\19802\AppData\Roaming\Typora\typora-user-images\image-20210227155342642.png)



![image-20210227155355651](C:\Users\19802\AppData\Roaming\Typora\typora-user-images\image-20210227155355651.png)

![image-20210227155412635](C:\Users\19802\AppData\Roaming\Typora\typora-user-images\image-20210227155412635.png)