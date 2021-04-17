---
title: "arch linux 復旧法"
date: 2014-10-27T17:47:21+00:00
description: "さっきサーバーをリブートしたら立ち上がらず、心当たりといえば、usbメモリを無断で抜いたことなんだが（おい。。。 エラーを見る限り、カーネルが壊れた模様。 archのインストールusbを作成してarch-chrootコマ ..."
draft: false
---

さっきサーバーをリブートしたら立ち上がらず、心当たりといえば、usbメモリを無断で抜いたことなんだが（おい。。。  
エラーを見る限り、カーネルが壊れた模様。

archのインストールusbを作成してarch-chrootコマンドでrootを乗っ取り、baseパッケージをインストールしなおせば復旧できます。

約10分の格闘でした。

以上。

The post [arch linux 復旧法](https://blog.cfw4.tokyo/wordpress/122/) first appeared on [あんなことやこんなこと](https://blog.cfw4.tokyo).