# 前言
在国内的一些项目中，需要内网开发程序。python的依赖库，比如numpy等也需要离线安装。其中的一个办法是拿离线安装包一个一个下载并导入内网里安装，还有一个方法就是在本机上安装anaconda并配置好环境，然后将整个anaconda环境导入内网环境中。
本文主要讲解如何将anaconda环境迁移到内网系统里，并配置初始化为默认启动，即命令行前出现`(base)`字样。
# 本机安装anaconda
这一步已经有很多人讲过了。
+ 首先本机和内网里的系统需要一致，要是Ubuntu，都是Ubuntu系统。
+ 其次可以从[清华镜像源](https://mirrors.tuna.tsinghua.edu.cn/)l里下载anaconda安装包
+ 运行`.\ Anaconda3-2021.11-Linux-x86_64.sh`
+ 在默认的路径下会生成Anaconda3的文件夹，这是等下需要迁移的文件夹
+ 可以配置清华镜像源，在使用帮助中有[使用方法](https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/)
+ 配置好环境，使用`conda install numpy`或者`pip install numpy`
# 将本机环境迁移到内网环境
+ 第一步肯定是将配置好的Anaconda3文件夹迁移到内网环境
> 需要将文件夹放到与本机相同的位置
+ 第二步运行命令
	```bash
	source /root/anaconda3/bin/activate
	```
> 需要更换成自己的地址
+ 第三步运行命令
	```bash
	conda init
	```