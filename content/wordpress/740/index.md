---
title: "32bitUEFIのスティックPCのdebian（64bit）を8から9にアップグレードした話"
date: 2017-09-17T21:20:02+00:00
description: "スティックPC、DG-STK1B でマイクラ鯖を立てた話 この記事の続き。 前回は32bitUEFI環境に64bitlinuxをインストールするに当たって、以下のOSイメージを使えば一発ですよ。という話をした。 同じ状況 ..."
draft: false
---

[スティックPC、DG-STK1B でマイクラ鯖を立てた話](http://www.cfw4.tk/wordpress/296)

この記事の続き。

前回は32bitUEFI環境に64bitlinuxをインストールするに当たって、以下のOSイメージを使えば一発ですよ。という話をした。

<figure class="wp-block-embed"><div class="wp-block-embed__wrapper">
http://cdimage.debian.org/cdimage/unofficial/efi-development/jessie-upload3/
</div></figure>

同じ状況の方がアップグレードするための話

前回の記事に結構アクセスが来ていて、反応を見ていると楽しかった。スティックPCでWindowsが重くてアップデートできなくなった難民の方や、子供ために固定費を浮かせてマイクラ鯖立てるお父さんとかｗ  
32bitでインストールするのは簡単だけど、ちょうど移行の時期で、64bitじゃないとパフォーマンスが出ないソフトが結構あった。javaのヒープとかね。だからみんなの目に止まったんだと思う。

それから時間は過ぎて、debianのアップデートがきた。debianは結構お硬いイメージのディストリビューションで、パッケージがもろ古いので、早くアップデートしたくて、debianの”unofficial”なパッケージを監視していたが、アナウンスがない。重い腰を上げて調べてみると、stretch(9)では、公式に対応したそうだ。

なので、この状態のままアップグレードを強行することにした。

以下の手順を参照されたい。

<script src="https://gist.github.com/naniwaKun/ed99711899c4816b3cf445dd0785d17c.js"></script>

無事に再起動できた。

最近はマイクラに飽きてきて、たまにしかサーバーを起動しなくなった。その代わりにwebで使えるIDEをインストールしたので今度はその話をしようかな。

The post [32bitUEFIのスティックPCのdebian（64bit）を8から9にアップグレードした話](https://blog.cfw4.tokyo/wordpress/740/) first appeared on [あんなことやこんなこと](https://blog.cfw4.tokyo).