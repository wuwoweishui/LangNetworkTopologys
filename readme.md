
**本项目仅进行内网主机资产整理，无漏洞利用、攻击性行为，请使用者遵守当地相关法律，勿用于非授权测试，如作他用所承受的法律责任一概与作者无关，下载使用即代表使用者同意上述观点。**


# 资产扫描

调用MASSCAN对内网主机进行如下任务，完成内网主机资产快速获取：

1. 开放端口扫描
2. 运行服务检测
3. 主机部署网站探测
4. 自动生成扫描结果报表

# 依赖环境

## Windows


自带masscan.exe，masscan来自[巡风](https://github.com/ysrc/xunfeng/tree/master/masscan/windows_64),需要注意的是Windows还需要安装WinPcap4.1.12

## Linux

自行安装masscan

# 快速使用

![](/image/1.jpg)

## 准备资产 

编辑文本，文本内容为你需要进行扫描的IP，比如：

	192.168.8.0/24
	10.152.168.0/24
	10.16.26.3
	10.26.36.0/24
	192.168.0.2
	192.168.0.6	
	192.168.0.15
	192.168.0.16
	192.168.0.17
	192.168.0.12
	192.168.0.19

## 启动扫描

随后直接启动Project下run.bat，按照提示导入上面的文本

## 输入端口

随后输入需要扫描的端口号，比如:

	21,22,23,25,80-9999,27017,27018
	or
	80,81,88,90,800,8000,888,8888,8887,8889,8080,9090,999
	or
	20-25,80,88,8080,8888,999,9999,1433,3389,3306,1521,6379,22222
	or
	21,22,23,25,80,88,888,8000,8888,8080,999,9999,9111,8873,87,9000,7000-7005,1433,3306,3389,1521,27017-27019,6379,6371,11211,8088,111,1001,50000,9110
	or
	1-65535

如果要使用默认的扫描端口，输入 0 即可

## 进程数设置

	单IP文本：2~6
	
	C段IP文本: 2~4
	
	B段IP文本：1

按照机器配置设置扫描进程数，如果扫描全端口，建议设置使用一个进程，最后的结果会自动保存在当前目录下

# 生成结果

扫完毕后，会生成相关的HTML和Xlsx文件，自动保存在目录下。

![](/image/0.jpg)


## 日志文件

当前目录会自动保存扫描日志，扫描异常原因，扫描结果


![](/image/9.jpg)


![](/image/10.jpg)


## 网页文件

1. 内网资产可视化报表
2. 端口/服务数据整理，点击标签即可查看相关开放主机
3. 每台主机资产详情


![](/image/2.jpg)


![](/image/3.jpg)


![](/image/4.jpg)


![](/image/5.jpg)



## Xlsx文件

1. 端口/服务数据整理
2. 部署网站主机整理
3. 每台主机资产详情整理



![](/image/6.jpg)


![](/image/7.jpg)


![](/image/12.jpg)

![](/image/8.jpg)



![](/image/11.jpg)

