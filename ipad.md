ubuntu network sftp://root@ipad/
------
批量删除app

pp助手  系统-设置-  ipainstaller/installipa force install

------
install ipa application without iTunes

    Find your lovely application/game and download the .ipa file
    Rename the .ipa file to xxx.zip(xxx is the name of the application/game)
    Open the .zip file and extract it
    You will see a xxx.app folder(xxx is the name of the application/game)
    Transfer the xxx.app folder to your iphone via SSH to the /Applications folder
    chmod 775 this xxx.app folder
    Respring/Reboot and you are done!

------
ipad上gcc编译一直出错，说是ld什么host arm，bing搜索和百度搜索结果都差不多，然后google就靠谱多了，前三条就有一条是theos，我一看，我就知道有希望了，我有弄过这个theos，很可能是它的原因。然后cydia卸载掉theos安装过的，然后重新安装了iphone-gcc ldid，最后就成功了！

太折腾了。又回到起点了。


为ipad2安装和配置gcc编译环境 | 王恒's Blog

http://wangheng.org/configure-gcc-on-ipad2.html

------
ios 越狱对我而言

以前就只有一个原因：越狱后可以安装破解应用，不花钱。就这一条，其他的都是假的

但现在在这条的基础上有更多的功能！

以前都没想过ipad越狱后有这么多能玩的东西，就是我这一代的老古董也玩的了

1、方便的复制黏贴 


------

以前一直抱怨ipad的边框太宽，占用了不少屏幕面积，导致可视面积缩小，现在才知道原来宽边框可以防止误操作，比较好手持，而且现在的可视面积也够了，再大就浪费电
------
unlock 嘿嘿 自动解锁ipad屏幕
------
 Voice Reader Text To Speech
