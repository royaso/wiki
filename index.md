%template default

我一定要把电用光！
---------

开始前准备：
如果您确定想要着手操作的话，首先您应该了解linux的一些基础知识、ssh，shell和bash基本操作、基本编译等，并且要有一定的英语基础。这是一篇面向有一定基础的读者的文章，文中部分知识在本文中不会详细解释，如果您有什么不懂的地方，你来打我啊，咳咳，建议您先从基础学起。


 == [[about-about|archives]] ==
 
永远相信美好的事物即将发生 
--------
所謂‘常在河邊走，哪有不溼鞋',終於也輪到我中獎了吧！

如何估计博客网站广告报价？【内含福利】 | 土木坛子

https://tumutanzi.com/archives/12870/comment-page-1#comment-57415


---------

这种事在互联网圈很常见，诸如办抽奖活动伪随机谁*获得iphone，其实人名，iphone都是假的，制造一种活跃度高的现象，这几乎是行业内人人皆知的事，我只能说你还没习惯这种事」——Haroel Ho这种事在互联网圈很常见，诸如办抽奖活动伪随机谁*获得iphone，其实人名，iphone都是假的，制造一种活跃度高的现象，这几乎是行业内人人皆知的事，我只能说你还没习惯这种事」——Haroel Ho

---------
I have been bothered by the problem for so long time even I dont recall when It started.

my final solution is 

    inoremap <C-v> <C-v>

and it works great!

once when I <C-v> It paste twice! That is very annoying!

I tried 

    inoremap <C-v> <C-v><C-v>

that seems like make sense, but It's useless cause It doesnt' work!

In the process of fixing this , I tried `inoremap <C-v> i<C-v><esc>`, this makes difference. after some tries, it came down to that final solution.

---------
using WebDav protocal in ubuntu nautilus ( the file manager) to connect to the iPad app : textastic

in a nutshell `dav://192.168.2.101/`

and to get things further, I install davfs2, and now I can mount the webdav to my file system.

`sudo mount -t davfs http://192.168.2.101 /mnt/textastic -o uid=roya,gid=roya,rw`

------------

to be honest, this is how my site was updated

combined with vimwiki ,you have all package

another git hook to save you the trouble having to ssh your server to check out


now you can just write in your vim, push to your server, the server check out your head automatically and BANG, people gets to see it all at nice


update

it's not easy to get my comment here, but it is all me to blamed

normally I can just paste my comment here, save it commit it an push it ,all seems so well.

now bellow is what really happened

since it is been long time since I pull, so to get update , first I need to get to pull down all my updates, and it went well

after I made the change. i issue the command "git status" to see the status,but nothing, it said my working stage is clean, nothing to commit"

what the hell!

afterwards i firgured out that there are two user in my ipad, and also two copy of vimwiki

i just pulled update to mobile user's vimwiki and made the change in root user's vimwiki.

and also note that when i pull in the right vimwiki, it said "index.md no todate" ,the error seems odd, cause i never saw it before, then i know waht the problem is: when i merge the updates i didnt commit my change yet, so it is simple and clear, all i have to to is check out my change to restore index.md to previous state and pull, and it worked out great. i can also take the other more trouble approach , commoit my changes and fixed the merge conflict afterwards.


so what left to do is push all of this changes to get my blog updated.

finally i wanna to say all of this are done soly using my ipad, without using pc, that is impressive right?

probally i will get used to the way it goes 
