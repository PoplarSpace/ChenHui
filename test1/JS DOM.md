# DOM

## HTML DOM（文档对象模型）

### 1.通过id查找HTML元素

查找id=“intro"

```javascript
var x = document.getElementById("intro");
```

### 2.通过标签查找

查找id="main"里的p元素

```javascript
var x =x document.getElementById("mian");
var y = x.getElementsByTagName("p");
```

### 3.通过类名查找

查找class="mian"

```javascript
var x = document.getElementsByClassName("intro");
```
## 改变HTML
### 改变输出了流
```javascript
document.write(Data());
#不可以在DOM加载完成后使用document.write().这会覆盖文档
```
### 改变HTML内容
```javascript
document.getElementById("p").innerHTML=新的HTML；
var element = document.getElementById("id");
element.inerHTML=新内容;
```
### 改变HTML属性
```javascript
document.getElementById(/*attributee*/)=新属性
```
## 改变CSS
### 改变HTML样式
```js
document.getElementById(/*id*/).style./*property*/=新样式;
```
## HTML DOM事件
### 对事件做出反应
```js
onclick=/*js语句*/;
```
### 事件属性
向button元素分配onclick事件
```js
<button onclick="displayData()">点这里<button>
/*点击按钮时displayData()事件被执行
```
### 使用HTML DOM分配事件
向button元素分配onclick事件
```js
document.getElementById("myBtn").onclick=function(){displayDate()};
```
### onload和onunload事件
onload和onunload事件会在用户进入或者离开网页时被触发。
### onchange事件
常常结合输入字段验证来使用
````js
<input type="taxt" id="fname" onchange="upperCase()">
```
当用户输入文字时，会调用upperCase()函数
### onmouseover和onmouseout事件
可用于鼠标移动到HTML元素上时触发的函数









