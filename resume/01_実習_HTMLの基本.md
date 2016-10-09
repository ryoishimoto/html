# HTML5

##学習を始める前に
みなさんはこれまでバックエンドと呼ばれる領域を勉強してきたと思いますが、<br>
ここからは「フロントエンド」と呼ばれる領域を勉強していきます。<br>
<br>
例えば、Facebookの見た目の部分（投稿、フィード、友達一覧など）や、Pinterestの見た目などを作っているのはフロントエンドの役割です。

一般的にフロントエンドは以下の3つで構成されています。

- HTML（画面に文字を表示することが出来る）
- CSS（画面に色や形などのレイアウトを表現することが出来る）
- Javascript（画面に動きを付けたりすることが出来る）

他にも覚えることはあるのですが、今は、HTMLはこの3つで構成されていることを理解して下さい。

さて、バックエンドを学習したことがある方は、バックエンドから渡されたデータをWebブラウザ（Google Chrome, Firefox, Safari）などで表示したと思います。<br>

今から始めるHTMLとCSSとjavascriptを勉強すれば先ほど表示したものをもっとおしゃれにすることが出来ます！<br>
おしゃれというとすごくライトなものに聞こえるかもしれませんが、ユーザーさんに気持ちよく使ってもらえるようにレイアウトを変えたり、文字色を変えたりすることは非常に重要な事です！<br>
UI/UXという言葉を聞いたことがある方もいらっしゃるかもしれませんが、UI/UXはフロントエンジニアにも非常に密接な分野なので覚えておいて下さい！<br>
<br>
ユーザーさんに気持ちよく使っていただけるかどうかはフロントエンジニアの腕次第なので頑張りましょう！

##HTMLを勉強する前に
ここでは勉強に必要なツールをインストールします！<br>
以下の2つのソフトがPCに入っていない人はインストールして下さい！

