---
title: "中間発表のやり方"
date: 2014-07-13T08:56:34+00:00
description: "さて、昨日中間発表が終わりました。 しんどかったー。 今回からlatexのコマンドをplatexからlualatexに変えました。 あ、あと、ポイントとしては、プレゼンソフトの対応でしょうか、以下忘備録としてまとめ。 m ..."
draft: false
---

さて、昨日中間発表が終わりました。  
しんどかったー。

今回からlatexのコマンドをplatexからlualatexに変えました。  
あ、あと、ポイントとしては、プレゼンソフトの対応でしょうか、以下忘備録としてまとめ。

mactex(texlive)のインストール  
基本的に[公式](http://oku.edu.mie-u.ac.jp/~okumura/texwiki/?Mac)に従う。だけど、MacPortから入れようとしたら、インストールは出来るんだけど、tlmgrのコマンドが見つからなかったので、おとなしく.pkgからインストールした。いつも思うことだけど、rikenのサーバーが早いです。  
linuxユーザーはtexliveを入れてください。大体のディストリビューションでもワンライナーで入ると思います。  
これで、lualatexのコマンドが通る。が、  
以下のコマンドを実行しておくこと  
`$ sudo tlmgr update --self --all`  
これで最新版にアップデートしてくれるっぽい。

ちなみに、lualatexやxelatexはここ最近できたコマンドで、一気にpdfを作ってくれます。インストールやだって方は[ShareLatex](https://www.sharelatex.com)を使おう。今は日本語に対応しています。バックアップにもなるしね。実はsharelatex自体もオープンソース[github](https://github.com/sharelatex/sharelatex)なのでサーバーに入れいたい方はどうぞ。こんなところでもrailsが使われててびっくり。

これで、環境が整ったので、vimかなんかでスライドを作成する。自分のテンプレートは以下のとおり。

内容は各セクションで\input{}で指定されてるファイルに書き込む。  
これで、pdfはできるのだが、PDFでプレゼンって難しいよね。そこで、以下のコマンドを実行。(imagemagick必須)  
`convert -density 300 tex.pdf slide.jpg `  
これで、すべてのスライドを画像に変換してくれる。-densityオプションで解像度を指定できる。コマンド例はdpi単位で指定してる。画像をパワポなり、リブレなりに投げれば発表者ツールが使える。

これでプレゼンできるね！

The post [中間発表のやり方](https://blog.cfw4.tokyo/wordpress/56/) first appeared on [あんなことやこんなこと](https://blog.cfw4.tokyo).