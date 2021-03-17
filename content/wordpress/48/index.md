---
title: "Webで使えるターミナルを導入してみた！"
date: 2014-07-02T17:10:42+00:00
description: "大学から自分のサーバーに接続しよう！うききー！ あれ、接続できない！プロキシか！ うんぬー。と思っていたら、webベースでターミナルぐらいあるんじゃないのか？と思い、ググってみたら、、、 ありましたよ。 しかも、若干２７ ..."
draft: false
---

大学から自分のサーバーに接続しよう！うききー！  
あれ、接続できない！プロキシか！  
うんぬー。と思っていたら、webベースでターミナルぐらいあるんじゃないのか？と思い、ググってみたら、、、  
ありましたよ。

しかも、若干２７歳のFlorian Mounierさんが単独で開発したっぽい。  
名前は、Butterflyってソフト。  
すげぇ。→ [本家](http://paradoxxxzero.github.io/blog/)

しかも、sslで立ち上げも可能だそうで、ネットワーク越しに接続できるんじゃないかと。  
（本人のブログによると、安全じゃないからやめれとのこと。）

とりあえず、面白そうなので導入してみた。

githubもあるみたいだけれど、yaourtでいれる。archのyaourtコマンドは非公式だけど便利。でも、空気読めみたいなところがあってちょっと面白い。実装が中途半端だったりね。  
AURにはそのまんまの名前で登録されてた。

`$ yaourt -S butterfly`

それで、今回はなんか、設定がいるのかと思ったけど、すんなり入ったようで、

`# butterfly.server.py --unsecure`

のコマンドが通れば、[localhost:57575](http://localhost:57575)で確認できる。  
ここで、sslの設定しなきゃと思ったんだけど、なんか全部やってくれるっぽい。  
フランスのひとすごい。  
とりあえず、–unsecure　を外してコマンドを実行すれば、証明書つくんないとだめだよって怒られるので、怒られた通りに素直にコマンドを実行する。２つ実行したが忘れた。証明書を自動で作ってくれるので、リモートで使いたいパソコンに移しておく。  
オプションでipを指定できるので、家で使いたい人はルーターのローカルipを、リモートで使いたい人は0.0.0.0に設定する。  
この辺りは、本家のブログを読めばわかる。てゆーか、ほんとに使いやすい。

そして、systemdでつかえる.serviceのファイルも用意してくれていた。最近はarch以外にもsystemdを使うディストリビューションが増えてきたらしく、なんか感動したね。rc.confが懐かしい。とかいいつつ、freebsdをいじるときには全然使うのだがw

とかいいつつ、  
`# systemctl enable butterfly`  
`# systemctl start butterfly`  
を実行する。

と、、ここで少しはまった。yaourtで入れてくれた/etc/systemd/system/butterfly.serviceのファイルにあるbutterfly.server.py　の実行行にオプションを入れたのがまずかったっぽい。ipをダブルクオーテーションで囲むと裏でエラーが人知れず吐かれるので、注意されたし。

[bash]  
[Unit]  
Description=Butterfly Terminal Server  
After=network.target  
[Service]  
#ExecStart=/usr/bin/butterfly.server.py –host=”0.0.0.0″  
ExecStart=/usr/bin/butterfly.server.py –host=0.0.0.0  
Restart=on-abort  
[Install]  
WantedBy=multi-user.target  
[/bash]

やった！

[![名称未設定](http://cfw4.dip.jp/wordpress/wp-content/uploads/2014/07/名称未設定.png)](http://cfw4.dip.jp/wordpress/wp-content/uploads/2014/07/名称未設定.png)

これでリモートでサーバーにアクセスできるぜ！とおもったら、学内からアクセスできない。

［追記］  
本日、学内からアクセスできました。原因はサービスを起動してなかったから。。。

The post [Webで使えるターミナルを導入してみた！](https://blog.cfw4.tokyo/wordpress/48/) first appeared on [あんなことやこんなこと](https://blog.cfw4.tokyo).