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
}}}
