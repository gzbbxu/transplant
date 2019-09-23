android 移植  thttpd

http://www.acme.com/software/thttpd/thttpd-2.29.tar.gz



```
export NDK=/develop/android/android-ndk-r16b
export SYSROOT=$NDK/platforms/android-21/arch-x86_64
export CC="$NDK/toolchains/x86-64/prebuilt/linux-x86/bin/i686-linux-android-gcc  --sysroot=$SYSROOT"

export CFLAGS="--sysroot=$SYSROOT  "
export LDFLAGS="--sysroot=$SYSROOT  "
sudo ./configure --prefix=/home/zhouke/work/thttpd_install  //配置
```

遇到报错解决：

无效的组 

chgrp: invalid group: `www' make[1]: *** [install] Error 1 make[1]: Leaving `

增加组：
cat /etc/group
addgroup www
which addgroup
sudo addgroup www
cat /etc/group



无法创建一般文件“/usr/local/man/man1/makeweb.1”: 

只需创建//home/zhouke/work/thttpd_install/man/man1文件夹即可安装。