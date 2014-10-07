How to look up dictionary via command line on Linux - Linux FAQ

http://xmodulo.com/how-to-look-up-dictionary-via-command-line-on-linux.html

ii dictd dict-gcide
dict -I 
dict -d gcide 'love' |less
------
第 [mozlab] Lightweight MozRepl + Vim integration: Refresh Firefox, and restore scroll position on Vim save ! - Google 网上论坛 个

https://groups.google.com/forum/#!topic/mozlab/dJrRJQv474E


{{{
autocmd BufWriteCmd  *.html,*.css,*.gtpl  : call Refresh_firefox() 

function! Refresh_firefox()
    if &modified
        write
        silent !echo  'vimYo = content.window.pageYOffset;
                     \ vimXo = content.window.pageXOffset;
                     \ BrowserReload();
                     \ content.window.scrollTo(vimXo,vimYo);
                     \ repl.quit();'  |
                     \ nc -q 1 localhost 4242 2>&1 > /dev/null
    endif
endfunction 

}}}
------
rlwrap  telnet 
------
git config --global credential.helper store 

记住密码 
------
screen -x test

c-a-c/w/n/p/d
------
centos

cat /var/log/secure|awk '/Failed/{print $(NF-3)}'|sort|uniq -c|awk '{print $2"="$1;}'

ubuntu

cat /var/log/auth.log|awk '/Failed/{print $(NF-3)}'|sort|uniq -c|awk '{print $2"="$1;}'
------
Generating QR Codes in Linux » Linux Magazine

http://www.linux-magazine.com/Online/Features/Generating-QR-Codes-in-Linux


------
ii qrencode QtQR
------
apache2.conf add the path other than /var/www
------
remove ibus ; ii fcitx fcitx-pinyin

(after installing, something went wrong with system setting panel)
------
recordMyDesktop--no sound

