---
title: "H330でXonar DGXを通して音楽聞くと左右音が反転する話。"
date: 2016-12-12T15:24:38+00:00
description: "僕は未だに lenovo H330 を使っているのだが、2年ほど前にサウンドカードXonar DGXを増設していた。H330のマザーボードとケースは独自規格なので、h330のオーディオのケーブルに互換性がない。そこで、配 ..."
draft: false
---

僕は未だに [lenovo H330](http://shopap.lenovo.com/jp/desktops/essential/h-series/h330/) を使っているのだが、2年ほど前にサウンドカード[Xonar DGX](https://www.asus.com/jp/Sound-Cards/Xonar_DGX/)を増設していた。H330のマザーボードとケースは独自規格なので、h330のオーディオのケーブルに互換性がない。そこで、[配線ケーブル](https://www.amazon.co.jp/AINEX-EX-001-%E3%82%A2%E3%82%A4%E3%83%8D%E3%83%83%E3%82%AF%E3%82%B9-%E3%83%94%E3%83%B3%E9%85%8D%E5%88%97%E4%BA%A4%E6%8F%9B%E3%82%B1%E3%83%BC%E3%83%96%E3%83%AB6%E6%9C%AC%E5%85%A5%E3%82%8A/dp/B000FHQAAC/ref=sr_1_15?s=computers&ie=UTF8&qid=1481555962&sr=1-15&keywords=ainex%E3%82%B1%E3%83%BC%E3%83%96%E3%83%AB)を使って配列を変換するのだが、その配線が間違っていたのでステレオ音声の左右が間違っていた話です。

配線はこんな感じ

[![](http://www.cfw4.tk/wp-content/uploads/2017/02/e8483046e6c02cdafd03ff84970bfd61.jpg)](http://www.cfw4.tk/wp-content/uploads/2017/02/e8483046e6c02cdafd03ff84970bfd61.jpg)

参考にしていた情報はこの[ブログ](http://nyarurato.hatenablog.com/entry/2014/10/11/011748)なのだが、左右の音が逆になるので、[レノボのフォーラム](https://forums.lenovo.com/t5/ThinkCentre-A-E-M-S-Series/ThinkCentre-A60-front-panels-power-audio-and-USB-pinout/td-p/190651)を参考にして修正する。

配線したときのメモはtwitterにとってあるので、参考にしたい方は以下のツイートを参考にしてください。

> Audioフロントパネル側
> 
> xx|xx|12|11|10|09|08  
> 07|06|05|xx|03|xx|zz
> 
> — なにわくん (@naniwarinrin) [2016年12月12日](https://twitter.com/naniwarinrin/status/808296370066976768)

> lenovoマザボ側
> 
> 09|07|10|11|12  
> 06|zz|05|03|08
> 
> — なにわくん (@naniwarinrin) [2016年12月12日](https://twitter.com/naniwarinrin/status/808296606764122118)

いじょう！

The post [H330でXonar DGXを通して音楽聞くと左右音が反転する話。](https://blog.cfw4.tokyo/wordpress/389/) first appeared on [あんなことやこんなこと](https://blog.cfw4.tokyo).