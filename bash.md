svn 超简单教程，还是自己摸索的，git果然有帮助

1 svn add a.txt

2 svn commit a.txt
------
Linux 终端字符颜色设置

http://www.phpfans.net/article/htmls/200905/MjczMTI4.html


echo -e "\\033[0;32mtest"
------
php command line 命令行

php -a

echo 6+4;

php提示符

#cli.prompt=hello world :> 

 #cli.prompt=`echo date('H:i:s');` php > 

提示符颜色变量设置

#cli.prompt=\e[032m\v \e[031m\b \e[34m\> \e[0m

php 内置浏览器

PHP: Built-in web server - Manual

http://php.net/manual/en/features.commandline.webserver.php

0.0.0.0:8000

 php -S localhost:8889   
------
google tts txt发音


wget 'http://translate.google.com/translate_tts?tl=zh&q=%E6%88%91%E5%96%9C%E6%AC%A2%E4%BD%A0' -O like.mp3

wget 'http://translate.google.com/translate_tts?tl=en&q=text' -O jj.mp3
------
ssh rsync port 备份  ~/work/myrsync.sh 700 用ssh连接比较简单，配置好无密码登陆就行

1 不知道vps要不要先开启rsync 

chkconfig rsync on  | chkconfig --list |grep rsync

?  /etc/xinetd.d/rsync   disable = on

reboot | lsof -i :873

? rsync --daemon

不同端口

`rsync -av -e ssh $basedir ${id}@${host}:${remotedir}`


` rsync -e "ssh -p 1234" -avz --bwlimit=3000 REMOTE_HOST:data_path .`


{{{


[root@node1 backup]# crontab -e

*/5 * * * * /backup/rsync.sh > /dev/null
}}}

注意 crontab 都要用绝对路径
------
apache htaccess

1 a2enmod rewrite

2 apache2.conf -- override all

3 site_document_root .htaccess 

4. 因为我的ci是在子目录，所以要相应修改RewriteRule ^(.*)$ index.php\$1 [L]
------
无意中按到一个快捷键vim shift+k 可以查看man 当前光标下的关键字


tail -f a.txt 实时查看文件
------
强制更新push 用于reset后

git reset --hard HEAD

饿，其实就是强制push，不管是不是reset，就算全新或完全不同的repo，只要remote origin是此repo的话都可以！
git push origin +master

------
ubuntu 清除dns缓存
sudo /etc/init.d/dns-clean start
------
gnome-session-properties

开机启动项

------
ipad上的screen中文乱码

在/etc/screenrc 加入中文编码

{{{

defencoding utf-8
encoding utf-8 utf-8
}}}
------
恢复默认滚动条


    gsettings set com.canonical.desktop.interface scrollbar-mode normal

隐藏式滚动条

    gsettings reset com.canonical.desktop.interface scrollbar-mode
------
Betty：和你的Linux说说话 - 桌面应用

http://linux.cn/article-3453-1.html

`ysh whats my username`
------

    login shell 启动--->读取/etc/porfile文件--->读取~/.bash_profile文件
    no-login shell 启动--->读取~/.bashrc文件
    exec env -i /bin/bash命令会开启一个全新的non-login shell。

su - lfs #注意中间这个 - 符号是一定要的，代表为lfs用户启动一个login shell 
------
关于SVG文件在Firefox中正确显示的研究 - DZQABC - 博客园

http://www.cnblogs.com/dongzhiquan/archive/2009/10/10/1994727.html


svg 在火狐firefox中显示， 在hight后面

`xmlns="http://www.w3.org/2000/svg"`
------
怎样在 Ubuntu Unity Dash 添加关机、重启选项 shutdown - 技术

http://linux.cn/article-2652-1.html


------
sublime text 中文输入

点滴记录——在Ubuntu 14.04中使SublimeText 3支持中文输入法 - Cynric 的博客 - 博客频道 - CSDN.NET

http://blog.csdn.net/cywosp/article/details/32350899

