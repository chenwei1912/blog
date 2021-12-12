# 嵌入式系统编译
修改toolset,在 project-config.jam 文件中找到toolset部分,填写对应的cross-compiler,注意空格  
```bash
if ! gcc in [ feature.values <toolset> ]
{
    using gcc : : /opt/arm/arm-ca9-linux-gnueabihf-6.5/usr/bin/arm-ca9-linux-gnueabihf-g++ ;
}
```
编译完成后就可以在板子的arm-linux系统上跑boost库程序  

## context/fiber库无法链接  
原因是boost一些库用到了平台的差异性代码,所以要指定平台架构,b2选项必须加入  
```bash
architecture=arm
abi=aapcs
binary-format=elf
./b2 stage architecture=arm abi=aapcs binary-format=elf --with-filesystem --with-fiber --with-context threading=multi link=static link=shared
```  
顺利完成编译  

## 致谢  
[交叉编译](https://www.cnblogs.com/findumars/p/7461244.html)  
[boost::context](https://github.com/moritz-wundke/Boost-for-Android/issues/116)
