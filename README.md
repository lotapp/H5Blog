## 1.不用模版的原因

本来是准备直接使用模版的，但是用过模版的同志都知道模版有3个特别麻烦的地方：
1. 样式`杂乱`而`重复`
    - 语义化标签基本上不用或者瞎用
    - 很多样式都通用还是写了一遍又一遍
2. 不太考虑`并发`请求的情况，小图片一堆又一堆
    - PS：有经验的前端会使用雪碧图，经常和程序员打交道的同志会尽量不使用图片（iconfont基本够用）
3. 经常出现首个|尾部效果和列表不一样的情况
    - PS：这样就需要多一层程序判断（能前端解决的尽力不使用后端判断）
4. 最后就是 ~ PC端习惯宽屏了，所以就以宽屏为基准了

正巧之前业余之际弄了几个简单小程序，然后把几年前写的H5文章回顾了下，接着W3C逛了下，把个H5系列的文章草稿也写掉了，想着：要不抽空仿一个？

于是就有了这个博客了。。。（更新ing）
> PS：博客主要仿的就是杨青姐的（记得大学那会的博客也是仿的她的）

## 2.兼容性说明

**由于个人能力限制，目前只支持>=IE9的IE浏览器**
> PS：微软爸爸早就放弃IE了，也就没必要全支持了（企业网站建议继续支持）

## 3.使用的插件

### 3.1.小说明：
1. 插件都是不依赖JQ的，可单独使用的
2. 把插件从页面剥离也是不影响页面的
    - PS：插件的目的就是为了美化，使用异步加载+CDN（成功就漂亮点，失败也无所谓）

### 3.2.粒子背景JS插件
<https://github.com/lotapp/canvas-nest.js>

使用方式：
```js
<script type="text/javascript" color="22,192,255" opacity="1" zIndex="-2" count="99" src="//cdn.staticfile.org/canvas-nest.js/1.0.1/canvas-nest.min.js"></script>
```

### 3.3.页面滚动插件（不依赖JQ）
<https://github.com/scrollreveal/scrollreveal>

使用方式：
```js
<script src="https://cdn.staticfile.org/scrollReveal.js/4.0.5/scrollreveal.min.js"></script>
<script>
window.onload = function () {
    // 加载成功就进行设置
    if (window.ScrollReveal) {
    // 实例化，根据默认配置改即可：https://scrollrevealjs.org/api/defaults.html
    window.ScrollReveal({
        origin: "right", // 从右边出现
        duration: "1500", // 持续时间1.5s
        reset: true // 循环
    }).reveal(".bloglist li,#header,#banner,.bg_white");
    // 经测试，支持CSS选择器
    }
}
</script>
```

## 4.欢迎提交对应版本的动态实现

欢迎反馈bug和提交对应版本的动态实现