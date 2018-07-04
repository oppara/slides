# Capistrano について

---

## Capistrano とは？

デプロイを実行するツール

---

## デプロイとは

* ソースコードを本番環境などに設置
* ディレクトリ、ファイルなどにパーミッション設定
* キャッシュの削除 
* その他、業務ルールに則った手順諸々

---

## ツールを使わない場合

* タイムスタンプ信じられるなら、`rsync` やSFTPソフトの同期機能を使ったり...
* SFTPソフトを起動して、対象のサーバにログインして、ディレトリ移動して、更新されたファイルをアップロードとか...
* キャッシュ削除したり、パーミッション変更したり...

* それを複数サーバ... 😩

---

## ツールを使わない場合の弊害

* 手順書の更新ミス、記述ミス
* 手動で実行することによる作業ミス、手順ミス
* デプロイ手順の秘伝のタレ化、属人化

---

## ツールを使うことのメリット

* デプロイ手順のコード化 -> バージョン管理ができる -> 非属人化
* コマンド一発で実行可能 -> チャットボットで実行
* ロールバックできる！

---

## ツールを使うことのデメリット

* デプロイツールの作法を覚える必要がある
* うまく動作しない場合、調査にはまる（traceオプション付きで実行すれば大体解決するけど）
* デプロイツールを実装している言語力はあったほうがよい

---

## その他のデプロイツール

* [Fabric](https://get.fabric.io/) (Python)
* [Ansistrano](https://github.com/ansistrano) (Python) AnsibleのRole
* [Deployer](https://deployer.org/) (PHP)
* [Rocketeer](http://rocketeer.autopergamene.eu/) (PHP)
* [Cinnamon](https://github.com/kentaro/cinnamon) (Perl)


---

## なんで、Capistrano

* 先発なので情報が豊富（長いものには巻かれる主義）
* 当時、PHP製のデプロイツールはなかった
* 当時、Pythonは今ほど盛り上がってなく、  
    バージョン問題もあった
* 世の中の便利ツールはRubyとNodeで作られている
    * Vagrant, Fluentd, Serverspec, Awspec, Webpack, ESlint...
* Web関連の仕事をするなら、RubyとNodeを扱えたほうが夢が広がる
    今なら、GolangとPython

---

## 使い方

力尽きた😅

* 何十台ものサーバには向かない。（4,5台くらまで）。

本家読んだ方が早いと思うよ
https://capistranorb.com/