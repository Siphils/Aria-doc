
?> 本篇教程会介绍一些进阶功能的使用  

## 链接盒子  

!>这种形式的短代码可以用来创作一个*友情链接*的页面，或者用来作为一个带*图片的链接*使用。  

### `[link-item]` 参数  

| 参数 | 内容 | 是否必需 | 类型 | 
| ------ | ------ | ------ | ------ |
| name | 链接的文字 | 是 | string |
| href | 链接的地址 | 否 | string |
| img | 链接图片 | 是 | string |
| title | 悬停鼠标显示文字 | 否 | string |  

!> 由于`Typecho 1.1`正式版的编辑器解析问题，一定需要用`!!!`包裹短代码  
并且`[link-item]`需要用`[link-box]`包裹住  
属性值之间用空格分开，不要用回换行
基本举例  
```markdown
[link-box]
[link-item name="链接" title="这是一个链接" img="/path/to/image" href="url"]
[/link-box]
``` 
你也可以使用多个`[link-box]`  
```markdown
[link-box]
[link-item .....]
[link-item .....]
[/link-box]

[link-box]
[link-item .....]
[link-item .....]
[/link-box]
``` 
*** 
!> `href`可以为空，那么你就可以像这样使用一个仅为了用于显示图片和文字的`link-item`
```markdown   
!!!
[link-box]
[link-item name="图片" title="这是一张图片" img="/path/to/image"]
[link-item name="图片" title="这是一张图片" img="/path/to/image"]
[link-item name="图片" title="这是一张图片" img="/path/to/image"]
[/link-box]
!!!
```  
也可以用作友情链接  
```markdown  
## 邻居1组
!!!
[link-box]
[link-item name="Siphils" title="Life is what you make it." img="https://cn.gravatar.com/avatar/9d05d12216701bf5135894c55232ae99?d=mp&r=g&s=50" href="https://eriri.ink"]
[/link-box]  
!!!
## 邻居2组
!!!
[link-box]
[link-item name="Siphils" title="Life is what you make it." img="https://cn.gravatar.com/avatar/9d05d12216701bf5135894c55232ae99?d=mp&r=g&s=50" href="https://eriri.ink"]
[/link-box]
!!!
```  
*** 
## 图标  
> 图标用来干什么呢？  
1. 导航栏前边的小图标  
2. 主题默认的一些对应的图标  
3. 个人喜好定制  
4. ...
### 导航栏使用图标  
你可以自己引入额外的图标，比如`FontAwesome`或者`Iconfont`，然后可以在配置项的`icon`参数里填入对应的值。  

!> `icon`参数需要填写完整的类名，例如`iconfont icon-aria-home`或者`fa fa-wikipedia-w`  
主题内置图标前缀为`iconfont`

### 所有图标  
下面为最新版本所有内置图标以及其`class`  

