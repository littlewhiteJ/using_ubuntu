# 执行远程脚本配置方法



## 所需硬件

- 一台路由器

- n台宿主机

- 一台远程控制机（如笔记本 工作站）



## 配置步骤

### 设置路由器

- 连接路由器 并进行设置密码等基础配置

- 无线网络基本设置中 将模式设置为11n only

- 尽量将信道设为不常用的信道 避免干扰（如8）

- 绑定端口 将宿主机的MAC与固定的ip地址绑定



### 设置宿主机

- 安装ssh server



```

	sudo apt-get install openssh-server

```



- 观察ssh是否开启



```

	ps -e | grep sshd

```



- 若没有开启 使其开启



```

	sudo service ssh start

```

or

```

    sudo systemctl start ssh

```



### 设置控制机

- 生成公钥

若之前生成过 则不用反复生成



```

	ssh-keygen

```



- 将公钥复制到宿主机



```

	ssh-copy-id -i [path of id_rsa.pub] user@ip

```









