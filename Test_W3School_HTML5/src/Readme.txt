学习地址：http://www.w3school.com.cn/html5/index.asp

为 HTML5 建立的一些规则：

    新特性应该基于 HTML、CSS、DOM 以及 JavaScript。
    减少对外部插件的需求（比如 Flash）
    更优秀的错误处理
    更多取代脚本的标记
    HTML5 应该独立于设备
    开发进程应对公众透明
    
========================================================    

新特性

HTML5 中的一些有趣的新特性：

    用于绘画的 canvas 元素
    用于媒介回放的 video 和 audio 元素
    对本地离线存储的更好的支持
    新的特殊内容元素，比如 article、footer、header、nav、section
    新的表单控件，比如 calendar、date、time、email、url、search

========================================================    

视频：
当前，video 元素支持三种视频格式：
Ogg = 带有 Theora 视频编码和 Vorbis 音频编码的 Ogg 文件
MPEG4 = 带有 H.264 视频编码和 AAC 音频编码的 MPEG 4 文件
WebM = 带有 VP8 视频编码和 Vorbis 音频编码的 WebM 文件

<video> 标签的属性
属性 	值 	描述
autoplay 	autoplay 	如果出现该属性，则视频在就绪后马上播放。
controls 	controls 	如果出现该属性，则向用户显示控件，比如播放按钮。
height 	pixels 	                      设置视频播放器的高度。
loop 	loop 	                      如果出现该属性，则当媒介文件完成播放后再次开始播放。
preload 	preload     如果出现该属性，则视频在页面加载时进行加载，并预备播放。 如果使用 "autoplay"，则忽略该属性。
src 	url 	要播放的视频的 URL。
width 	pixels 	设置视频播放器的宽度。

HTML5 <video> - 方法、属性以及事件

下面列出了大多数浏览器支持的视频方法、属性和事件：
方法 	          属性 	                      事件
play() 	currentSrc 	play
pause() currentTime pause
load() 	videoWidth 	progress
canPlayType videoHeight 	error
	  	duration 	timeupdate
	  	ended 	    ended
	  	error 	    abort
	  	paused 	    empty
	  	muted 	    emptied
	  	seeking 	waiting
	  	volume 	    loadedmetadata
	  	height 	 
	  	width 	 



========================================================
什么是SVG？

    SVG 指可伸缩矢量图形 (Scalable Vector Graphics)
    SVG 用于定义用于网络的基于矢量的图形
    SVG 使用 XML 格式定义图形
    SVG 图像在放大或改变尺寸的情况下其图形质量不会有损失
    SVG 是万维网联盟的标准

SVG 的优势
	与其他图像格式相比（比如 JPEG 和 GIF），使用 SVG 的优势在于：

    SVG 图像可通过文本编辑器来创建和修改
    SVG 图像可被搜索、索引、脚本化或压缩
    SVG 是可伸缩的
    SVG 图像可在任何的分辨率下被高质量地打印
    SVG 可在图像质量不下降的情况下被放大

  
 

Canvas 和 SVG 都允许您在浏览器中创建图形，但是它们在根本上是不同的。
SVG

SVG 是一种使用 XML 描述 2D 图形的语言。

SVG 基于 XML，这意味着 SVG DOM 中的每个元素都是可用的。您可以为某个元素附加 JavaScript 事件处理器。

在 SVG 中，每个被绘制的图形均被视为对象。如果 SVG 对象的属性发生变化，那么浏览器能够自动重现图形。
Canvas

Canvas 通过 JavaScript 来绘制 2D 图形。

Canvas 是逐像素进行渲染的。

在 canvas 中，一旦图形被绘制完成，它就不会继续得到浏览器的关注。如果其位置发生变化，那么整个场景也需要重新绘制，包括任何或许已被图形覆盖的对象。
Canvas 与 SVG 的比较

下表列出了 canvas 与 SVG 之间的一些不同之处。
Canvas

    依赖分辨率
    不支持事件处理器
    弱的文本渲染能力
    能够以 .png 或 .jpg 格式保存结果图像
    最适合图像密集型的游戏，其中的许多对象会被频繁重绘

