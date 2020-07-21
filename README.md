# 介绍
Xiuno BBS 4.0 是一款轻论坛产品。
本版本在消逝的官方git版本基础上，修复了php7.4安装时的兼容问题；采用utf8mb4，支持emoj；，jQuery更新到 3.5.1；bootstrap更新到4.5.0。移除部分插件，更新默认主题。

## 我做了些什么

### 修复
- 修复php7.4兼容问题
- 修复无法卸载插件bug
### 更新
- 💄默认主题更新
- 💥采用**utf8mb4**，支持emoji
- jQuery更新到 3.5.1
- 💥bootstrap更新到4.5.0
- 部分css、js改用min版，提高页面速度
- 移除IE hock
- 移除插件中心链接
- UMEditor 百度编辑器更新简约主题，后续可能替换成大白编辑器
### 移除部分原始插件
* 在线手册（xn_manual），不能用，删掉
* 返回顶部（z_top），后续会集成到主题中
* Xiuno BBS 测试插件 (xn_test)，无用插件
* 屏幕阅读 ( xn_screen_reader)
* 幸运踩楼 (xn_lucky_post)，很不常用的功能，且影响美观
* 版块三级分类 (xn_forum_level_3)
* 我的第一个 Xiuno BBS 插件 (my_hello)
* 移除官方自带三款主题(xn_theme_red、 xn_theme_paopao、xn_theme_dark)，后续会添加简约风、acg主题、绿色小清新

## 截屏
![image](https://raw.githubusercontent.com/jiix/xiunobbs/master/screenshot.png)

## 使用
使用请下载发布版，集成较少插件。数据库请采用**utf8mb4**，安装完成后，请删除install目录。
插件和主题，直接上传到**plugin**目录中，后台插件中心开启。

### 伪静态
打开`/conf/conf.php`文件，把`  'url_rewrite_on' => 0,`改为`  'url_rewrite_on' => 1,`
#### Apache伪静态
```
<IfModule mod_rewrite.c>
RewriteEngine on

# Apache 2.4
RewriteCond %{REQUEST_FILENAME} !-d 
RewriteCond %{REQUEST_FILENAME} !-f 
RewriteRule ^(.*?)([^/]*)$ $1index.php?$2 [QSA,PT,L]

# Apache other
#RewriteRule ^(.*?)([^/]*)\.htm(.*)$ $1/index.php?$2.htm$3 [L]
</IfModule>
```
#### nginx伪静态
```
location ~* \.(htm)$ {
    rewrite "^(.*)/(.+?).htm(.*?)$"$1/index.php?$2.htm$3last;
}
```

## 下一步
增加插件仓库，添加常用插件，重启社区计划。

## 贡献者
创始人[axiuno](http://bbs.xiuno.com/)
Thanks For: [cnteacher@discuz](http://www.discuz.net/) [Discuz! Team](http://www.discuz.net/) [Artery](http://artery.cn/) [剑心@wooyun](http://www.wooyun.org/) [右键森林](http://bbs.xiuno.com/) [吴兆焕](http://bbs.xiuno.com/) [杨永全](http://www.zd.hk/) [郑城](http://www.huux.cc/) [大象](http://www.baiup.com/)

## Enjoy!
