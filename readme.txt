��3��������ִ�г���

��    �ڵ�ǰĿ¼������>msg.tmp�������ļ�msg.tmp��

��    ���뷢����Ϣ���г��� gcc msgsnd.c -o  msgsnd��

��    ִ��./msgsnd��ִ�н������:

  ----- Message Queues --------

key        msqid      owner      perms      used-bytes   messages   

0x0101436d 294912     zjkf       600        1072         2          

��    ���������Ϣ���� gcc msgrcv.c -o msgrcv

��    ִ��./msgrcv��ִ�н������:

 type=1,time=03:23:16, message=happy new year!

 

------ Message Queues --------

key        msqid      owner      perms      used-bytes   messages   

0x0101436d 294912     zjkf       600        536          1         

��    ����ipcrm -q 294912ɾ������Ϣ���С���Ϊ��Ϣ���������ں˳������ڵģ��ڳ�������������msgctl����������������ipcrm������ʽ��ɾ��������Ϣ���о�һֱ������ϵͳ�С������ź����͹����ڴ�Ҳ�����ں˳������ڵġ�

 

ժ¼�ԡ�����ǳ��Linux�������̡