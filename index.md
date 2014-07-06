ubuntu和ipad同步wiki生成的html的时候，才发觉原来有改过一个文件`.vim/autoload/vimwiki/html.vim`,
原作者忘了闭合<li>标签 ，我给修正了，ipad那边 没改，所以生成的htm就差这么一点。

以后就这样同步，不论在那边写wiki先pull，而后html生成再push。
-----------
royaso:有只小狗一直跟着我怎么办
alison:干翻它
royaso：有效！没想到你名声在外。我把你短信给它看，它就吓跑了！

------------
ipad上的vimwiki和ubuntu上的vimwiki还是有个同步上的问题

我单是想到生成的html可以同步，没想到各自的viki文件也会修改html，所以两者的viki文件也得同步下
------------

好不容易终于折腾到答案，当然要马上保存好，备份到ubuntu，结果！把我本来的.vimrc给覆盖 了！
我勒个去啊！！！
幸好记得之前有传一个到ipad了，翻了出来，还好，一切正常！！scp 要记得改名，覆盖它不给提示啊！
--------
终于成功了！！ipad上的vimwiki，没想到居然是这么简单！！！


{{{

可以自行在$HOME目录下建一个.vimrc配置文件， set encoding=UTF-8 set langmenu=zh_CN.UTF-8 set fileencodings=ucs-bom,utf-8,chinese,cp936,gb18030,big5,euc-jp,euc-kr,latin1 set fileencoding=utf-8 set termencoding=utf-8


再一看，发觉更简单只要第一句就可以了 `set encoding=UTF-8`

这就是我这好几天的成功啊！一句话啊！！！


}}}
-------------

如果不舒服，那就是不对了
---------
真的是泪流满面啊 ！！！！

终于找到支持utf8的vim了

眼泪都流出来了

甚至想到降级到4.3.3 只要能用上multibyte的vim！！

重新啊安装了好几次，终于在这次绝望得要删掉的时候，把vimrc先给删掉，然后，居然就成了！！

那其他都是小事，虽然mobile的还是那个错误，实在不行root也没问题！

可以去吃饭了！


---------

晕啊，那个版本的vim不知道什么原因，居然不能高亮语法，我去，vimwiki唯三个条件就是有个要
`syntax on`

这还怎么玩，还怎么做朋友啦！！

----------
算了，不折腾了 ！！！


=== 改描述好了:鞋子合不合脚，只有脚知道 ===

 = [[girl/|女博主点这里]] =
ipad gcc 

http://wangheng.org/configure-gcc-on-ipad2.html

---------
明天早起，带装备去感受清晨，

2014年 07月 01日 星期二 17:38:48 CST

alison  过来看啊

找到女博主一只，哇咧，还是个美女啊

小蝴蝶

{{http://photos-h.ak.instagram.com/hphotos-ak-xpa1/925466_1415846272020615_2043392289_n.jpg}}

http://xiaohudie.net/photo?1

== 想写的东西 ==

        - [ ] yeah! almost forget! blog like your publish your book!
        - [ ] 舍弃，一对夫妇，搬家，东西都留下。舍友，4年辛苦笔记，离校，舍下
        - [ ] 吐槽mac设置，tult视频
        - [ ] 原创，seo，转载
        - [ ] 在很早很早以前，我就喜欢一句话：一个人总得实践他所相信的东西。
*我是不是真的喜欢编程*
        - [ ] goodbook for sync, ipad vim to write
        - [ ] what you are , that will attract poeple like you!
        - [ ] good blog from ruanyifeng.com commenters
        - [ ] n 有人说财务自由是个骗局，活在当下
        - [ ] 加入过几个Q群，not what i expected
        - [ ] ubuntu 14 新界面 火狐，
        - [ ] a movie ( 9 person in a room)
        - [ ] what is unique in blog. Your Values!!
        - [ ] 我的浏览器firefox
        - [ ] QQmail webpage , an intereseting pic
        - [ ] video script downloader: make my first vedio
        - [ ] fuck you seo, iplaysoft,
        - [ ] about friend links
        - [ ] dont get seriouse about your birthday, everyday is equal.
        - [ ] <我爱你> 木头
        - [ ] motivational video
        - [ ] "I am to old for this stuff" KTV
        可以参考这篇 用什么浏览器更好高效地阅读  http://jianshu.io/p/66c95fe1f627
	- [ ] 我真的需要一部大屏智能手机吗？
	- [ ] 既要写也要回顾，以前的东西
	- [ ] 扇贝苹果客户端评论换贝壳活动！ 从今天开始，凡是在iPhone或者iPad上下载扇贝系列客户端，并且评论打分（打分请客观，不要违心），评论中按照“shanbay:你的用户名”这个格式写上你的用户名，我们就会在24小时内赠送200贝壳！下载评论4个客户端，就送800！ 
	- [ ] 我的兵器
	
----------


 == [[mystudy|所学]] ==
 == [[myposts|所写]] ==
 == [[posts|好文]] ==
 == [[words|好句]] ==
 == [[people|我欣赏的人,我喜欢的站]] ==
 == [[ideas|我的想法]] ==
 ==[[about|关于本站]]==


貌似新建文件夹不会删掉，但文件夹里的只要是html结尾的都会被删掉，除非vim里有设置忽略

ipad 貌似就算原配蓝牙键盘都会有esc键不能用的情况

看来还是我这外接键盘和prompt好用



-------




编码不统一啊，怎么弄都不行，试了其他几个ipad上的ssh软件
还不如原先这个promtp好呢，
有的界面看起来就不喜欢，更别提登陆后连命令都出错
这还让我们怎么做朋友啊

次之的是issh，居然pp助手里没有，让我费尽心思网上找破解版
上传安装时才发现，tmd原来就有安装过，安装包还在呢

更无语的是，最新版的这个，估计是ios6了，可怜我ios5不支持

好不容易卸载又从电脑里翻出来旧版的安装上，

tmd键盘连接又出问题，不能打英文，中文打得出来却不能现实

这还让我们怎么做朋友啊

一种就这么折腾没了。没成果

gbk和utf8转化也是失败的

最好的解决方法就是统一用utf8
那只好自己编译到ipad上，但这不容易啊hd

要么二者分开用，，这就让我不爽了

之前找到个别人编译的说是支持多字节的vim，安装成功，运行失败
。难道是iphone专用？


