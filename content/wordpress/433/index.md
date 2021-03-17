---
title: "wordpress 4.7.0 4.7.1 の脆弱性に関して"
date: 2017-02-08T01:40:36+00:00
description: "すでに公開・公表されている脆弱性に関してです。 日本メディアに関しては以下にアナウンスされています。 https://www.ipa.go.jp/security/ciadr/vul/20170206-wordpress ..."
draft: false
---

すでに公開・公表されている脆弱性に関してです。  
日本メディアに関しては以下にアナウンスされています。  
https://www.ipa.go.jp/security/ciadr/vul/20170206-wordpress.html

バージョン、4.7.0、4.7.1を使っている方は4.7.2へ至急アップデートを行ってください。

内容はwordpressに備え付けのrestAPIを叩けば記事の内容が勝手に改ざんできるということ。

自動アップデートができていない現象があったので管理者は自分で確認したほうがいいです。

この記事は再現性のレポートになります。POCも公開されています。以下のコード。  
https://github.com/linuxsec/pentest/blob/master/ruby/wordpress/41224.rb  
rubyコードだけど、WebAPIを叩ければ誰でも単純に実行できます。

すぐにアップデートしましょう。

The post [wordpress 4.7.0 4.7.1 の脆弱性に関して](https://blog.cfw4.tokyo/wordpress/433/) first appeared on [あんなことやこんなこと](https://blog.cfw4.tokyo).