# web-editor
17行实现一个web editor

#### Html
```
<div>                                  // 左边区域
  <textarea id="textarea"></textarea>  // 放入一个textarea
</div>
<div id="right"></div>                 // 右边区域
```

#### CSS
```
html, body {height: 100%; padding: 0; margin: 0;}
#left {width: 50%; height: 100%; float: left;}
#right {width: 50%; background: #f5f5f5; height: 100%; float: left; overflow: hidden;}
#textarea {width: 100%; height: 100%; background: #fff;}
```

#### JS
```
window.onload = function() {
  let rightContainer = document.getElementById("right");
  let textarea = document.getElementById("textarea");
  let right = document.getElementById("right");
  textarea.oninput = function() {
    let input = this.value;   // 关键代码，获取textarea的输入内容
    right.innerHTML = input   // 关键代码，获取到的内容放入右边区域
  }
}
```
嗒哒～～ 好啦 ：）