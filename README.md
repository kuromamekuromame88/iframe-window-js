# iframe-window.js

このライブラリは、様々なデバイスでも操作しやすいように、HTML内で操作可能なiframeウィンドウを作成するライブラリを作成することを目的としたリポジトリです。

## 特徴

### 1. ウィンドウ作成

ライブラリのスクリプトを読み込みます。

```html
<script src="https://kuromamekuromame88.github.io/iframe-window-js/src/IframeWindow.js"></script>
```

window作成は以下のように行います。

```javascript
const iw = new IframeWindow();
var window = iw.win("page", {
  pos:[10,10],
  size:[1040,300],
  content:{type:"web",con:"https://example.com"}
});
```



HTML文書を挿入するにはこのように行います。

```javascript
const iw = new IframeWindow();
var window = iw.win("page", {
  pos:[10,10],
  size:[1040,300],
  content:{type:"html",con:"<html><body><h1>これはHTML文書の埋め込みのサンプルです。</h1></body></html>"}
});
```

### 2. ウィンドウ操作

内部コンテンツの書き換え

```javascript
const iw = new IframeWindow();
var window = iw.win("page", {
  pos:[10,10],
  size:[1040,300],
  content:{type:"web",con:"https://example.com"}
});

//別のURLに書き換え
window.setContent({type:"web", con:"https://anothersite.com"});
```

ウィンドウの大きさの変更

```javascript
const iw = new IframeWindow();
var window = iw.win("page", {
  pos:[10,10],
  size:[1040,300],
  content:{type:"web",con:"https://example.com"}
});

//大きさ変更
window.setSize(400,300);//幅、高さ
```

ウィンドウの位置の変更(ページの左上を原点として)

```javascript
const iw = new IframeWindow();
var window = iw.win("page", {
  pos:[10,10],
  size:[1040,300],
  content:{type:"web",con:"https://example.com"}
});

//位置を変更
window.setPosition(500,500);//x座標、y座標
```

## 改造など

どんどん改造しちゃってください！
