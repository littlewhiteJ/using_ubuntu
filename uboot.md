# Ubuntu18.04 启动盘制作


首先进入 Ubuntu 官网下载 Ubuntu18.04 ios 镜像包，下载的镜像包为：ubuntu-18.04.1-desktop-amd64.iso

下载链接：https://www.ubuntu.com/download/desktop

 

插入U盘，在Linux系统中打开终端，查看 U 盘信息：

# sudo fdisk -l

 

然后卸载掉 U 盘：

# sudo umount /dev/sdb*

 

U 盘格式化：

# sudo mkfs.vfat /dev/sdb -I

完成格式化后查看磁盘信息：

 

最后使用 dd 命令制作启动盘：

# sudo dd if=ubuntu-18.04.1-desktop-amd64.iso of=/dev/sdb bs=10M

**来源：https://blog.csdn.net/xiaoma_2018/article/details/85059930**