`LD_PRELOAD=/home/roya/d/sublime_text/sublime_text_3/sublime_text_fcitx.so st $1`

------
vim  q:  显示运行过的外部命令历史
------
路由器还可以telnet？！
------
focus on mouse

gnome-tweak-tool 

窗口-->focus mode = mouse
{{{
gsettings set org.gnome.desktop.wm.preferences focus-mode 'sloppy'

gsettings set org.gnome.desktop.wm.preferences focus-mode 'mouse'

gsettings set org.gnome.desktop.wm.preferences auto-raise true

gsettings set org.gnome.desktop.wm.preferences auto-raise-delay 500

gsettings set org.gnome.desktop.wm.preferences raise-on-click false


gconftool-2 --type string --set /apps/metacity/general/focus_mode mouse

gconftool-2 --type boolean --set /apps/metacity/general/auto_raise true

gconftool-2 --type integer --set /apps/metacity/general/auto_raise_delay 600

}}}
------
`sudo ln -s /usr/bin/nodejs /usr/bin/node`

因为是使用的apt-get install 方式安装，所以出现以上问题
------
删除有特殊字符的文件 `rm -- asdfasdf`
------

`cat >>myfile << EOF`

命令行直接输入文件内容
------

xdotool
键盘鼠标自动化操作


http://xmodulo.com/2014/07/simulate-key-press-mouse-movement-linux.html

`xdotool key alt+Tab`

`xdotool type 'asdfasdf'`

`xdotool search --name vimperator key g+t`

`xdotool mousemove 11 11 click 1`
------

sudo apt-get install bsdgames

There are a total of forty-three games in the collection! Here is the list: random, gomoku, caesar, countmail, rot13, bcd, atc, number, boggle, quiz, morse, teachgammon, snake, snscore, pig, wargames, tetris-bsd, adventure, arithmetic, worms, hunt, canfield, battlestar, rain, robots, cribbage, dab, sail, wump, trek, phantasia, wtf, go-fish, monop, backgammon, worm, hack, ppt, primes, hangman, pom, cfscores, and mille.




adventure ,worm, trek, bastet, tetris-bsd,ninvaders,moon-buggy,tanglet

居然有个pacman在ipad上编译成功运行了，倒是在ubuntu上编译不了
------

学了一招 :用jk来代替esc
------

http://www.cnseay.com/816/

linux命令
------
sudo egrep '(vmx|svm)' --color=always /proc/cpuinfo

是否支持硬件虚拟化
-----------
http://www.kvm.la/kill-login-ssh-user.html

剔除登陆账号

kuser -k /dev/pts/0

who >>>kill -9 222
------------
Centos安装davfs2挂载WebDAV

http://www.kvm.la/808.html

`ii davfs2`

除了box.com还有什么支持webdav？'owncloud'?
------
查看磁盘空间大小

`df -h`

`du -sh`
-------
`find . -iname '*txt*' --exec mv -v {} /home/test \;`

`name=royaso;${name:2:3};`

`find . -maxdepth 1 -type d -empty`

`<test.txt sed -n '22,33p'`
-------
登录Ubuntu Linux需要输入密码以解锁密钥环的解决  

`seahorse`  ->login 

or `sudo rm -rf ~./gnome2/keyrings/*`


-------
gnome应用技巧

* 修改目录图标：可以把nautilus中看到的图片，直接拖放到目录属性的图标上就可以了。
 * 压着shift拖动窗口可以让窗口吸附在屏幕的边缘。
 
----------
 转换 mp3 标签编码 :
`  sudo apt-get install python-mutagen;find . -iname '*.mp3' -execdir mid3iconv -e GBK {} \;`
-------------
sismics reader (a rss reader like gr)
----------
挂载远程linux主机文件到本机

http://article.yeeyan.org/view/90729/347310

`sshfs -p 23402 root@234.234.34.324:/ ~/vps`

