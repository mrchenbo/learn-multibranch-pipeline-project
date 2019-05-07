环境准备

1、window10支持Hyper-V，所以安装Docker更简洁

2、Docker官网获取windows版，安装，基本上按照提示即可，期间会有几次重启计算机

3、使用docker启动jenkins镜像，详情参考https://jenkins.io/doc/tutorials/build-a-multibranch-pipeline-project/



遇到的问题

Q:\User\Administator is invalid path. 

A:不知何故%HOMEPATH%的值非法，所以在启动时，直接不适用该变量，换成home。

Q:重启时发现端口被占用，但是使用netstat -ano | findstr "port" 并未发现有进程占用该端口。

A：使用docker ps -a 发现之前的jenkins容器仍然驻留在后台，但网站依然无法访问，停止容器后报Error starting userland proxy: mkdir /port/tcp:0.0.0.0:9092:tcp:172.17.0.2:9092: input/output error. 重启docker解决，参考https://github.com/docker/for-win/issues/3338
