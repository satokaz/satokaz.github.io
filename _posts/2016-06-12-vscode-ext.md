﻿---
layout: post
title:  "[vscode] 勉強に利用した Visual Studio Code の Extension"
---

markdown editor として利用しはじめた Visual Studio Code だけど、エクステンション機能が実装されてから、いろいろと source code を参考にして勉強している中で、Extensin そのものを修正してたりしてしまう事案がいくつか。記念にリスト化してみる。

いつのまにか、Extension のために Javascript や Typescript を勉強しはじめているオレがいた・・・
目標としては、Solaris と色々と絡めたいと思ってはいるが、いまのところ markdown で Solaris 関連のドキュメント書くのがせいいっぱいw

## Issue や PR したエクステンション

* vscode-pandoc
  * [https://github.com/dfinke/vscode-pandoc](https://github.com/dfinke/vscode-pandoc)
  * OS X での挙動確認とオプションを個別に記述できるように機能を追加。はじめて PR に挑戦。 
    * [does not work with Mac OS X #2](https://github.com/dfinke/vscode-pandoc/issues/2)
    * [Setting additional pandoc options #5](https://github.com/dfinke/vscode-pandoc/issues/5)
* Project Manager Extension for Visual Studio Code
  * [https://github.com/alefragnani/vscode-project-manager](https://github.com/alefragnani/vscode-project-manager)
  * こちらも Mac OS X で動作するようにお手伝い
    * [Project switching does not work #7](https://github.com/alefragnani/vscode-project-manager/issues/7)
* vscode-ext-yandex-translate
  * [https://github.com/airstep/vscode-ext-yandex-translate](https://github.com/airstep/vscode-ext-yandex-translate)
  * 日本語も変換候補として対応していたので追加してもらう
    * [Add "en-ja" and "ja-en" combinations](https://github.com/airstep/vscode-ext-yandex-translate/pulls?q=is%3Apr+is%3Aclosed)
* vscode-gist
  * [https://github.com/dbankier/vscode-gist](https://github.com/dbankier/vscode-gist)
  * secret gist が public gist になってしまう問題の対応
    * [PRIVATE gist is public #4](https://github.com/dbankier/vscode-gist/issues/4)
  * 作者さん、やっぱり vim にもどっちゃうということで、メンテ引き受けてくれる人を募集中
    * [https://gist.github.com/dbankier/5d3e699360419cb291b0f1e3724f5fde](https://gist.github.com/dbankier/5d3e699360419cb291b0f1e3724f5fde)
* MarkdownTOC(Table Of Contents) Plugin for Visual Studio Code.
  * [https://github.com/AlanWalk/Markdown-TOC](https://github.com/AlanWalk/Markdown-TOC)
  * codeblocks がエラーになるので、その対策を PR
    * [Fix : Interim fix for the codeblock](https://github.com/AlanWalk/Markdown-TOC/pulls)


## 自分で作ってみたエクステンション

* vscode-insert-date
  * [https://github.com/satokaz/insert-date](https://github.com/satokaz/insert-date)
  * カーソルがいる場所に日付と時刻を挿入するエクステンション。見よう見ままねで作成。
* vscode-toggleProxy
  * [https://marketplace.visualstudio.com/items?itemName=satokaz.vscode-toggleproxy](https://marketplace.visualstudio.com/items?itemName=satokaz.vscode-toggleproxy)
  * [https://github.com/satokaz/vscode-toggleProxy](https://github.com/satokaz/vscode-toggleProxy)
  * ちょーニッチというか、オレ得な感じですが、settings.json にある http.proxy 設定をステータスバーの地球アイコンで on/off するエクステンション。会社と家の環境違うので毎回切り替えるのが面倒だなと、面倒なエクステンション作成にとりかかってみた。
  settings.json の入れ替え処理を atomic にできていない気がするので怖いひ・・・
