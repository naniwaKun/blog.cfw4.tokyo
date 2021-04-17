---
title: "podTerm : Podcastはterminalで聞こう！"
date: 2015-02-17T07:55:02+00:00
description: "皆さん、podcastをどうやって聞いてますでしょうか？iTunes?, iphone?, android? 僕はガラケーユーザーだし、ノートパソコンは研究で使うからあんまり汚したくない。かと言って家のWindowsに ..."
draft: false
---

皆さん、podcastをどうやって聞いてますでしょうか？iTunes?, iphone?, android?

僕はガラケーユーザーだし、ノートパソコンは研究で使うからあんまり汚したくない。かと言って家のWindowsに iTunes を入れるのは嫌だ。でも、Podcast聞く時って作業中とかだしな。RSSのURLだけあれば、いいんだよなー。って考えてるうちに作っちゃいました。

一応、terminalからpodcastのエピソードをダウンロードするソフトならあったんだけど、ダウンロードする必要ある？

ってことで作っちゃいました！Rubyのシンプルなやつです。perlで書こうとしたら長くなっちゃうので、初めてのRubyでした。生産性はあがってるんですねぇ。5年前に触った時は全然好きになれなかったけれど。しかし、初めてgithubのアカウントとったぜ。。

興味ある方は[こちら](https://github.com/naniwaradio/podTerm)。ブラウザを開かずにpodcastを聞けるので仕事に集中できます。まだ全然作りが荒いんだけど、これから更新したかチェックできるようにしたいな。再生済みでマークできたりしたらいいよね。

使ってみたらこんな感じ。

<!--[if lt IE 9]><script>document.createElement('video');</script><![endif]--><video class="wp-video-shortcode" id="video-158-1" width="1200" height="675" preload="metadata" controls="controls"><source type="video/mp4" src="http://cfw4.dip.jp/wordpress/wp-content/uploads/2015/02/000.mp4?_=1"></source><a href="http://cfw4.dip.jp/wordpress/wp-content/uploads/2015/02/000.mp4">http://cfw4.dip.jp/wordpress/wp-content/uploads/2015/02/000.mp4</a></video>

[追記]

使用感を多少改善してAURにPKGBUILDをポストしました。  
archlinuxユーザーならワンライナーでインストールできます。

`$ yaourt -S podterm-git`

The post [podTerm : Podcastはterminalで聞こう！](https://blog.cfw4.tokyo/wordpress/158/) first appeared on [あんなことやこんなこと](https://blog.cfw4.tokyo).