---
title: "読み上げアプリ作ったので公開する。"
date: 2016-03-20T11:31:32+00:00
description: "しょぼい読み上げアプリを作ったのでテンションで公開しようと思う。クリップボードを0.1秒間隔で監視して読み上げるアプリケーションです。棒読みちゃんの設定がややこしいので完全に自分向け。僕はツイキャスの読み上げに使ってます ..."
draft: false
---

しょぼい読み上げアプリを作ったのでテンションで公開しようと思う。クリップボードを0.1秒間隔で監視して読み上げるアプリケーションです。棒読みちゃんの設定がややこしいので完全に自分向け。僕はツイキャスの読み上げに使ってます。  
動作確認環境は、64bit windows10 だけど、たぶん最新のjavaの環境とクリップボードがあれば動くと思う（未確認）。興味のある人は勝手に使ってくださいという気分です。  
また、このアプリケーションは個人が趣味の範囲（いかなる事業, 営利活動とも無関係）で書いたものです。

[よみよみちゃん](http://www.cfw4.tk/wordpress/wp-content/uploads/2016/03/yomiyomi.zip)

### **はじめに**

本アプリケーションは、[VoiceText Web API](https://cloud.voicetext.jp/webapi) に通信して音声を取得、再生するアプリです。記事公開時は個人利用は無料ですが、音声の二次利用は制限されています。また、VoiceText Web API の規約は変更することも予想されます。本アプリケーションは”VoiceText Web API”の規約違反を助長する意図で公開したものではないと宣言しておきます。  
また、本アプリケーションを使用したことで不利益を被っても利用者の責任であるものとします。開発者である私は一切の責任を負いません。  
また、開発されたコードには、[voicetext4j](https://github.com/making/voicetext4j/)で公開されているコードが含まれています。

### **インストールの前に**

VoiceText Web API の登録とjava(jre)のインストールをしておくこと。

### **インストール**

よみよみちゃんをダウンロードして展開して好きなところに設置してください。そして、VoiceText Web API を登録して得られたAPIキーをkey.txtに書き込んでください。また、java(jre)をインストールしておいてください。以上でインストールは終了です。

### **使い方**

yomiyomi.exeを起動(通常はダブルクリック)してください。ウィンドウの”Start”ボタンでクリップボードの読み上げを開始し、”End”ボタンでアプリケーションを終了します。

<figure id="attachment_309" aria-describedby="caption-attachment-309" style="width: 293px" class="wp-caption aligncenter"><a href="http://www.cfw4.tk/wordpress/wp-content/uploads/2016/03/%E7%84%A1_%E9%A1%8C.png" rel="attachment wp-att-309"><img loading="lazy" class="size-full wp-image-309" src="http://www.cfw4.tk/wordpress/wp-content/uploads/2016/03/%E7%84%A1_%E9%A1%8C.png" alt="起動画面" width="303" height="83"></a><figcaption id="caption-attachment-309" class="wp-caption-text">起動画面</figcaption></figure>

### **ライセンス**

ライセンスは「Apache License, Version 2.0.」とします。近々ソースコードを公開する予定です。

The post [読み上げアプリ作ったので公開する。](https://blog.cfw4.tokyo/wordpress/301/) first appeared on [あんなことやこんなこと](https://blog.cfw4.tokyo).