<i class="iconfont icon-aria-archlinux" style="font-size:2rem"></i>	 icon-aria-archlinux	<i class="iconfont icon-aria-search" style="font-size:2rem"></i>	 icon-aria-search<br>
<i class="iconfont icon-aria-os" style="font-size:2rem"></i>	 icon-aria-os	<i class="iconfont icon-aria-friends" style="font-size:2rem"></i>	 icon-aria-friends<br>
<i class="iconfont icon-aria-windows" style="font-size:2rem"></i>	 icon-aria-windows	<i class="iconfont icon-aria-success" style="font-size:2rem"></i>	 icon-aria-success<br>
<i class="iconfont icon-aria-archives" style="font-size:2rem"></i>	 icon-aria-archives	<i class="iconfont icon-aria-book" style="font-size:2rem"></i>	 icon-aria-book<br>
<i class="iconfont icon-aria-ipad" style="font-size:2rem"></i>	 icon-aria-ipad	<i class="iconfont icon-aria-iphone" style="font-size:2rem"></i>	 icon-aria-iphone<br>
<i class="iconfont icon-aria-link" style="font-size:2rem"></i>	 icon-aria-link	<i class="iconfont icon-aria-qq" style="font-size:2rem"></i>	 icon-aria-qq<br>
<i class="iconfont icon-aria-failure" style="font-size:2rem"></i>	 icon-aria-failure	<i class="iconfont icon-aria-reply" style="font-size:2rem"></i>	 icon-aria-reply<br>
<i class="iconfont icon-aria-more" style="font-size:2rem"></i>	 icon-aria-more	<i class="iconfont icon-aria-freebsd" style="font-size:2rem"></i>	 icon-aria-freebsd<br>
<i class="iconfont icon-aria-music" style="font-size:2rem"></i>	 icon-aria-music	<i class="iconfont icon-aria-date" style="font-size:2rem"></i>	 icon-aria-date<br>
<i class="iconfont icon-aria-warning" style="font-size:2rem"></i>	 icon-aria-warning	<i class="iconfont icon-aria-github" style="font-size:2rem"></i>	 icon-aria-github<br>
<i class="iconfont icon-aria-about" style="font-size:2rem"></i>	 icon-aria-about	<i class="iconfont icon-aria-emotion" style="font-size:2rem"></i>	 icon-aria-emotion<br>
<i class="iconfont icon-aria-windows10" style="font-size:2rem"></i>	 icon-aria-windows10	<i class="iconfont icon-aria-cancel" style="font-size:2rem"></i>	 icon-aria-cancel<br>
<i class="iconfont icon-aria-chrome" style="font-size:2rem"></i>	 icon-aria-chrome	<i class="iconfont icon-aria-email" style="font-size:2rem"></i>	 icon-aria-email<br>
<i class="iconfont icon-aria-centos" style="font-size:2rem"></i>	 icon-aria-centos	<i class="iconfont icon-aria-debian" style="font-size:2rem"></i>	 icon-aria-debian<br>
<i class="iconfont icon-aria-gentoo" style="font-size:2rem"></i>	 icon-aria-gentoo	<i class="iconfont icon-aria-ubuntu" style="font-size:2rem"></i>	 icon-aria-ubuntu<br>
<i class="iconfont icon-aria-wechat" style="font-size:2rem"></i>	 icon-aria-wechat	<i class="iconfont icon-aria-browser" style="font-size:2rem"></i>	 icon-aria-browser<br>
<i class="iconfont icon-aria-android" style="font-size:2rem"></i>	 icon-aria-android	<i class="iconfont icon-aria-submit" style="font-size:2rem"></i>	 icon-aria-submit<br>
<i class="iconfont icon-aria-tag" style="font-size:2rem"></i>	 icon-aria-tag	<i class="iconfont icon-aria-code" style="font-size:2rem"></i>	 icon-aria-code<br>
<i class="iconfont icon-aria-edge" style="font-size:2rem"></i>	 icon-aria-edge	<i class="iconfont icon-aria-firefox" style="font-size:2rem"></i>	 icon-aria-firefox<br>
<i class="iconfont icon-aria-opera" style="font-size:2rem"></i>	 icon-aria-opera	<i class="iconfont icon-aria-safari" style="font-size:2rem"></i>	 icon-aria-safari<br>
<i class="iconfont icon-aria-markdown" style="font-size:2rem"></i>	 icon-aria-markdown	<i class="iconfont icon-aria-view" style="font-size:2rem"></i>	 icon-aria-view<br>
<i class="iconfont icon-aria-360" style="font-size:2rem"></i>	 icon-aria-360	<i class="iconfont icon-aria-ie" style="font-size:2rem"></i>	 icon-aria-ie<br>
<i class="iconfont icon-aria-maxthon" style="font-size:2rem"></i>	 icon-aria-maxthon	<i class="iconfont icon-aria-sogou" style="font-size:2rem"></i>	 icon-aria-sogou<br>
<i class="iconfont icon-aria-uc" style="font-size:2rem"></i>	 icon-aria-uc	<i class="iconfont icon-aria-qqbrowser" style="font-size:2rem"></i>	 icon-aria-qqbrowser<br>
<i class="iconfont icon-aria-close" style="font-size:2rem"></i>	 icon-aria-close	<i class="iconfont icon-aria-mac" style="font-size:2rem"></i>	 icon-aria-mac<br>
<i class="iconfont icon-aria-twitter" style="font-size:2rem"></i>	 icon-aria-twitter	<i class="iconfont icon-aria-fedora" style="font-size:2rem"></i>	 icon-aria-fedora<br>
<i class="iconfont icon-aria-menu" style="font-size:2rem"></i>	 icon-aria-menu	<i class="iconfont icon-aria-write" style="font-size:2rem"></i>	 icon-aria-write<br>
<i class="iconfont icon-aria-like" style="font-size:2rem"></i>	 icon-aria-like	<i class="iconfont icon-aria-comment" style="font-size:2rem"></i>	 icon-aria-comment<br>
<i class="iconfont icon-aria-paperboat" style="font-size:2rem"></i>	 icon-aria-paperboat	<i class="iconfont icon-aria-category" style="font-size:2rem"></i>	 icon-aria-category<br>
<i class="iconfont icon-aria-linux" style="font-size:2rem"></i>	 icon-aria-linux	<i class="iconfont icon-aria-telegram" style="font-size:2rem"></i>	 icon-aria-telegram<br>
<i class="iconfont icon-aria-picture" style="font-size:2rem"></i>	 icon-aria-picture	<i class="iconfont icon-aria-guestbook" style="font-size:2rem"></i>	 icon-aria-guestbook<br>
<i class="iconfont icon-aria-reward" style="font-size:2rem"></i>	 icon-aria-reward	<i class="iconfont icon-aria-weibo" style="font-size:2rem"></i>	 icon-aria-weibo<br>
<i class="iconfont icon-aria-qrcode" style="font-size:2rem"></i>	 icon-aria-qrcode	<i class="iconfont icon-aria-home" style="font-size:2rem"></i>	 icon-aria-home<br>
<i class="iconfont icon-aria-username" style="font-size:2rem"></i>	 icon-aria-username	<i class="iconfont icon-aria-mail" style="font-size:2rem"></i>	 icon-aria-mail<br>
<i class="iconfont icon-aria-bilibili" style="font-size:2rem"></i>	 icon-aria-bilibili	<i class="iconfont icon-aria-copy" style="font-size:2rem"></i>	 icon-aria-copy<br>
<i class="iconfont icon-aria-checked" style="font-size:2rem"></i>	 icon-aria-checked <i class="iconfont icon-aria-rss" style="font-size:2rem"></i>	 icon-aria-rss<br>

*** 
## Aria.reloadAction()  
这是一个PJAX自定义重载代码的接口  

举例：
```javascript
Aria.reloadAction = function() {
    //...
    console.log("pjax completed!");
}
```