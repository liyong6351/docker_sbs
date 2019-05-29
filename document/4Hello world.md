## 1. Hello World
<pre>
docker run ubuntu:15.10 /bin/echo "Hello world"
</pre>
#### 参数解析
1. docker: docker的二进制执行文件
2. run: 与前面的参数docker组合来运行一个容器。
3. ubuntu:15.10 : 指定运行的镜像，docker首先从本地查找镜像是否存在，如果不存在，docker会从镜像仓库 hub.docker 下载公共镜像。
4. /bin/echo "Hello world": 在启动的容器内执行的命令 
* 以上命令完整的意思可以解释为：Docker 以 ubuntu15.10 镜像创建一个新容器，然后在容器里执行 bin/echo "Hello world"，然后输出结果。

---
## 2.交互式的容器  
* 我们通过两个参数 -i、-t，让docker具有对话的功能  
<pre>
docker run -i -t ubuntu:15.10 /bin/bash
</pre>
* 以上命令就是代表已经进入到容器的内部操作

---
## 3.启动容器(后台模式)
<pre>
docker run -d ubuntu:15.10 /bin/sh -c "while true; do echo hello world; sleep 1; done"
</pre>
* 此时容器就在后台启动，命令返回的随机字符串就是docker容器的id

---
## 4.查看docker进程 
<pre>
docker ps
</pre>
* 返回docker进程情况，其中name是系统自动分配的

---
## 5.在容器内使用docker logs命令，查看容器内的标准输出
<pre>
docker logs [id]/[name]
</pre>

---
## 6.停止容器  
<pre>
docker stop [name]/[id]
</pre>
