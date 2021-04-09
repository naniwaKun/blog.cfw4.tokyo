+++
author = "naniwa"
categories = ["あんなことやこんなこと", ""]
date = "2021-03-18T12:50:03+09:00"
description = "wordpress から hugoへブログを移動した。"
draft = false
title = "hello hugo world"
+++

URLそのままで、wordpress から hugoへブログを移動しました。

URLを引き継ぎたかったので、移動には自作の[rubyスクリプト](https://gitlab.com/naniwastrongboy/wordpress2hugo/-/blob/master/main.rb)を使いました。こういうのは車輪の再発明なんて呼ばなくて、自分にフィットしたやり方でやるほうが効率が良いのだ。

```ruby
#!/bin/ruby

require 'xmlsimple'
require 'open-uri'
require 'reverse_markdown'
require 'date'
require "fileutils"

domain = "XXXX.YYYYY.ZZZ"
rss = "https://" + domain + "/feed"

hash = XmlSimple.xml_in(open(rss))
arr = hash["channel"][0]["item"]

arr.each do |item|

  title = item["title"][0].empty? ? "無題" : item["title"][0]
  date = Time.parse(item["pubDate"][0]).iso8601()
  contents = ReverseMarkdown.convert item["encoded"][0]
  discription = ReverseMarkdown.convert item["description"][0]
  discription = discription.split("...")[0] + "..."

  dir =  item["link"][0].split("/")[3] +"/"+ item["link"][0].split("/")[4]
  name = "/index.md"
  FileUtils.mkdir_p(dir)
  mdfile = "---\n"
  mdfile = mdfile + 'title: "' + title + '"'
  mdfile = mdfile + "\ndate: " + date + "\n"
  mdfile = mdfile + 'description: "' + discription  + '"'
  mdfile = mdfile + "\ndraft: false"
  mdfile = mdfile + "\n---"
  mdfile = mdfile + "\n\n"
  mdfile = mdfile + contents.to_s

  File.open(dir + name, mode = "w"){|f|
    f.write(mdfile)
  }
end
```

頂いていたコメントは過去の記事の中に書かれています。


ところで、コメントのシステムが変わりました。システムは変わりましたが、方針は何も変わっていません。今後とも相変わらずどうぞよろしくお願いいたします。