- [SublimeText](http://www.sublimetext.com/3)<br>
  これはHTMLやCSS、Javascriptを編集していくソフトです。テキストを書くことが出来るソフトならなんでも大丈夫ですが、Webの言語を書きやすいエディタなのでこちらを使用しましょう！
- [GoogleChrome](https://support.google.com/chrome/answer/95346?hl=ja)<br>
  これはInternet Exploreやsafariと同じWebブラウザと呼ばれるものです。<br>
  GoogleChromeが一番デバッグ（コードが正しいか間違っているかの検証）をしやすいのでこちらを使用しましょう。

##HTMLとは

Hyper Text Markup Language（ハイパーテキスト・マークアップ・ランゲージ）の略で、

- 文章に意味づけをして、文書構造を作る、Webサイト用の文書を書くための言語。
- HTMLで作るものはあくまで「文書」で、 見出し`<h1>`や、段落`<p>`などのタグと呼ばれるものの組み合わせで作成されています。
- 現在、皆さんが目にするインターネット上で公開されてるWebページのほとんどは、HTMLで作成されています。
- HTMLはそれほど難しい言語ではありません。簡単なWebページなら、数種類のタグで作成することが可能。
- HTMLの記述は大文字でも小文字でも認識してくれますが、できれば小文字をおすすめします。参考：[HTMLタグは大文字と小文字の区別はしません](http://homepage-market.com/basic07.html)

<br>

##HTMLの記述のひな形
下に書いてあるのが一番基本的なhtmlの構成です。

```html
<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="utf-8">
    <title></title>
  </head>
  <body>
    <h1>HTMLを学習しよう！</h1>
    <p>HTMLはタグで囲むのが基本です</p>
  </body>
</html>
```

<br>
上記のコードは一つ一つに意味があって、それを説明したものを下に書きました。

```html
<!DOCTYPE html> <!--DOCTYPE宣言,HTMLのバージョンを宣言するためのもの-->
<html lang="ja"><!--言語の指定-->
  <head><!--ページに表示されない情報(Webページの設定に関する情報)-->
    <meta charset="utf-8">
    <title></title><!--ブラウザのタブ上のページのタイトルを指定-->
  </head>
  <body><!--ページに実際に表示される内容-->
    <h1>HTMLを学習しよう！</h1>
    <p>HTMLはタグで囲むのが基本です</p>
  </body>
</html>
```

```html
//index.html
<!DOCTYPE html> <!--DOCTYPE宣言をするとこれがHTMLだよーと認識してくれる-->
<html lang="ja"><!--このサイトはどの言語向けに書かれているかを指定する、langを変更するとフォントが変わったりする-->
  <head><!-- htmlに関する情報を入れていく -->
    <meta charset="utf-8">
    <title></title><!--ブラウザのタブ上のページのタイトルを指定-->
  </head>
  <body><!--bodyの中に書いたものがwebサイトの中に表示される-->
    <h1>HTMLを学習しよう！</h1>
    <p>HTMLはタグで囲むのが基本です</p>
  </body>
</html>
```

これは決まり文句のようなものなので一言一句覚えておく必要は全くありません。<br>
<br>
なので、さらっと各タグが何を意味しているのかだけを理解して下さい。<br>

###html決まり文句サラッと復習
.htmlのファイルを用意（例:index.html）します。<br>
<br>
続いて**<!DOCTYPE html>**でHTMLの宣言をします。

```html
<!DOCTYPE html>
```

<br>
次に**htmlタグ**を使用してhtmlの全体の情報を入れていく部分を作ります

```html
<!DOCTYPE html>
<html lang="ja" >
  ココの中にコードを書いていく
</html>
```
<br>
**headタグ**を使用して、このページに必要な情報を追加します。<br>
※ここではmeta charsetを使用して文字コード、titleタグを使用してwebページのタイトルを入れました。

```html
<!DOCTYPE html>
<html lang="ja">
  <!-- headタグの中にhtmlの情報を書いていく -->
  <head>
    <meta charset="utf-8">
    <title>Webサイトのタイトルだよ</title>
    <!-- facebookでシェアした時の画像とか、ファビコンとか、css, javascriptも記述できる -->
  </head>
</html>
```

<br>

次に、**bodyタグ**の中に実際にユーザーさんに見える部分を追加しました。

```html
<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="utf-8">
    <title>webサイトのタイトルだよ</title>
    <!-- facebookでシェアした時の画像とか、ファビコンとか、css, javascriptも記述できる -->
  </head>
  <body>
    ここに見える部分を書いていく
  </body>
</html>
```

これで雛形は全て完成です！<br>
どのWebサイトを見ても、DOCTYPEの宣言はしてありますし、htmlタグ、headタグ、bodyタグは必ず存在しています！<br>
<br>
開発するときは雛形をカスタマイズして作成していきます。<br>

```
読み込むCSSとかJavascriptを増やしたいなー → headタグの中に記述
ブラウザに表示される文字を追加したり、画像を表示したりしたいなー → bodyタグの中に記述
```

という感じですね！
<br>
<br>

また、雛形のコードからわかるように、HTMLファイルはタグで囲んで記述していくのが基本になります！<br>
少しだけ、終了タグが必要ないタグも存在しますが、基本的にはタグで囲んで記述していきます。<br><br>
先ほどの図を閉じタグで表すと以下のようになります。

![html_入れ子構造.jpg](https://qiita-image-store.s3.amazonaws.com/0/67977/5bdc8848-8109-dddc-c30f-44f6bbc9b566.jpeg "html_入れ子構造.jpg")

<開始タグ>～</終了タグ>が基本の書き方です。
タグは入れ子の構造になることにご注目ください。複雑な文書になっても、基本の構造は変わりません。

<br>

簡単な例で言うと以下のようになります。

```html
<開始タグA>
  <開始タグB>ここに内容</終了タグB>
  <開始タグC>
    <開始タグD>ここに内容</終了タグD>
  </終了タグC>
</終了タグA>
```

<br>

一方、複雑な例で言うと以下の様になります。

```html
<開始タグA>
  <開始タグB>ここに内容</終了タグB>
  <開始タグC>
    <開始タグD>
      <開始タグE><開始タグK>メニューへのリンク</開始タグK></開始タグE>
      <開始タグF><開始タグL>メニューへのリンク</開始タグL></開始タグF>
      <開始タグG><開始タグM>メニューへのリンク</開始タグM></開始タグG>
      <開始タグH><開始タグN>メニューへのリンク</開始タグN></開始タグH>
      <開始タグI><開始タグO>メニューへのリンク</開始タグO></開始タグI>
      <開始タグJ><開始タグP>メニューへのリンク</開始タグP></開始タグJ>
    </終了タグD>
  </終了タグC>
</終了タグA>
```

また、このこういう構造のことを入れ子構造といい、自分の中に入っている要素のことを「子要素」、自分を囲っている要素を「親要素」といいます。

また、開始タグと閉じタグは対応していなければなりません。
例えば、以下のコードの場合

```html
<開始タグA>
  <開始タグB></終了タグA>
</終了タグB>
```

**開始タグA**の中に**開始タグB**が存在していますが、**開始タグB**の終了タグが**終了タグA**の前に来ています。<br>
このようなタグの閉じ方はNGです！<br>
図で言うと以下のとおりです。

![Untitled 16.55.24.png](https://qiita-image-store.s3.amazonaws.com/0/67977/777236fd-e688-8e00-ef5a-2e885c53a65d.png "Untitled 16.55.24.png")　　　　　　　　　![Untitled 16.58.44.png](https://qiita-image-store.s3.amazonaws.com/0/67977/2c11c4c6-67ff-e4ce-5397-1693f1b51347.png "Untitled 16.58.44.png")

できるだけ注意して書くようにしましょう！

<br>
<br>

##htmlを書くときに使う基礎知識
###空要素
* HTMLの中には、`<br>`（改行）や`<img>`（画像の表示）のように、要素内容を持たない空要素があります。 <br>このような空要素には終了タグはありません。

###コメントアウト
<!-- -->で囲まれた部分はブラウザには表示されません

![スクリーンショット 2016-02-23 12.35.27.png](https://qiita-image-store.s3.amazonaws.com/0/67977/daa81532-084e-8356-abf3-ca8419706c71.png "スクリーンショット 2016-02-23 12.35.27.png")

###属性
- HTMLでは、それぞれタグの種類ごとに指定できる属性の名称とその値が定義されています。

- 例）`<a href="(url)">〜</a>`
  - a = anchor（アンカー）の略
  - href属性は、ハイパーリンク先のURLを指定する際に使用
  - （ダメな例）`<a href="(◯◯.jpg)"></a>`


<br>


##実際にHTMLを書いて保存してみよう！

1. SublimeTextを開く
2. 右下のPlain TextをクリックしHTMLを選択（この時、Plain Text右のTab Sizeを4にしておくと良い）
3. ナビゲーションバーのFileから「Save」又は「command + s」(WinはCtrl + s)
4. ファイルの拡張子は「.html」(デスクトップ(保存場所はどこでもOK)に、新しいフォルダを作成しそちらに保存)

```html
<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="utf-8">
    <title>ELITES</title>
  </head>
  <body>
    <h1>HTMLを学習しよう！</h1>
    <p>HTMLはタグで囲むのが基本です</p>
  </body>
</html>
```

<img src="./others/images/html/before.png" width="100%" style="border:solid 1px #ccc;"><br>
<br>

少し改良してみましょう！

```html
<!DOCTYPE html>
<html lang="ja">
  <head>
    <meta charset="utf-8">
    <title>ELITES</title>
  </head>
  <body>
    <h1>HTML/CSSを学習しよう</h1>
    <h5>ELITES</h5>
    <p>HTML/CSSを使用すると、１からホームページの作成ができます。</p>
  </body>
</html>
```

<br>
以下の画像のように表示されれば正解です！<br>

<img src="./others/images/html/after.png" width="100%" style="border:solid 1px #ccc;"><br>

##参考
[htmlの復習とHTML5のお勉強](http://qiita.com/piotzkhider/items/62d2a0975dbdd0ef78b2)