SVG

    不依赖分辨率
    支持事件处理器
    最适合带有大型渲染区域的应用程序（比如谷歌地图）
    复杂度高会减慢渲染速度（任何过度使用 DOM 的应用都不快）
    不适合游戏应用

========================================================
地理定位：
Geolocation（地理定位）用于定位用户的位置。

 
 
 
========================================================

在客户端存储数据

HTML5 提供了两种在客户端存储数据的新方法：
    localStorage - 没有时间限制的数据存储
    sessionStorage - 针对一个 session 的数据存储

之前，这些都是由 cookie 完成的。但是 cookie 不适合大量数据的存储，因为它们由每个对服务器的请求来传递，这使得 cookie 速度很慢而且效率也不高。
在 HTML5 中，数据不是由每个服务器请求传递的，而是只有在请求时使用数据。它使在不影响网站性能的情况下存储大量数据成为可能。
对于不同的网站，数据存储于不同的区域，并且一个网站只能访问其自身的数据。
HTML5 使用 JavaScript 来存储和访问数据。

localStorage 方法存储的数据没有时间限制。第二天、第二周或下一年之后，数据依然可用。
sessionStorage 方法针对一个 session 进行数据存储。当用户关闭浏览器窗口后，数据会被删除。 
 
 

========================================================
使用 HTML5，通过创建 cache manifest 文件，可以轻松地创建 web 应用的离线版本。
什么是应用程序缓存（Application Cache）？
   HTML5 引入了应用程序缓存，这意味着 web 应用可进行缓存，并可在没有因特网连接时进行访问。

应用程序缓存为应用带来三个优势：
    离线浏览 - 用户可在应用离线时使用它们
    速度 - 已缓存资源加载得更快
    减少服务器负载 - 浏览器将只从服务器下载更新过或更改过的资源。

========================================================   
什么是应用程序缓存（Application Cache）？ 
http://www.w3school.com.cn/html5/html_5_app_cache.asp

HTML5 引入了应用程序缓存，这意味着 web 应用可进行缓存，并可在没有因特网连接时进行访问。

应用程序缓存为应用带来三个优势：
    离线浏览 - 用户可在应用离线时使用它们
    速度 - 已缓存资源加载得更快
    减少服务器负载 - 浏览器将只从服务器下载更新过或更改过的资源。


======================================================== 

什么是 Web Worker？

当在 HTML 页面中执行脚本时，页面的状态是不可响应的，直到脚本已完成。

web worker 是运行在后台的 JavaScript，独立于其他脚本，不会影响页面的性能。您可以继续做任何愿意做的事情：点击、选取内容等等，而此时 web worker 在后台运行。


========================================================
HTML5 服务器发送事件（server-sent event）允许网页获得来自服务器的更新。
Server-Sent 事件 - 单向消息传递

Server-Sent 事件指的是网页自动获取来自服务器的更新。

以前也可能做到这一点，前提是网页不得不询问是否有可用的更新。通过服务器发送事件，更新能够自动到达。

例子：Facebook/Twitter 更新、估价更新、新的博文、赛事结果等。


======================================================== 
HTML5输入类型
HTML5 拥有多个新的表单输入类型。这些新特性提供了更好的输入控制和验证。
    email
    url
    number
    range
    Date pickers (date, month, week, time, datetime, datetime-local)
    search
    color



======================================================== 
HTML5 的新的表单元素：

HTML5 拥有若干涉及表单的元素和属性。

本章介绍以下新的表单元素：
    datalist
    keygen
    output
    
    
    
======================================================== 
HTML5 的新的表单属性

本章讲解涉及 <form> 和 <input> 元素的新属性。
新的 form 属性：
    autocomplete
    novalidate

新的 input 属性：
    autocomplete
    autofocus
    form
    form overrides (formaction, formenctype, formmethod, formnovalidate, formtarget)
    height 和 width
    list
    min, max 和 step
    multiple
    pattern (regexp)
    placeholder
    required
    
    
========================================================






 