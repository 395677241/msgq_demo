（3）编译与执行程序

①    在当前目录下利用>msg.tmp建立空文件msg.tmp。

②    编译发送消息队列程序 gcc msgsnd.c -o  msgsnd。

③    执行./msgsnd，执行结果如下:

  ----- Message Queues --------

key        msqid      owner      perms      used-bytes   messages   

0x0101436d 294912     zjkf       600        1072         2          

④    编译接收消息程序 gcc msgrcv.c -o msgrcv

⑤    执行./msgrcv，执行结果如下:

 type=1,time=03:23:16, message=happy new year!

 

------ Message Queues --------

key        msqid      owner      perms      used-bytes   messages   

0x0101436d 294912     zjkf       600        536          1         

⑥    利用ipcrm -q 294912删除该消息队列。因为消息队列是随内核持续存在的，在程序中若不利用msgctl函数或在命令行用ipcrm命令显式地删除，该消息队列就一直存在于系统中。另外信号量和共享内存也是随内核持续存在的。

 

摘录自《深入浅出Linux工具与编程》