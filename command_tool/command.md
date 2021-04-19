### 输出环境变量
    echo $PATH

### 根据程序名查看进程 (pid)
    ps -ef | grep 程序名 | grep -v grep 

### 根据端口号(port number) 查看端口所监听的进程 (pid)
    netstat -anp | grep 端口号
    lsof -i: 端口号

# Firewall操作

## 查看所有开放的端口列表
    firewall-cmd --zone=public --list-ports
    
## 查看防火墙某个端口号(3306)是否开放
    firewall-cmd --query-port=3306/tcp
    
## 开放某个端口号
    firewall-cmd --zone=public --add-port=3306/tcp --permanent
    
## 关闭某个端口号
    firewall-cmd --remove-port=3306/tcp --permanent
    
## 查看防火墙状态
    systemctl status firewalld
    
## 关闭防火墙
    systemctl stop firewalld

## 打开防火墙
    systemctl start firewalld
    
## 重启防火墙
    systemctl restart firewalld
    
