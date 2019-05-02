环境准备

1、window10支持Hyper-V，所以安装Docker更简洁

2、Docker官网获取windows版，安装，基本上按照提示即可，期间会有几次重启计算机

3、使用docker启动jenkins镜像，详情参考https://jenkins.io/doc/tutorials/build-a-multibranch-pipeline-project/


遇到的问题

Q:\User\Administator is invalid path. 

A:不知何故%HOMEPATH%的值非法，所以在启动时，直接不适用该变量，换成home。