Kazam  ---really worked just checkout sound from speakers
------
speed up dash display-->using ccsm, set on-blur to no-blur
------
vim n **/*.txt
:argdo %s/a/A/ge|update

TOhtml
------
vim :g/^/m 0 反转行
------
mygit.sh cheat
------
git config --global core.quotepath false(  中文文件)
------
ii Build new apps quickly

ii gnome do
------
git error

remote: fatal: unable to create thread: Resource temporarily unavailable

Git pull fails with bad pack header error - Stack Overflow

http://stackoverflow.com/questions/7362709/git-pull-fails-with-bad-pack-header-error

git config --global pack.windowMemory "100m"
git config --global pack.packSizeLimit "100m"
git config --global pack.threads "1" 
------
ubuntu ipad 充电 

sudo apt-get install  libusb-1.0-0-dev

https://github.com/mkorenkov/ipad_charge
------
Python的包管理工具Pip - 大毛的部落 - 博客频道 - CSDN.NET

http://blog.csdn.net/maowenbin/article/details/6622307


pip install
curl -O http://python-distribute.org/distribute_setup.py
$ python distribute_setup.py
------

Ubuntu 安装软件备份工具 Aptik

sudo add-apt-repository ppa:teejee2008/ppa
------
parcellite  clipboard
------
Ubuntu 14.04 及衍生版本安装 Tor Browser 3.6.3_Linux教程_Linux公社-Linux系统门户网站

http://www.linuxidc.com/Linux/2014-08/105259.htm

sudo add-apt-repository ppa:webupd8team/tor-browser
------
ubuntu postgresql  ii postgresql{,-client} php5-psql pgadmin3
------
14.04 ubuntu caps_lock change to ctrl using gnome-tweak-tool
------
自动挂载ntfs分区

/dev/hda1 /media/windows ntfs utf8,umask=0222 0 0
------
ibus-daemon -x -d -r
------
/usr/share/doc/phpmyadin    there are other documents

man dpkg-recofigure

debconf-show

phpmyadmin 用apt安装后localhost/phpmyadmin 找不到

ll /usr/share/phpmyadmin  原来在这，自己ln吧

webmin 默认帐号就是登录帐号，搜索的时候才想起之前有这样做过印象
------
ubuntu 14.04 Server 如何安装 webmin | IMCN

http://imcn.me/html/y2014/21254.html


------
ubuntu lamp web

Ubuntu 14.04 LTS Server 安装 LAMP Server | IMCN

http://imcn.me/html/y2014/20481.html


------
apt-cache search php5
------
git config --global core.excludesfile ~/.gitignore
------
Ubuntu 14.04 LTS Server 安装web LAMP Server_服务器应用_Linux公社-Linux系统门户网站

http://www.linuxidc.com/Linux/2014-06/102919.htm


------

Gnome-keyring总是提示输入密码问题

cd ~/.gnome2/keyrings/
cp login.keyring login.keyring.backup
rm ~/.gnome2/keyrings/login.keyring 
------
alsamixer 音量
------
autokey powerfull than autohotkey
------
ctrl+:  输入法剪贴板？
------

How To Install Java On Ubuntu 14.04 – 卡书

http://www.kashu.org/3435.html

In line copy and paste to system clipboard - Vim Tips Wiki

http://vim.wikia.com/wiki/In_line_copy_and_paste_to_system_clipboard

------
phatch 图片批处理
------
 grep -r -i roy
------
自动换壁纸 variety ppa
------
indicator-multiload 系统运行指示
------
Whatever you're learning, if you want to learn it fast and keep that knowledge with you all your life, then do this:
1) Install Anki.
2) Learn to use it.
3) Stick to it.
By far one of the most important pieces of software I've ever found out!
------
By far one of the most important pieces of software I've ever found out!
------
网页背景色yong用gm设置成我站点的背景色，现在舒服多了，#e6e6e6，感觉整个互联网都被我站点同化了！哇哈哈哈 愚蠢的地球人
------
pcman file manager
------
find -inum 1704875 -exec rm {} \; 删除乱码文件
------
for file in * ;do sed -i '/google/d' $file;done
------
xx=$(eval pwd)
------
dialog --msgbox 'you are handsome' 222 222

dialog/Xdialog使用範例（Linux/bash）

http://www.360doc.com/content/11/0928/15/834950_151898745.shtml


mytime=`dialog --stdout -title 'title here' --calendar 'title calneder' 0 0 8 8 1999`
------
inotify-tools

unison

incron

inoticoming
------
       ssh-copy-id –i .ssh/id_rsa.pub user1@192.168.0.101
------
read -s name  输入密码不回显 echo $name

------
Home · bard/mozrepl Wiki

https://github.com/bard/mozrepl/wiki


MozRepl
------
command line - Close current tab firefox using terminal - Ask Ubuntu

http://askubuntu.com/questions/295584/close-current-tab-firefox-using-terminal


wmctrl -a firefox

命令行控制程序窗口
------


wmctrl -a firefox

命令行控制程序窗口
------

http://askubuntu.com/questions/295584/close-current-tab-firefox-using-terminal


wmctrl -a firefox

命令行控制程序窗口
------
设置LANG

v /etc/default/locale
------
复制为curl命令
------
Git 获取远程分支 - WNFK - 博客园

http://www.cnblogs.com/hanxianlong/archive/2012/09/10/2678659.html

git fetch

git checkout -b localbranch orgin/remotebranch



Git中从远程的分支获取最新的版本到本地 - - 博客频道 - CSDN.NET

http://blog.csdn.net/chb2000/article/details/6976022

git fetch origin master:tmp

git diff tmp

git merge tmp

------
This can be done using Python 2.x by running python -m SimpleHTTPServer or Python 3.x with python -m http.server 

using Ruby by installing and running asdf,
------
mysql 随机取出记录
{{{
SELECT *
FROM `table` AS t1 JOIN (SELECT ROUND(RAND() * ((SELECT MAX(id) FROM `table`)-(SELECT MIN(id) FROM `table`))+(SELECT MIN(id) FROM `table`)) AS id) AS t2
WHERE t1.id >= t2.id
ORDER BY t1.id LIMIT 1;
}}}
------
php5-sqlite ii安装
------
google pagespeed 安装

Apache加速模块mod_pagespeed安装使用详细介绍_Linux/apache_脚本之家

http://www.jb51.net/article/48065.htm


------
屏幕录像

sudo apt-get install gtk-recordmydesktop 
------
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

#cli.prompt=hello world :> 

 #cli.prompt=`echo date('H:i:s');` php > 

提示符颜色变量设置


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
autocump ---> j -stat  : autojump -s : jo movie : j roya movie

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
imagemagick
zbar-tools
keynav
ack-grep
PlayOnLinux
