
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
