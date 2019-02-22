# 微信小程序的一些局限

小程序的局限，或者说坑，一大部分都是来源自小程序的自定义组件，强烈建议完整阅读一遍 [微信小程序官方文档](https://developers.weixin.qq.com/miniprogram/dev/index.html)，当中有非常多的细节点都值得注意，在此摘录部分。

## 选择器支持度

自定义组件中无法使用 id 选择器、标签选择器等，也需要注意组件和引用组件的页面中使用后代选择器（.a .b）在一些极端情况下会有非预期的表现。

## 全局样式

全局样式的最低基础库版本要求为 2.2.3，如果要使用全局样式，建议在后台设置最低版本，否则低版本用户访问时样式会错乱。

## 外部样式

在同一个节点上使用普通样式类和外部样式类时，两个类的优先级是未定义的，因此最好避免这种情况。