------
 plutil -covert xml1 [filename  	转化plist为xml
------
sftp root@ipad - get 下载ipad文n件

------
 ssh root@ipad 'reboot' 一键重启ipad

ssh root@ipad 'killall SpringBoard'
------
用威风论坛的方法，是很简单，但他提供的第一个例子就make不过

就返回原来方法，用$THEOS/bin/nic.pl

被kill就ldid 然后make，这次出错信息就不一样了，明显进入到下一步，仔细一看，貌似就是我傍晚一直卡在的出错信息

ldid -S clang++试试看

上步可以，但新问题

'stdarg.h' file not found

貌似是sdks的框架问题

找到并复制了stdarg.h
/var/mobile/royaso/theos/sdks/iPhoneOS6.1.sdk/System/Library/Frameworks/CoreFoundation.framework/Headers/

这个h文件又找不到另外的h文件


2014年 08月 05日 星期二 00:38:18 CST

不折腾了
------
 vim --cmd "set encoding=utf-8" test.txt
------
killall SpringBoard
------
真是太幸运了！

自己编译的vim是在这里　/usr/local/bin/vim --version　7.3版的

cydia安装的vim是在 /usr/bin/vim --version  7.1

自己编译的好处当然多啦，中文支持啊！！泪流满面的那时候啊。

/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/bin/X11:/usr/games

更幸运的是路径在前面，所以用的还是自己编译的！！

刚才要安装bigboss recommended tools 想要在ipad上直接搭建软件环境theos，一看里面有vim，犹豫再三，还是决定安装了，就算真的覆盖了，没时间马上再次编译，反正真的在ipad上vimwiki的时间不多。

但真的担心啊，担心这次就没那么幸运可以编译成功，我还记得那次编译等了很久，一个晚上都没通过，后来是自己一条命令一条命令打过去的，才成功啊！！

才发现用root显示的是英文的欢迎，用mobile显示中文欢迎

恩，一开始一直找可以备份vim的方法，但我这个vim是编译的，他们提供的一般是已安装的列表，估计就是重新安装一遍

等我点下安装bigboss recommended tools 才想到，我应该搜索下怎么把编译的vim打包成deb然后host到自己网站上，这样以后就直接安装了啊

Compile For Cydia Submission | Submit Apps

http://thebigboss.org/hosting-repository-cydia/submit-your-app/compile-for-cydia-submission



Theos/Setup - iPhone Development Wiki

http://iphonedevwiki.net/index.php/Theos/Setup

#  bigboss tools
#  installtheos3
#  add source.list
#  install perl and theos

start new instant  

perl $THEOS/binn/nic.pl


出错‘first argument to `word' function must be greater than 0.  Stop.’

 解决： Retrieving SDKs

记得曾经在威风论坛有sdk，原来就早就下载了，还有vim呢。。拷贝到thoes/sdk


接着来make package 然后又出错 Clang命令没找到，看安装thoes教程，往上看，才知道还要下面的工具

The "iOS Toolchain" package

先安装　Darwin CC Tools　在bigboss 源　才能安　ios toolchain

clang++ llvm 

龟速下载，能下就好！

晕，好不容易下了，安装的时候崩溃

说要这个命令运行'dpkg --configure -a'

又一轮漫长等待，还没吃完饭啊alison
2014年 08月 04日 星期一 19:40:19 CST

一直崩溃

想直接命令行安装，找不到下载的deb，截图，搜索，还是下载慢，vps下载完成，赶紧保存网盘

clang一直被kill 不能make package

2014年 08月 04日 星期一 20:58:31 CST

吃饭吧

回来试下这个

在 iPhone 或 iPad 安装 iphone gcc llvm-clang, THEOS 编译程序或插件 - iPhone App开发外包专区 - 威锋论坛 - 威锋网

http://bbs.feng.com/read-htm-tid-5259660.html


------

2014年 07月 28日 星期一 10:37:00 CST

貌似samba出问题了，手机连不上，参考此文

ubuntu下开启samba服务和windows共享文件 - findaway123的专栏 - 博客频道 - CSDN.NET

http://blog.csdn.net/findaway123/article/details/6967010

------
http://www.2cto.com/os/201209/152692.html

http://blog.sina.com.cn/s/blog_8978492b010194kj.html

    samba实现自动挂载     1 fstab  2 /etc/rc.local (checked)
------

ubuntu的文件管理器连接到服务器

sftp://root@11.1.1.1.1:102/root

smb://root@ipad/main_readonly/

------
http://www.52cydia.com/debs/77.html

http://wuchuang163.blog.163.com/blog/static/23071707520140101210349/


samba   /etc/samba/smb.conf

ipad 装samba 设置samba的root密码一直失败，最后还是用smbpasswd命令搞定，还是跟重启有关？

有些问题，但重启后貌似就正常了  smbclient -L ipad -U root%ysh

才发觉原来我早用上samba了，在goodreader里就可以了,没想到一个应用都自带samba一般传文件到ipad 是够用了，但不能操作pc上的文件，搜索下载了个filebrowser，试用下挺不错的，可以查看远程pc上的文件，一般操作也没问题，txt，pdf，mp3，mp4，jpg都可以直接看。现在就在听着《梦里花落知多少》，女主播声音挺好听，语速和语气我喜欢。

smb还是给降级了，果然降级后就有smbclient，可以在ipad上访问ubuntu了。不过只有命令行，但有上面那个filebrowser就够了。

本来想卸载的smb的，不过幸好之气百度搜索页面还在，正好瞄到说卸载smb有个问题，算了，直接安装低版本的覆盖安装就行了！

用samba协议来mountipad到ubuntu

原来smbfs被cifs取代了。。难怪ii smbfs失败

sudo mount -t cifs //ipad/main_readonly/ /mnt/ipad -o  user=root,pass=sh,iocharset=utf8


------
装了个命令行文件管理器midnight commander
mc 太屌了，居然支持用鼠标！！要知道我这是ssh上去的鼠标啊
------
从命令行打开应用

open com.apple.mobilesafari

open com.tencent.QQMusicHD

open com.shanbay.book
 
open com.saurik.Cydia

Preferences:  com.apple.Preferences
------
ipad直接说中文，本来在bash下打不了中文的，但在zsh可以打中文，只是显示为数字而已，这样就可以说中文了。但还有更好的，直接在文件里打中文，然后say a.txt 是不行的，提示说要直接在say后面输入字符，那就吧这个当初一条命令写在a.sh里就可以了，再配合下面launchctl，完美啊。。不过中文貌似读的不错，就是英文差了点，看看是不是系统语言的问题


ipad 用vim重命名中文乱码文件
------
veency

连接投影仪
------
    ipad/mac使用launchctl定时运行程序

http://www.2cto.com/os/201305/215350.html


~mobile/LauchAgents/com.royaso.plist
------

applinks 

进入有中文的目录：一个中文3个字符，cd后用pwd就可以显示中文

软链接：链接前后最好都要绝对路径，可以cd后用`pwd`来输出源路径
-------
官方源链接发现没有东西啊

后来是通过命令添加的源
 `echo 'deb http://ios-webstack.tk/cydia/ ./' > /etc/apt/sources.list.d/ios-webstack.list`

搜索其他的源包括拷贝别人的威锋源到自己源里，和一个外国myrepospace/oncewait

再进去，发现官方源有东西了，仔细看，发觉居然没有主要的那个ios-lighttpd-php-mysql

折腾了下修改用户身份的，感觉应该是cydia版本更新了，没有了那个'管理'和'设置',
感觉是集合到'已安装'那边

但就是搜索不到官方里的ios-lighttpd

没办法用外国源安装了，重启cydya几次，就差主程序了，其他都安装好了

就当是安装完成吧，测试localhost失败，发觉lighttpd没启动，这个要.conf配置文件的

`lighttpd -f /etc/lighttpd/lighttpd.conf`

去官网看配置吧

--
刚刚一直在搞mysql，httpd很容易启动毕竟有经验了

这个mysql一直启动不了，折腾了我老半天

最后我卸载了，

看到ipad上一切没问题了，我也可以去吃饭了，都快九点了啊
2014年 07月 09日 星期三 20:47:44 CST

简单步骤如下

1 外国源安装iso-webstack
2 卸载mysql
3 从我的weiphone源安装iso-webstack，


-----------
ioswebstack (lighttpd+mysql+php)

http://moreinfo.thebigboss.org/moreinfo/depiction.php?file=ioswebstackDp
-------
`ldid -S hello`

{{{
tar cvf aa.tar aa/

xz -z aa.tar

xz -d aa.tar.xz 

tar xvf aa.tar
}}}
------
{{http://d.pcs.baidu.com/thumbnail/092c43a0b178fb2b3a1eadf9e67c26e7?fid=2066263448-250528-182338647594379&time=1404892800&rt=pr&sign=FDTAER-DCb740ccc5511e5e8fedcff06b081203-rRLhyDqy4LHiQJdcNoJxyapqVsA%3D&expires=8h&prisign=RK9dhfZlTqV5TuwkO5ihMad7KcxNLQBVSNzsPgBmfSz/w84QlB4ZnD3zpRYJ58jLmCHPCKQ26W3lZgeqMIs1scDX2sP0NjkkvnJ9lZ0O/Cp7JeqCYB6LsX3A3Rtz2/Obwq48P8v2auVRdGeENY3ooYA9UoElzYfuys1/OqvVUKFbk5Hi3liHiw8Reb599Law&chkv=0&chkbd=0&size=c1280_u1024&quality=90}}

-----
http://www.keakon.net/2011/03/19/在iPhone上搭建lighttpd服务器

http://redmine.lighttpd.net/wiki/lighttpd/TutorialConfiguration

`killall -9 lighttpd`

/etc/lighttpd.conf

{{{
server.document-root = "/var/root/www" 

server.port = 80

server.username = "mobile"

mimetype.assign = (
  ".html" => "text/html; charset=utf-8",
  ".htm" => "text/html; charset=utf-8",
  ".css" => "text/css; charset=utf-8",
  ".js" => "text/javascript; charset=utf-8",
  ".txt" => "text/plain; charset=utf-8",
  ".jpg" => "image/jpeg",
  ".png" => "image/png",
  "" => "application/octet-stream"
)

index-file.names = ( "index.html" )

}}}

---------
ipad gcc 

http://wangheng.org/configure-gcc-on-ipad2.html

`./configure --host=arm`

--------
