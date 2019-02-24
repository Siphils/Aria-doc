## 环境支持 
主题版本在`Typecho 1.1/17.10.30`*(纯净无插件)*及`PHP 7.2`环境下测试通过。  
`PHP >= 5.4`应该可以正常使用。
***
## 安装启用 
### 普通安装  
1. GitHub上点击Download下载主题压缩包  
2. 将压缩包解压并上传至`/usr/themes`文件夹  
3. **`Typecho-Theme-Aria-master`文件夹重命名为`Aria`**
4. 登陆Typecho后台，`控制台 -> 外观 -> 可以使用的外观`，选择`Aria`启用。  
  
### Git  
切至`usr/themes`目录  
```bash
git clone https://github.com/Siphils/Typecho-Theme-Aria.git && mv Typecho-Theme-Aria-master Aria
```  
登陆Typecho后台，`控制台 -> 外观 -> 可以使用的外观`，选择`Aria`启用。  

!> 目录名一定要修改为`Aria`，否则可能会出现一些未知的问题。

***
## 更新 

!> 更新过程中请勿在后台切换主题，否则设置信息会被清空  
只要不切换主题，设置信息会被保存在数据库内

更新步骤：
1. 下载最新版本主题
2. 删除`usr/themes/Aria`内所有文件 
3. 将新版主题所有文件移动到`usr/themes/Aria` 

!> 若出现样式问题或者JS问题，刷新下浏览器和CDN缓存（如果有的话）即可