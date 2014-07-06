%toc
------



== vim [[==]]
- [[vim|vim 设置集合]]
- vim编辑远程文件
        - vim scp://root@12.12.12.12:1212//root/tet.txt
        *note there  is  two backslash in the path
- vimperator set editor to vim
本以为个会成功的`set editor=gnome-terminal\ -e\ vim`
折腾半天，还是只能用xterm　`set editor=xterm\ -e\ vim`

`ci c-i`
== 鼠标支持 ==
`set mouse=a`

鼠标选中不能复制的话，去掉上面那句

==vim插件管理vundle==
基本上在vimrc里配置如下，去掉了示例插件的安装
支持各种安装方式：github，ftp等等

{{{
set nocompatible
filetype off   
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()

" let Vundle manage Vundle, required
 Plugin 'gmarik/Vundle.vim'
 call vundle#end()            " required
 filetype plugin indent on    " required
}}}
