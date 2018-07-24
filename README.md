脚本一：CentOS6和CentOS7 一键更换内核，一键安装锐速[lotServer][serverSpeeder ]

支持KVM、VMWARE、Hyper-v、XEN 虚拟化技术的VPS

CentOS6和CentOS7 一键更换内核，完成后会重启

wget --no-check-certificate https://blog.asuhu.com/sh/ruisu.sh
bash ruisu.sh
CentOS6和7 更换内核完成一键安装锐速[lotServer]

wget --no-check-certificate -O appex.sh https://raw.githubusercontent.com/0oVicero0/serverSpeeder_Install/master/appex.sh && chmod +x appex.sh && bash appex.sh install
安装完成后检测是否启用

lsmod |grep appex
 

脚本二：LotServer（锐速）一键安装脚本

LotServer是锐速的母公司，这个跟之前分享的锐速破解一键脚本的区别就是内核支持的全面些，然后安装的锐速版本不再是清一色的3.10.61.0了。脚本作者Vicer，项目已在Github开源。

功能: 0.#Only for Linux.
1.支持自动检测公网网卡,多个网卡也能区分.
2.支持自动适配内核(需锐速支持).
3.添加询问是否开启accppp功能.(实测并开启后没有效果.)
4.默认设置为G口宽带.(听说设置大点可以提高速度)
5.支持一键完全卸载(此脚本安装的无残留).
6.所需文件均来自GiuHub,不放心可自行查阅.(完全公开,适合新手学习)
7.不支持自动更换内核,请自行更换.(网上教程非常多)
8.不支持 OpenVZ,不需要尝试,会告诉你找不到网卡.
9.吐槽: CentOS 居然连 which 都要自己安装,心好累.脚本将就着看吧.
#.除此脚本外,所有内容均来自互联网.本人不负任何法律责任,仅供学习使用.
#.安装文件appex.zip 为 lotServer的, 增加了一些 lotServer 加速模块。(感谢 @lotServer 提供安装文件.)
#.使用前请日常 update; 欢迎反馈bug(各种安装错误).

GitHub地址:

https://github.com/0oVicero0/serverSpeeser_Install

serverSpeeder_support_kernel支持的内核版本

https://github.com/0oVicero0/serverSpeeder_kernel/blob/master/SystemList.md

Linux serverSpeeder Install (安装):

wget --no-check-certificate -O appex.sh https://raw.githubusercontent.com/0oVicero0/serverSpeeser_Install/master/appex.sh && chmod +x appex.sh && bash appex.sh install

Linux serverSpeeder force Install (强制安装指定内核版本的锐速):

wget --no-check-certificate -O appex.sh https://raw.githubusercontent.com/0oVicero0/serverSpeeser_Install/master/appex.sh && chmod +x appex.sh && bash appex.sh install '${Kernel Version}'

Linux serverSpeeder Unstall (卸载):

wget --no-check-certificate -O appex.sh https://raw.githubusercontent.com/0oVicero0/serverSpeeser_Install/master/appex.sh && chmod +x appex.sh && bash appex.sh unstall

使用方法:
启动命令 /appex/bin/lotServer.sh start
状态查询 /appex/bin/lotServer.sh status
停止加速 /appex/bin/lotServer.sh stop
