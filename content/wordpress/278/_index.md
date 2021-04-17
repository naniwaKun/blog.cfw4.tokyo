---
title: "PocketMine-MPでPEのバニラ鯖 (v0.13.2) を立てる。"
date: 2016-02-09T12:26:37+00:00
description: "既出の話題かもしれないが、PEのクライアントがv0.13.2にバージョンアップしてから「サーバーが期限切れです」となってしまう。公式（と呼んでいいのかわからないけれど）のアナウンス通りサーバーを立ててもv0.13.1まで ..."
draft: false
---

既出の話題かもしれないが、PEのクライアントがv0.13.2にバージョンアップしてから「サーバーが期限切れです」となってしまう。[公式（と呼んでいいのかわからないけれど）](http://www.pocketmine.net/)のアナウンス通りサーバーを立ててもv0.13.1までしか対応していないようなので、[PocketMine-MPのgithub](https://github.com/PocketMine/PocketMine-MP)から最新のソースを取ってきてインストールしたらいけるんじゃないかと思って試してみました。advanceでのインストールより不安定だと思ってください。

**お約束ですが、この記事の文責はなにわにありますが、仮にこの記事通りにしたがってコマンドを実行し、結果なにが起きても僕は一切の責任を取るつもりはありません。**

インストール方法は英文で[ここ](http://pocketmine-mp.readthedocs.org/en/latest/installation.html)にあります。多分日本語ページがないからあんまり知られてないのかもしれない。詳しい各環境のインストール方法はリンク先をみてもらうこととして、linuxサーバーにインストールするなら以下のコマンドを実行してください。

`git clone https://github.com/PocketMine/PocketMine-MP.git
cd PocketMine-MP/ `

PHPのバイナリをインストールしてくだい。インストール出来ない人は期限切れになったPocketMine-MPのディレクトリの中のbinディレクトリをコピーしてください。それからいつもどおり立ち上げればいいはず。  
`cp -r /期限切れのパス/bin .
./start.sh `

うまく行けば以下のログが吐き出されるはず。

<figure id="attachment_279" aria-describedby="caption-attachment-279" style="width: 899px" class="wp-caption aligncenter"><a href="http://cfw4.dip.jp/wordpress/wp-content/uploads/2016/02/2.png" rel="attachment wp-att-279"><img loading="lazy" class="wp-image-279 size-full" src="http://cfw4.dip.jp/wordpress/wp-content/uploads/2016/02/2.png" alt="2" width="909" height="343"></a><figcaption id="caption-attachment-279" class="wp-caption-text">こんな感じのログが出ればおっけ～。</figcaption></figure>

というわけで、しばらく「サーバーの期限切れです」で困っている人は試してみてください。

The post [PocketMine-MPでPEのバニラ鯖 (v0.13.2) を立てる。](https://blog.cfw4.tokyo/wordpress/278/) first appeared on [あんなことやこんなこと](https://blog.cfw4.tokyo).