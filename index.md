%template index

this can be for short term file share and website display!! vagrant share!!!
------
还是有用到滚轮的时候的,比如terminal信息太长,我又把右边滚动条关闭了
------
吐槽下百度bae本地开发环境:
- 文件名字不好,叫localenv.zip,谁能一眼看出来是百度? 
- 近200m的下载包大部分是software里的vm,vagrant,git的windows版本等等,对我等ubuntu用户,真正有用的也就那几个vagrantfile,五个加起来还不到1m,浪费下载时间和空间,也浪费表情.
- bae一运行就出错,用户体验非常差!百度下错误信息,好不容易就找到一条,还是bae吧的,还是同样的问题,下面就一个人一直灌水,最后有人自问自答了,但我用他的办法没成功.还是自己想办法:升级看看,估计是这个localenv很久没更新了,然后就成了`sudo pip uninstall bae && sudo pip install bae --upgrade`
- git也是老版本的.因为http连接git,老是要输入密码,记得有个git命令可以记住,`git config --global credential.helper=store`,但同样的命令在这里就不行,本以为升级下就行`sudo aptitude upgrade git`,还是不行`invalid key`!干!原来没有等号!!  
- cha!这简直不叫吐槽,简直就是坑阿!!!坑在这里了!`bae app setup -I sadfasd` app里面没东西阿,我擦,vagrant里都是黑黑的,出错信息都没注意到,坑我半天阿,原来说是`.baeapp`这个文件要移除,然后在`git checkout master`才能看到文件阿!!混蛋!!百度没结果,难道只有我遇上这些问题?人品这么好?!感觉这个本地环境没人用也没人维护似得.下雨了

------
p5kpl am se主板上的'vanderpool technology'就是开启vt-x的选项,而不是我一直以为的'virtualiztion technolog',让我好找阿.而且貌似这个选项是跟cpu是否支持xt-x有关,cpu不支持的话是不会出现这个选项的.

关闭这个选项后,在ubuntu下`cat /proc/cpuinfo | grep vmx`还是会显示的,但`sudo kvm-ok`就起作用了,说明有效
{{{

10026  ii cpu-checker
10030  ll /dev/kvm
10031  ii msr-tools
10032  sudo modprobe msr
10033  sudo rdmsr 0x3A
 如果是5就是支持,1是不支持
}}}

我之所以会迷惘是因为vmware提示出错说vt-x不支持,要不要忽略并继续.

去xp下测试securty会不会检测出来,原先的结果是"locked on"
------
vagrant官网卡得跟屎一样,十几m的东西要两个小时,这不是开玩笑吗?!百度最新版本,
------
看来要改变管理密码的方式了. 1 用lastpass 2 不绑定手机,否则手机一丢,全部玩完
------
vmplayer运行xp下的mac虚拟机报错说vt-x不支持?忽略后开机mac卡在灰苹果界面,重新安装连光盘都检测不到,说是没有系统?果然不能在ubuntu下折腾阿.


------
看到很多人说到越狱时都说自己不为了装盗版软件,自己pc都是正版,用的app也是正版.我想说,我也买过两个正版app,今天第二个listeningDrill,之前那个豆丁阅读器.现在半夜下雨
------
绝知此事要躬行。 
------
chrome to remove one perticular ca
------
汽车对冰淇淋过敏
------
three steps to learn: what how why
------
"鬼妈妈",本来有点累,想休息,结果看了这电影,90分钟,现在很精神了.
------

不懂为什么安卓要用虚拟机运行app?这直接导致了流畅性不如苹果
------
rubber duck!
------

网站组织好,结构好,让人一看就知道要找的东西在哪里,又何需搜索引擎

分类也好,标签也好,都不如从源头遏制:只输出好东西,贵精不贵多.

google也不是万能的,GR被关我是经历过的,但比百度好


------

live as if you were to die tomorrow, learn as if you were to live forever
----------
another reason to get a cpu with vt: to get genymotion run faster  (docker)

"网购了两个东西,垃圾短信随风而至,我有理由相信,我个人信息被贩卖了!" 帝林说过,一次是意外,两次是巧合,三次就是恶意事件了!

"as long as I'm single, I have all possibility, once I get married, I got screwed. But even though I might get screwed, I still wanna meet the sole mate, the one who completes me"
