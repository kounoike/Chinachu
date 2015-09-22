Chinachu [![Build Status](https://secure.travis-ci.org/kanreisa/Chinachu.png)](http://travis-ci.org/kanreisa/Chinachu) [![tip for next commit](http://tip4commit.com/projects/689.svg)](http://tip4commit.com/projects/689)
========

Visit the Chinachu website for more information: <https://chinachu.moe/>

## このブランチについて

うちで使ってるブランチです。元はdevel-betaですので、Node.js-4.0.0ベースになっています。

そこに追加した機能として、

* 番組検索、ルール判定などでUnicode正規化をかけて判定する
* 番組検索をルール判定と同じロジック・UIにする
* あちこちにフックコマンドを導入（これはdevel-betaに取り込まれてます）

があります。このうち、最初のは簡単に言うと、全角・半角を区別せずに検索できる機能です。
2番目は今まで番組検索とルール判定で別々のロジックになっていたため、スケジューラを実行して予約登録をするまでルールの吟味ができなかったものを、検索でも同じロジックにすることで、ルールを書きやすくする機能です。
3番目は[ブログ記事](http://www.typemiss.net/2015/09/chinachu-jq.html) 参照。予約がルールで追加されたときとかにメールしたりできる機能です。

あとはBugFixとして、「（ほげほげ)」みたいなタイトル（かぎ括弧の中にある丸括弧が全角と半角がごっちゃになってる）があったときにエラーが出てしまっていたのを解決できるようになっています。
こんなタイトルがたまーに入ってくるみたいなんで、念のために直しておきました。
