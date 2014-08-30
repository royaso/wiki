
2014年 08月 26日 星期二 12:10:53 CST

ubuntu 14.04 安装java
{{{
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java8-installer
sudo apt-get install oracle-java8-set-default
}}}

既然想安装java，想必也对java有所了解了

也许很多像高手以后我这样的初学者都是怎么想的，但其实也不清楚java和jdk和jre和openjava是什么关系，尤其是在ubuntu下安装，会碰到些问题

一、理清楚各个关系

jre只是运行环境 ,jdk是开发环境，openjava是java的开源实现，也就是说oracle的java本身是闭源软件

然后，ubuntu系统自带了openjava一般够用了，但我火狐看魔方java动画看不了，还有学java还是用oracle的吧，android的sdk也需要用！

二、要不要卸载openjava

我想应该是要吧，还要设置什么环境变量的，直接用上面命令行安装好了，注意命令行从oracle官网下载很慢，150M我用了3小时，自己找到替换下吧

------


2014年 08月 23日 星期六 14:26:49 CST

keep me ocuppied or something bad may happen.But if I am displine, nothing will happen at all .
------
2014年 08月 21日 星期四 20:40:04 CST

atom 这个编辑器也不错啊，界面乍看像sublime text 还可以md预览，welcome信息简洁
