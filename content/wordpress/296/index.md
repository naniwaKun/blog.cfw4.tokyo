---
title: "スティックPC、DG-STK1B でマイクラ鯖を立てた話"
date: 2016-05-13T04:04:36+00:00
description: "これは維持費500円／年（電気代）でマイクラ鯖（バニラ）を立てる話です。 ついにドスパラのスティックPCを買った。前から欲しかったのだが、躊躇してたのは三つ。archlinuxのインストール記事が少ないのと値段と用途がな ..."
draft: false
---

これは維持費500円／年（電気代）でマイクラ鯖（バニラ）を立てる話です。

ついにドスパラのスティックPCを買った。前から欲しかったのだが、躊躇してたのは三つ。archlinuxのインストール記事が少ないのと値段と用途がなかったからだ。昨年末から1万を切っており、マインクラフトのサーバーを立てたくなったので買った。つまりサーバー用途である。

僕が買ったのは「[Diginnos Stick DG-STK1B](http://www.amazon.co.jp/Diginnos-Stick-DG-STK1B-%E3%82%B9%E3%83%86%E3%82%A3%E3%83%83%E3%82%AF%E5%9E%8B%E3%83%91%E3%82%BD%E3%82%B3%E3%83%B3-Windows/dp/B015XU925A/ref=sr_1_1?s=computers&ie=UTF8&qid=1457073213&sr=1-1&keywords=DG-STK1B)」である。後継機の「[DG-STK3](http://www.dospara.co.jp/5shopping/detail_prime.php?tg=2&tc=473&mc=5700&sn=0&_bdadid=JPGTE5.00bv0000)」を買おうと思ったのだが、スペックが対して変わらないのと、店頭で500円安かったのと、[キーボード](http://www.amazon.co.jp/%E3%83%9E%E3%82%A4%E3%82%AF%E3%83%AD%E3%82%BD%E3%83%95%E3%83%88-%E6%9A%97%E5%8F%B7%E5%8C%96%E6%A9%9F%E8%83%BD%E6%90%AD%E8%BC%89-%E3%83%AF%E3%82%A4%E3%83%A4%E3%83%AC%E3%82%B9-Keyboard-N9Z-00023/dp/B01B1DV094)がついてきたからだ。  
後継機の方はプラスチックボディらしく、ファンレス金属ボディのほうが良かったと思う。軽量コンパクト化は熱がこもりやすいではないか、うん。と一人で納得した。ドスパラは在庫を無くしたいのだろうか。店頭で9,480円だった。今はもう少し安いかもしれない。

そろそろ本題に入ろう。このPCにはwindows10がプリインストールされているが、USBに回復ドライブを作成したあとさくっと削除した。そしてサーバー運用のために以下の買い物をした。

[USB経由で有線ランつなげるやつ](http://www.amazon.co.jp/gp/product/B00LLUEJXW/ref=oh_aui_detailpage_o00_s00?ie=UTF8&psc=1)

[HDMIメスメスコネクタ](http://www.amazon.co.jp/gp/product/B019GXIMN8/ref=oh_aui_detailpage_o01_s00?ie=UTF8&psc=1)

コネクタは各自の環境に合わせるとして、内臓のwifiモジュールをlinuxが認識してくれないので、無理に苦労するぐらいならと思って買った。もっと安いのもあると思う。

ということで、Linuxのインストールだが,幾つかのブログにお世話になった。だが、最終的に利用した環境だけのべておく。

http://cdimage.debian.org/cdimage/unofficial/efi-development/jessie-upload3/

で公開されているdebianインストールディスクだ。これを用いるだけで、32bitのUEFIの悪魔から逃れることができる。おそらく,32bitUEFI環境に64bitlinuxをインストールするのは技術的に難しくないのだが、ディストリビューションの思想的なことだったり、UEFIの仕様に従うと難しいようだ。だからパッケージマネージャー管理から外れた運用になってしまうのだが、それは使用し続けることで、サーバーを不安定にしてしまう。上記のurlによる環境はdebian開発者によるものなのでその辺に転がっている怪しいtips寄りは信用できる。一応、インストールできた環境を下にのせておく。

32bit archlinux 安定に稼働する。但し、32bitカーネル  
64bit archlinux ハックすれば起動できる。でもする気が起きないほど面倒くさい。  
64bit ubuntu ハックすれば起動できる。面倒くさいし、aptが壊れて、不安定になってしまった。  
64bit debian 上記のISOで問題なくインストールできる。 Bay Trail-based machines と明確に書かれている。linuxカーネルにもパッチがあたっているらしい。debianなので頻繁なアップデートで壊れることもなさそう。GUIインストーラーで最小構成インストールできる。安定稼働。カーネルは3系。

以上、DG-STK1Bに導入するlinuxの話でしたｗ

マイクラ導入は癖なく普通のPC通りです。最大7人ぐらいで遊んでいますが、ネザーゲートくぐるときにラグが出るぐらいで他に不便なところはないです。MODいれるような余力はないです。バニラで遊びましょう。バニラで遊ぶにしてもspigotを導入したほうが使用感は軽くてトラブルが少ない印象です。

The post [スティックPC、DG-STK1B でマイクラ鯖を立てた話](https://blog.cfw4.tokyo/wordpress/296/) first appeared on [あんなことやこんなこと](https://blog.cfw4.tokyo).