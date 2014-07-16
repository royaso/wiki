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
