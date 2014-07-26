我用这样的方式写作，从一开始就碰到个不是很顺的地方

每次要引用其他地方的网页的时候，要分别拷贝网页标题和网址

用vimperator拷贝网址是很简单y就行了，但还要拷贝标题就要老方法了，不喜欢那么麻烦

今天搜索下，就把这个问题解决了，按Y就可以拷贝url和title，而且二者直接有空行，方便黏贴到vimwiki这里

参考如下


Vimperator 拷贝当前网页标题与URL成脚注形式文本 – 陈三

http://www.zfanw.com/blog/vimperator-copy-footnote-form-text.html#fn:2


有了网址和标题就容易备查了

嘿嘿，自己再改良下就是我想要的效果了

如果有这样的小工具，我就更愿意引用源地址了

命令如下

`nmap Y :js<Space>util.copyToClipboard(buffer.title+"\n\n"+buffer.URL)<Return>`
