# VirtualBox ubuntu server版 安装增强功能 共享文件夹

VirtualBox 安装增强功能 ubuntu server版

错误描述：未能加载虚拟光盘 C:\Program Files\Oracle\VirtualBox\VBoxGuestAdditions.iso 
到虚拟电脑，Could not mount the media/drive ‘C:\Program Files\Oracle\VirtualBox/VBoxGuestAdditions.iso’ (VERR_PDM_MEDIA_LOCKED). 
截图如下 
![Image text](https://github.com/tustzhaoyang/VirtualBox-ubuntu-server-/blob/master/image/20170919145155474.jpg)

主要参考 
http://blog.csdn.net/zhaihaifei/article/details/40055383
对链接的文章内容进行整理与补充

	·确保当前使用的账号有root权限，即可以执行sudo
	·更新apt-get，请执行 sudo apt-get update，以及 sudo apt-get upgrade
	·安装依赖工具，sudo apt-get install dkms， sudo apt-get install build-essential
	·重启， sudo reboot，如果命令无效或有执行错误，也可以使用外面的virtualbox的重启按钮
	·挂载cdrom， sudo mount /dev/cdrom /mnt/

		·如果挂载失败，则需检查设备->分配光驱下是否包含了VBoxGuestAdditions.iso这个镜像
		·如果有请选择它
		·如果没有，请点击选择虚拟盘，然后在C:\Program Files\Oracle\VirtualBox 下找到它
		·最后再执行上述命令，成功后的截图如下： 