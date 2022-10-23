# 第01回 ウェブ入門
- 目安提出日: 10月30日(日)
- [該当ページ](https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web)

## 必須項目
- [ファイルの扱い](https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web/Dealing_with_files)

## 推奨項目
- [HTMLの基本](https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web/HTML_basics)
- [CSSの基本](https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web/CSS_basics)
- [JavaScriptの基本](https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web/JavaScript_basics)
- [ウェブのしくみ](https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web/How_the_Web_works)

## 課題
> #### 提出について
> 課題の提出は初回講義で作ったリポジトリを通して行います。リポジトリ内に講義番号と同じ名前のフォルダー(今回は01)を作って、その中に作成したファイルを全て入れてください。ちなみに、初回講義で作ったファイルは全て消してもらって構いません。

以下のファイルは、項目「HTMLの基本」「CSSの基本」「JavaScriptの基本」を通して作成されたものです。これらのファイルを適切な位置に配置して、ブラウザで正しく表示されることを確認してください。

#### HTML
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>My test page</title>
    <link href="https://fonts.googleapis.com/css?family=Open+Sans" rel="stylesheet" type="text/css">
    <link href="styles/style.css" rel="stylesheet" type="text/css">
  </head>
  <body>
    <h1>Mozilla is cool</h1>
    <img src="images/firefox-icon.png" alt="The Firefox logo: a flaming fox surrounding the Earth.">

    <p>At Mozilla, we’re a global community of</p>

    <ul> <!-- changed to list in the tutorial -->
      <li>technologists</li>
      <li>thinkers</li>
      <li>builders</li>
    </ul>

    <p>working together to keep the Internet alive and accessible, so people worldwide can be informed contributors and creators of the Web. We believe this act of human collaboration across an open platform is essential to individual growth and our collective future.</p>

    <p>Read the <a href="https://www.mozilla.org/en-US/about/manifesto/">Mozilla Manifesto</a> to learn even more about the values and principles that guide the pursuit of our mission.</p>
  <button>Change user</button>
  <script src="scripts/main.js"></script>
  </body>
</html>
```

#### CSS
```css
html {
  font-size: 10px;
  font-family: 'Open Sans', sans-serif;
}


h1 {
  font-size: 60px;
  text-align: center;
}

p, li {
  font-size: 16px;
  line-height: 2;
  letter-spacing: 1px;
}


html {
  background-color: #00539F;
}

body {
  width: 600px;
  margin: 0 auto;
  background-color: #FF9500;
  padding: 0 20px 20px 20px;
  border: 5px solid black;
}

h1 {
  margin: 0;
  padding: 20px 0;
  color: #00539F;
  text-shadow: 3px 3px 1px black;
}

img {
  display: block;
  margin: 0 auto;
}
```

#### JavaScript
```js
// Image switcher code

let myImage = document.querySelector('img');

myImage.onclick = function() {
  let mySrc = myImage.getAttribute('src');
  if(mySrc === 'images/firefox-icon.png') {
    myImage.setAttribute ('src','images/firefox2.png');
  } else {
    myImage.setAttribute ('src','images/firefox-icon.png');
  }
}

// Personalized welcome message code

let myButton = document.querySelector('button');
let myHeading = document.querySelector('h1');

function setUserName() {
  let myName = prompt('Please enter your name.');
  if(!myName) {
    setUserName();
  } else {
    localStorage.setItem('name', myName);
    myHeading.innerHTML = 'Mozilla is cool, ' + myName;
  }
}

if(!localStorage.getItem('name')) {
  setUserName();
} else {
  let storedName = localStorage.getItem('name');
  myHeading.innerHTML = 'Mozilla is cool, ' + storedName;
}

myButton.onclick = function() {
  setUserName();
}
```

#### 画像
画像は右クリックで保存して使用してください。

![firefox-icon.png](https://raw.githubusercontent.com/mdn/beginner-html-site-scripted/gh-pages/images/firefox-icon.png)

![firefox2](https://raw.githubusercontent.com/mdn/beginner-html-site-scripted/gh-pages/images/firefox2.png)
