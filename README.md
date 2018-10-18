# typecho-plugin-pagetolinks
一个 typecho 插件， 将自定义页面转化成友情链接。


原插件可从官方插件仓库找到<https://github.com/typecho/plugins>
我做了少许修改，支持了使用 markdown 语法书写的页面内容。同时插件需要激活后使用。
算是对原插件的更新版本吧，原插件信息没有做修改，所以使用该插件会覆盖原有插件。

## 使用说明

1. 上传 `PageToLinks.php` 文件到 插件目录
2. 后台插件管理启用
3. 创建一个别名为 `links` 的自定义页面
4. 在模版文件的相应位置添加调用代码（具体代码参考下面部分）


###  模版添加代码例子


```
<?php if(Typecho_Plugin::exists('PageToLinks')): ?>
<section class="widget">
<?php PageToLinks::output(); ?>
</section>
<?php endif; ?>
```

