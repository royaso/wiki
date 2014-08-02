这是用生命在折腾啊！！

POP3协议接收邮件--命令行窗口下_翻山越岭的另一边_新浪博客

http://blog.sina.com.cn/s/blog_6dbfc2a901014yrt.html

*成功,记得开启smtp和pop*

SMTP协议--在cmd下利用命令行发送邮件_翻山越岭的另一边_新浪博客

http://blog.sina.com.cn/s/blog_6dbfc2a901014yqx.html

----------

telnet smtp.qq.com 25 (25端口)

helo qq.com

auth login

echo '1111@qq.com' |base64

echo 'password' |base64

mail from:1111@qq.com （no need base64)

rcpt to:alison@qq.com

data


from:

to:

subject:

(a blank line)

.

(end with a period)

-----
test with 中文

-----

rlwrap: 让telnet支持命令历史 - u012973744的专栏 - 博客频道 - CSDN.NET

http://blog.csdn.net/u012973744/article/details/19113889



企业路由器应用——命令行—管理 - TP-LINK 服务支持

http://service.tp-link.com.cn/detail_article_114.html


