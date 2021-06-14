# PS
### 精灵图
#### 什么是精灵图
css精灵(CSS sprites),是一种网页图片应用处理技术。主要是指将网页中需要的零星的小图片集成到一个大的图片中
#### 引用原因
1.减少对浏览器的请求次数，避免网页的延迟
2.方便小图标的统一管理
#### 使用方法
1，引入精灵图
````css
.basic{
    background-image:url(ui.png);
    width:80px;
    height:80px;
    background-repeat:no-repeat;
    display:inline-block;
}
```
2.精确定位小图标坐标
```css
.sprite1{
    background-position:80px 0px
}

.sprite2{
    background-position:160px 160px
}
```
1.将小图标聚集在一起，获得一张精灵图的png
2.利用切图找到position位置
```html
<div class="box">
<ul>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
</ul>
</div>
```
js部分代码样例
```javascript
<script>
//获取所有li ，形成伪数组
var list = document.querySelectorAll('li')
// 2.使用for循环来设置每个li的背景图
for(var i = 0;i < list.length;i++){
 // 通过设置精灵图的y坐标来设置不同li的背景图
// 让索引号*44就是每个li的背景y坐标，index就是我们的y坐标
var index = i * 44;
// console.log(index);
list[i].style.backgroundPosition = '0 -' + index +'px';
}
</script>


```

一种是纯css设定，一种用上了js Dom.
