
ubuntu下apache建立虚拟主机

之前有弄过，没成功，所以这次设置的时候发现有上次留下的配置文件

# 首先，apache的配置在win下和在linux下的配置是不一样的，

这个从我搜索到的结果来说是证实的，大部分都是win下的配置

# 要多看帮助稳定，就是man

至少我知道了 

	# 不能直接用apache启动，要用apachectl或者/etc/init.d/apache ，
因为需要启动的时候传入些系统参数（貌似就是/etc/apache/envvar这个文件）
	# 有谢好用的小工具，a2enconf a2ensite a2enmod
把available里的文件做个链接到enable就算是启用了，恩，体现了分模块的思想

恩，关键的这个小工具，a2query，让我发现原来只有加载了默认配置。
	# 要加conf才能被识别，名字倒是随意，但至少要自己看得懂：aa.com.conf

# 搜索，感觉老外更靠谱
   
   我的问题就是这样解决的。明明已经拷贝了配置文件，但就是怎么刷新都没用，
还是现实默认的那个.基于上面那点提到的那个a2query小工具，我知道了原因：
没有加载，所以一看到下面有人回复说要以conf结尾才能加载配置，我就知道我哪里
出问题了

原因找到了，就容易解决了。

注意：要记得sudo，没sudo它也没出错提示

让我测试失败好久

`sudo service apache2 reload`

{{{

NameVirtualHost *:80
<VirtualHost aaa.com:80>
ServerName aaa.com
DocumentRoot /var/www/aaa.com
</VirtualHost>

}}}
