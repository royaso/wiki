中午又折腾 vimwiki了

现在情况是有三个地方

一个在ubuntu，两个在ipad

ipad上新增了root账号的，因为空repo自动更新到web位置用root比较简单，没有mobile的权限问题，这样要更新到ipad本地的web就用root账号，也可以同时更新到royaso.com

维护还是老样子，不管在哪里，只要不是跟上次更新的环境一样，就要先pull，不管是pull网页文件html还是wiki，这样就应该没错了。

root要更新本地web还是在html里push

对了，还发现用root账号直接copy  mobile账号~mobile/.vim里的文件就可以完全复制vim的插件和各种设置，当然也要复制.vimrc


------

终于成功了！！ipad上的vimwiki，没想到居然是这么简单！！！


{{{

可以自行在$HOME目录下建一个.vimrc配置文件， set encoding=UTF-8 set langmenu=zh_CN.UTF-8 set fileencodings=ucs-bom,utf-8,chinese,cp936,gb18030,big5,euc-jp,euc-kr,latin1 set fileencoding=utf-8 set termencoding=utf-8


再一看，发觉更简单只要第一句就可以了 `set encoding=UTF-8`

这就是我这好几天的成功啊！一句话啊！！！


}}}
-------------
ubuntu和ipad同步wiki生成的html的时候，才发觉原来有改过一个文件`.vim/autoload/vimwiki/html.vim`,
原作者忘了闭合<li>标签 ，我给修正了，ipad那边 没改，所以生成的htm就差这么一点。

以后就这样同步，不论在那边写wiki先pull，而后html生成再push。

同步不必太频繁，就像之前想的那样，每天结束后push一次就可以了

这次从ubuntu测试
这次从ubuntu测试
-----------
维护两份以上的wiki时，同步步骤

ipad上的vimwiki和ubuntu上的vimwiki还是有个同步上的问题

我单是想到生成的html可以同步，没想到各自的viki文件也会修改html，所以两者的viki文件也得同步下

所以简单想就是：先分别同步wiki和html，然后写玩wiki再生成html，再分别同步，然后就是从头循环


---------
惨痛的ipad上的vimwiki折腾经历

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


------------

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


---------
明天早起，带装备去感受清晨，

2014年 07月 01日 星期二 17:38:48 CST

---------

注意


貌似新建文件夹不会删掉，但文件夹里的只要是html结尾的都会被删掉，除非vim里有设置忽略

ipad 貌似就算原配蓝牙键盘都会有esc键不能用的情况

看来还是我这外接键盘和prompt好用



-------

好不容易终于折腾到答案，当然要马上保存好，备份到ubuntu，结果！把我本来的.vimrc给覆盖 了！
我勒个去啊！！！
幸好记得之前有传一个到ipad了，翻了出来，还好，一切正常！！scp 要记得改名，覆盖它不给提示啊！
--------
