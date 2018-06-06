## 常用命令
cd ~ ： 回家(回根目录)  
touch xxx   创建文件或用nano  

mkdir 文件夹1/文件夹2/文件夹3  文件夹1里面创建文件夹2，文件夹2里面创建文件夹3（可以用多层）  

gedit xxx   打开文件，没有就创建 或用vi nano    

man 命令名   查看命令的相关用法  

cat   查看文件或用more less nano  

rm -rf 文件夹名 (删除非空文件夹,此命令要慎用，可以删除所有文件，包括系统文件)  

"> xxx.txt"      重定向，覆写整个文件  
">> xxx.txt"     重定向，追加  

ls -alh | more  管道  

ln -s  原文件名 新文件名   创建快捷方式（软链接文件(删除原文件将失效))  
ln     原文档名 新文档名      硬链接文件(删除原文件仍然有效 类似复制)  

tar -cvf xxx.tar                            放进去的文件  
tar -xvf xxx.tar                            解包  
tar -zcvf xxx.tar.gz (-C /制定路径)yyy zzz   打包和压缩（更精简）  
tar -zxvf xxx.tar.gz                        解压缩  

which 命令   查看命令路径  
cal         查看日历  
date        查看当前时间  

ps aux   查看所有运行进程  
top      持续显示运行进程  

kill -9 PID  强制结束进程  

reboot    重启系统  
df        查看磁盘状态  
du -h     查看当前路径占用多大容量  

ifconfig         查看网卡状态  
netstat -anptu   查看网络状态 t:tcp u:udp p:pid且可能需要sudo  

chmod a+x file   u:owner g:group o:other a:all rwx r=4,w=2,x=1  

sudo -s      切换到root  

dpkg --list                查看已安装的软件包列表  

apt-get update    # 更新安装源信息库  
apt-get update    # 更新已安装软件  

apt-get --purge remove <package>  # 删除软件及其配置文件  
apt-get purge                     # 和上面相同  
apt-get autoremove <package>      # 删除没用的依赖包(保留配置文件)  
apt-get autoclean     清理旧版本的软件缓存(已经卸载掉的软件包)  
apt-get clean         清理所有软件缓存(电脑上存储的安装包)  

源码安装时 ./configure --prefix 指定安装目录，卸载时直接删除整个目录  

## 网络资源
[常用命令](https://zhuanlan.zhihu.com/p/37666424)  
