### 根据程序名查看进程 (pid)
    ps -ef | grep 程序名 | grep -v grep 

### 根据端口号(port number) 查看端口所监听的进程 (pid)
    netstat -anp | grep 端口号
    lsof -i: 端口号
