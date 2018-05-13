# lsof

```bash
查看最大文件句柄数
ulimit -n

统计系统中当前打开的总文件句柄数
lsof|awk '{print $2}'|wc -l

查看当前进程打开了多少句柄数
lsof -n|awk '{print $2}'|sort|uniq -c|sort -nr| head -n 10

第一列 是打开的句柄数
第二列 是进程ID

通过ID 查看进程名
ps -aef | grep ID


查看当前主机TIME_WAIT
netstat -anp | grep TIME_WAIT

查看进程打开了哪些文件
lsof -p PID

```

