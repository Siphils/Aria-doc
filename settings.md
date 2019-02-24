
?> 本篇会详细解读主题后台的设置项目

## 站点头像  
填入一个图片（推荐正方形）地址，需要带上 `http(s)://`

?> 留空会根据博主邮箱调用Gravatar头像。  

> 显示位置
>1. 导航栏站点名称旁    
>2. 竖直导航栏顶部  
***  
## 默认文章缩略图  
**这个缩略图对文章和页面都有效**  
按行填入图片的地址，并带上`http(s)://`前缀，图片会随机显示。  

?> 调用顺序的优先级：`文章/页面缩略图Url字段` > `后台设置->默认文章缩略图url` > `assets/img/thumbnail.jpg` 

> 显示位置  
>1. 首页文章卡片内   
>2. 文章页面顶部(头部图片)  
>3. 文章底部的上一篇/下一篇内  
***  
## 首页背景图片  
按行填入图片的地址，并带上`http(s)://`前缀，图片会随机显示。  

?> 这里的图片会显示在`首页`、`搜索结果页面`、`分类`等页面  

***  
## OwO  
填入`OwO.json`的文件地址，带上`http(s)://`前缀  
***  
## 评论框placeholder  
显示在评论框内  
***  
## 统计代码  
填入服务商内获取的统计代码  

!> 需要注意的是，如果你开启了`pjax`，那么最好使用`Google`或百度的分析统计代码。  
因为`pjax`会导致统计代码统计不准确，需要对统计代码进行重载，而目前我也只内置了这两个统计的重载代码。  

