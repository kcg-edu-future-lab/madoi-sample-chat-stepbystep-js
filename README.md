# madoi-sample-chat-stepbystep-js

未来環境ラボで開発しているオブジェクト共有サービス madoi を使ってチャットを作成するサンプルです。チャットメッセージをログに追加するサンプル([index_01.html](https://github.com/kcg-edu-future-lab/madoi-sample-chat-stepbystep-js/blob/master/index_01.html))から始まり，通信機能を実装して最終的にmadoiのオブジェクト共有機能を使うところまで段階的に実装しています。

まずはこのリポジトリをcloneしてください。
```
git clone https://github.com/kcg-edu-future-lab/madoi-sample-chat-stepbystep-js
```

次にindex.htmlがあるディレクトリでHTTPサーバを起動し，ブラウザで表示してください。例えばpython3がインストールされていれば，以下のコマンドでサーバを起動できます。Rubyや他の言語でもHTTPサーバを起動できるものはありますので，環境に応じた方法で起動してください。
```
python3 -m http.server
```

index.htmlには各段階の実装へのリンクが含まれています。ブラウザに表示されるページの見た目は全て同じで，共有機能の実現方法が異なります。

1. [index_01.html](https://github.com/kcg-edu-future-lab/madoi-sample-chat-stepbystep-js/blob/master/index_01.html) - メッセージをログ領域に追加するだけのサンプルです。ネットワーク機能は使用していません。
2. [index_02.html](https://github.com/kcg-edu-future-lab/madoi-sample-chat-stepbystep-js/blob/master/index_02.html) - madoiのメッセージ配信機能を使って共有を実現するサンプルです。メッセージの送信や受信処理を独自に記述しています。
3. [index_02_2.html](https://github.com/kcg-edu-future-lab/madoi-sample-chat-stepbystep-js/blob/master/index_02_2.html) - index_02とindex_03の中間。本来madoiが自動的に作成するプロキシの作成やオリジナルの関数の退避を自前で行っています。
4. [index_03.html](https://github.com/kcg-edu-future-lab/madoi-sample-chat-stepbystep-js/blob/master/index_03.html) - madoiの関数共有機能を使って共有を実現するサンプルです。index_02.htmlで記述していた送受信処理が省かれています。
5. [index_04.html](https://github.com/kcg-edu-future-lab/madoi-sample-chat-stepbystep-js/blob/master/index_04.html) - madoiのオブジェクト共有機能を使って共有を実現するサンプルです。チャット関連の処理がクラス化され，インスタンスとメソッドをmadoiに登録することで共有機能が実現されています。
5. [index_05.html](https://github.com/kcg-edu-future-lab/madoi-sample-chat-stepbystep-js/blob/master/index_05.html) - madoiのオブジェクト共有機能を使い，Chatオブジェクトの状態保存/再現を行うサンプルです。
