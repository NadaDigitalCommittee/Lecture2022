# 第03回 マルチメディアと埋め込み、HTML表
- 目安提出日: 11月27日(日)
- [該当ページ](https://developer.mozilla.org/ja/docs/Learn/HTML/Multimedia_and_embedding)
- [該当ページ](https://developer.mozilla.org/ja/docs/Learn/HTML/Tables)

## 必須項目
- [HTML の画像](https://developer.mozilla.org/ja/docs/Learn/HTML/Multimedia_and_embedding/Images_in_HTML)
- [動画と音声のコンテンツ](https://developer.mozilla.org/ja/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content)
- [object から iframe まで — その他の埋め込み技術](https://developer.mozilla.org/ja/docs/Learn/HTML/Multimedia_and_embedding/Other_embedding_technologies)
- [HTML の表の基本](https://developer.mozilla.org/ja/docs/Learn/HTML/Tables/Basics)
- [HTML 表の高度な機能とアクセシビリティ](https://developer.mozilla.org/ja/docs/Learn/HTML/Tables/Advanced)

## 推奨項目
- [ウェブへのベクターグラフィックの追加](https://developer.mozilla.org/ja/docs/Learn/HTML/Multimedia_and_embedding/Adding_vector_graphics_to_the_Web)
- [レスポンシブ画像](https://developer.mozilla.org/ja/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images)

## 課題
上の必須項目を読み、HTMLだけで下の画像のようなページを作ってください。

提出方法は前回と同じです。
![Sample Image](https://user-images.githubusercontent.com/83213179/199967874-868996f4-efb9-439d-bb58-10bd56497f55.png)

ページ内に使うファイルはこのリポジトリの03フォルダの中のを使用してください。各画像の説明等は適切につけておいてください。

また、ページ内にYoutubeの動画を埋め込む時に下のコードを利用してください

```html
<iframe width="806" height="453" src="https://www.youtube.com/embed/zEBw7lY2QXs" title="【ワークライフ・ジャパン】 過労死はなくなるのか　犠牲者遺族に話を聞く" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```

また、ページ内で次のCSSを読み込んでください
```css
th{
    width: 100px;
    background-color: rgb(209, 128, 128);
    color: white;
}
td{
    width: 100px;
    background-color: rgb(180, 224, 154);
}
```