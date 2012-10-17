---
author: root
title: 弹出窗口代码
excerpt:
layout: post
category:
  - Life
tags: [ ]
post_format: [ ]
---
转自：www.zcool.com.cn 

【1、最基本的弹出窗口代码】  
其实代码非常简单： 

　因为这是一段javascripts代码，所以它们应该放在之间。是对一些版本低的浏览器起作用，在这些老浏览器中不会将标签中  
的代码作为文本显示出来。要养成这个好习惯啊。  
　window.open (‘page.html’) 用于控制弹出新的窗口page.html，如果page.html不与主窗口在  
同一路径下，前面应写明路径，绝对路径(http://)和相对路径(../)均可。  
　用单引号和双引号都可以，只是不要混用。  
　这一段代码可以加入HTML的任意位置，和之间可以，间也可以，  
越前越早执行，尤其是页面代码长，又想使页面早点弹出就尽量往前放。 

【2、经过设置后的弹出窗口】  
　下面再说一说弹出窗口的设置。只要再往上面的代码中加一点东西就可以了。我们来定制这个  
弹出的窗口的外观，尺寸大小，弹出的位置以适应该页面的具体情况。 

　参数解释：  
js脚本结束 

【3、用函数控制弹出窗口】  
　下面是一个完整的代码。 

..任意的页面内容… 

　这里定义了一个函数openwin(),函数内容就是打开一个窗口。在调用它之前没有任何用途。  
怎么调用呢？  
　方法一： 浏览器读页面时弹出窗口；  
　方法二： 浏览器离开页面时弹出窗口；  
　方法三：用一个连接调用： 

【4、同时弹出2个窗口】  
　对源代码稍微改动一下： 

　为避免弹出的2个窗口覆盖，用top和left控制一下弹出的位置不要相互覆盖即可。最后用上面  
说过的四种方法调用即可。  
注意：2个窗口的name(newwindows和newwindow2)不要相同，或者干脆全部为空。OK？ 

【5、主窗口打开文件1.htm，同时弹出小窗口page.html】  
　如下代码加入主窗口区： 

加入区：  
open即可。 

【6、弹出的窗口之定时关闭控制】  
　下面我们再对弹出的窗口进行一些控制，效果就更好了。如果我们再将一小段代码加入弹出的  
页面(注意是加入到page.html的HTML中，可不是主页面中，否则…)，让它10秒后自动关闭是不  
是更酷了？  
　首先，将如下代码加入page.html文件的区： 

　然后，再用 这一句话代替page.html中原有的这一句就可  
以  
了。(这一句话千万不要忘记写啊！这一句的作用是调用关闭窗口的代码，10秒钟后就自行关闭  
该  
窗口。) 

【7、在弹出窗口中加上一个关闭按钮】 

呵呵，现在更加完美了！ 

【8、内包含的弹出窗口-一个页面两个窗口】  
上面的例子都包含两个窗口，一个是主窗口，另一个是弹出的小窗口。  
通过下面的例子，你可以在一个页面内完成上面的效果。 

　看看 OpenWindow.document.write()里面的代码不就是标准的HTML吗？只要按照格式写更多的  
行即可。千万注意多一个标签或少一个标签就会出现错误。记得用OpenWindow.document.close  
()  
结束啊。 

【9、终极应用–弹出的窗口之Cookie控制】  
　回想一下，上面的弹出窗口虽然酷，但是有一点小毛病(沉浸在喜悦之中，一定没有发现吧？)  
比如你将上面的脚本放在一个需要频繁经过的页面里(例如首页)，那么每次刷新这个页面，窗口  
都会弹出一次，是不是非常烦人？:-(  
　有解决的办法吗？Yes! Follow me.  
　我们使用cookie来控制一下就可以了。  
　首先，将如下代码加入主页面HTML的区： 

　然后，用（注意不是openwin而是loadpop啊！）替换主页面中  
原  
有的这一句即可。你可以试着刷新一下这个页面或重新进入该页面，窗口再也不会弹出  
了。真正的Pop-Only-Once！  
　写到这里弹出窗口的制作和应用技巧基本上算是完成了，俺也累坏了，一口气说了这么多，希  
望对正在制作网页的朋友有所帮助俺就非常欣慰了。  
　需要注意的是，JS脚本中的的大小写最好前后保持一致。