*当cp命令用就行了，ps：sshfs在14.04居然就自带了，什么也不用多做，就那条命令*
----
w3m elinks lync
----------
关于github的技巧

http://linux.cn/article-2894-1.html

curl -i http://git.io -F 'url=asdfdasf' 

 gist  asdfdasf.git-------.asdfasdf.pibb
----------
视频提取音频 extract audio from video using ffmpeg and libav-tools

1 install those two tools: ffmpeg , libav-tools

2 convert commands :avconv -i a.mp4 asdf.mp3
-------
zsh!!

http://linux.cn/article-1308-1.html

{{{
autojump ---> j -stat  : autojump -s : jo movie : j roya movie

kill firefox

1 -->last directory
2 ---> last second directory

git ad<tab>


$ alias -s log=less
$ ~/package/tomcat/log/catalina.log # 相当于 less ~/package/tomcat/log/catalina.log
$ alias -g PR=http_proxy=127.0.0.1:8087
$ PR curl https://twitter.com # 相当于 http_proxy=127.0.0.1:8087 curl https://twitter.com
}}}
----------
apt-fast

`sudo add-apt-repository ppa:apt-fast/stable`
-------------
视频截取gif

` $ ffmpeg -t 5 -ss 00:00:10 -i funny.mp4 out%04d.gif `

优化大小

`convert -resize 100 a.gif b.gif`

-------------
`clex`  命令行文件管理
`ranger` 更强大
---------
检测cpu温度

`watch -n 1 sensors`

`watch -n 1 " "`  

----------
bash 与 或 命令 

`$ [ -f a.txt ] && echo 'yes' || echo 'no'`

----------
ubuntu 安装ffmpeg

http://ask.xmodulo.com/compile-ffmpeg-ubuntu-debian.html

` sudo apt-get install git make nasm pkg-config libx264-dev libxext-dev libxfixes-dev zlib1g-dev `

{{{
 git clone https://github.com/FFmpeg/FFmpeg.git
 cd FFmpeg
 ./configure --enable-nonfree --enable-gpl --enable-libx264 --enable-x11grab --enable-zlib
 make 

 sudo make install 
}}}
------------

关机重启命令

{{{
sudo add-apt-repository ppa:atareao/atareao
sudo apt-get update && sudo apt-get install power-commands
}}}
现在就可以在 dash 里面搜索到了：

--------
`cutycapt --url=http://www.cnn.com --out=cnn.png`
网页截图


music on console
`cmus` `mocp`

http://www.youbangtuo.net/post/2012-07-21/40030364102
-------------------
用 dircolors -p  可以 看到缺省的颜色设置

`find *.txt -exec sh -c 'mv {} {}.py' \;`

 批量重命名
{{{
    #!/bin/bash  
      
    // batch_change_GB2312_to_UTF-8  
      
    cd directory  
    find ./ -type f -name "*.java" | while read line;do  
    echo $line  
    iconv -f GB2312 -t UTF-8 $line > ${line}.utf8  
    mv $line ${line}.gb2312  
    mv ${line}.utf8 $line  
    done  
}}}


delete other files except zip and iso

`find . -type f -not \( -name '*.zip' -or -name '*.iso' \) -delete`

--------

 `${1}` 第一个参数
        {{{
vim scp://root@12.121.21.12:323/${1}

useage: vimhost "/root/test.txt"
}}}
----

{{{
sudo pip install Beautifulsoup
sudo pip uninstall Beautifulsoup
}}}

-----------
基本的linux命令，多多看看man

{{{
ls
diff
ssh
wget
mkdir
mv
cp
echo
curl
sed
grep
cut
paste
asciidoctor
yelp 'browser system documentation' (like xml)
sed '2,3s/oo/ii/g' test
mono
gdb
newsbeuter  rss
gThumb
gmusicbrowser
deepin-music-player http://www.linuxidc.com/Linux/2014-05/101789.htm
deepin-media-player
cmus  :music player like mocp
}}}
