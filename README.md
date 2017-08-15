# web-editor
17行实现一个web editor

#### Html
```
<div id="left">
  <textarea id="textarea"></textarea>
</div>
<div id="right"></div>
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
    let input = this.value;
    right.innerHTML = input
  }
}
```
嗒哒～～ 好啦 ：）