***  
## 顶部自定义内容  
这里可以填需要额外链接的`css`、`html`之类的内容，会插入到`</head>`标签之前。
***  
## 底部自定义内容  
可以填写`html`的内容，例如服务器提供商、CDN提供商等。  
会插入到底部版权的上面。
***  
## 自定义JS  
插入到`main.min.js`文件之后，可以加入你自己的JS代码，例如[重载代码](?advanced#ariareloadaction)等等。 

!> 只填写代码，不需要`<script></script>`标签

***  
## 底部链接组件  
配置方式是通过`json`格式的字符串，可以留空  

| 参数 | 内容 | 是否必需 | 类型 |
| ------ | ------ | ------ | ------ |
| text | 链接的文字 | 是 | string |
| href | 链接地址 | 否 | string |
| target | 参考[`html`](http://www.w3school.com.cn/tags/att_a_target.asp)语法 | 否 | string |  

!> 注意所有`string`类型的参数必须要用英文引号包裹

单个  
```json
{"text":"Siphils","href":"https: //eriri.ink","target":"_blank"}
```  
多个  
```json
{"text":"Siphils","href":"https: //eriri.ink","target":"_blank"},
{"text":"Siphils","href":"https: //eriri.ink","target":"_blank"}
```  

!> 注意末尾的逗号，最后一项不需要逗号。

***  
## Copyright年份  
比如`2017-2018`,`2018`。  
会显示在网站底部版权处。  
***  
## Gravatar头像源  
填入gravatar镜像地址，填写类似格式为  
```html
http(s)://domain/avatar/
```
留空默认为 
```html
https://cn.gravatar.com/avatar/`
```
***  
## 导航栏配置  
各项参数如下表  

| 参数 | 内容 | 是否必需 | 类型 | 
| ------ | ------ | ------ | ------ |
| text | 链接的文字 | 是 | string |
| [slug](settings?id=slug参数) | 页面缩略名 | 否 | string |
| href | 链接地址 | 否 | string |
| target | 参考[`html`](http://www.w3school.com.cn/tags/att_a_target.asp)语法 | 否 | string |
| icon | [图标](/advanced?id=图标) | 否 | string |
| sub | 子菜单 | 否 | array |

!> 子菜单内各项配置与上面参数相同*(除`sub`外)*

### 配置举例  
 添加一个`首页`的标签：
```json
{
    "text": "首页",
    "href": "https://eriri.ink",
    "icon": "iconfont icon-aria-home"
}
```
再添加一个`归档`的标签：
```json  
{
    "text": "首页",
    "href": "https://eriri.ink",
    "icon": "iconfont icon-aria-home"
},
{
    "text": "归档",
    "href": "https://eriri.ink/archives.html",
    "icon": "icon-aria-archives"
}
```  
在归档下添加一个`日常`的子菜单：
```json
{
    "text": "首页",
    "href": "https://eriri.ink",
    "icon": "iconfont icon-aria-home"
},
{
    "text": "归档",
    "href": "https://eriri.ink/archives.html",
    "icon": "iconfont icon-aria-archives",
    "sub" : [
        {
            "text":"日常",
            "href":"https://eriri.ink/category/daily/",
            "icon": "iconfont icon-aria-book"
        }
    ]
}
```  
再添加一个`代码`的子菜单：  
```json
{
    "text": "首页",
    "href": "https://eriri.ink",
    "icon": "iconfont icon-aria-home"
},
{
    "text": "归档",
    "href": "https://eriri.ink/archives.html",
    "icon": "iconfont icon-aria-archives",
    "sub" : [
        {
            "text":"日常",
            "href":"https://eriri.ink/category/daily/",
            "icon": "iconfont icon-aria-book"
        },
        {
            "text":"代码",
            "href":"https://eriri.ink/category/zturn/",
            "icon": "iconfont icon-aria-code"
        }
    ]
}
```  
!> 子菜单的项目也是可以设置`target`属性的  
并且每个父级菜单都可以设置子菜单，目前仅支持最多二级菜单
  
### `slug`参数  
这个参数比较特殊，仅支持在typecho后台创建的页面并设置了`slug`的页面。  

?> 页面的`slug`就是在创建页面时，填写页面链接的那串字符。  

!> 填入`slug`后，`text`、`href`参数不会被解析，而是会根据`slug`查询数据库后输出对应的页面的链接和标题。  

!> 输出的顺序会按照配置信息的填写顺序

例如：  
```json
{
  "slug":"archives",
  "icon":"iconfont icon-aria-archives"
}
```  
这时就会查找对应的slug并输出对应的页面名称和链接，此时`text`和`href`参数无效，其他参数仍有效。  
***  
## 打赏功能配置  
每行按照`键值对`的方式填写即可，例如：
```json
"Alipay":"https://cdn.siphils.com/reward/alipay.jpg",
"Wechat":"https://cdn.siphils.com/reward/wechat.jpg"
```  

!> 配置好后会在*文章/页面*末尾显示打赏按钮，若留空则按钮不输出

***  
## 自定义「一言」接口地址  
?> 句子会显示在页面底部  

填入接口地址，**注意接口需要是只返回一条句子的，比如我使用的默认的hitokoto.cn的接口：
```url
https://v1.hitokoto.cn/?c=a&encode=text
```  
!> [开关设置-一言](settings?id=一言)内可以选择开启或关闭显示，留空使用默认接口地址。  
如果不知道什么意思留空即可。 
***  
## MathJax配置信息  
在此输入MathJax配置信息，不需要script标签，只输入JS代码。
例如：
```javascript
MathJax.Hub.Config({
    tex2jax: {inlineMath: [['$','$'], ['\\(','\\)']]}
})
```

!> 此项设置在[开关设置](settings?id=开关设置)中`启用MathJax`项目启用后才会显示

***  
## 开关设置   
### PJAX  
[什么是PJAX?](https://github.com/defunkt/jquery-pjax#pjax--pushstate--ajax) 
PJAX重载接口见[Aria.reloadAction()](advanced?id=ariareloadaction)

!> 启用后会强制关闭`评论反垃圾保护`  

*** 
### AJAX评论
[什么是AJAX?](https://en.wikipedia.org/wiki/Ajax_%28programming%29)

!> 此功能目前尚不太完善  

***
### Fancybox  
[什么是fancybox?](https://fancyapps.com/fancybox/3/)  
开启图片灯箱效果，会自动解析文章/页面/评论区内的图片。并且一篇文章或页面内的图片会自动解析为一个相册集。

?> 如果*文章/页面*内某张图片不想要解析为灯箱，则可以如此书写：
```html
!!!
<img src="/path/to/img" no-fancybox>
!!!
```
***  
### Lazyload  
[什么是lazyload?](https://appelsiini.net/projects/lazyload/)  
图片懒加载功能开启后，所有的图片会自动解析为懒加载。

?> 如果某张图片不想要解析为懒加载，则可以如此书写：
```html
<img src="/path/to/img" no-lazyload>
```
*** 
### 评论邮件回复提醒按钮  
开启后会在评论框右下角增加一个**不接收回复邮件通知**的按钮 

!> 若想此按钮有效，你必须安装[CommentToMail](https://9sb.org/58)插件 *(文章中最后一个插件)*

***
### MathJax  
[什么是MathJax?](https://www.mathjax.org/)  
`v1.9.0`以上版本已经内置了MathJax  

!> 此开关启用后，需要在[MathJax配置信息](settings?id=mathjax配置信息)设置内填入配置信息

***
### 文章链接二维码  
在*文章/页面*末会输出一个本文链接的二维码
***
### 评论UserAgent  
显示评论者的操作系统和浏览器信息
*** 
### 一言
显示在网站底部


