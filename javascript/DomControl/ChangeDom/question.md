## DOMの入れ替え
以下のように、1つの要素を内包したDOMがある。
```html
<div id="parent">
  <div id="primal_child"></div>
</div>
```
いま、`id="primal_child"` が付与された要素を `id="alternative_child"` が指定されたものに
入れ替えるための操作を行いたい。<br>
このとき、意図した挙動を示すのは次のうちどれか。

1.
```javascript
let child = document.getElementById('primal_child');
const alternative = document.createElement("div");
alternative.id = 'alternative_child';
child = alternative;
```

2.
```javascript
const parent = document.getElementById('parent');
let child = document.getElementById('primal_child');
const alternative = document.createElement("div");
alternative.id = 'alternative_child';
parent.removeChild(child);
parent.appendChild(alternative);
```

3.
1, 2のどちらも意図した挙動を示す
