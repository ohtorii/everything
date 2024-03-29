﻿秀丸エディタからEverythingを使用する秀丸マクロ
========


![GitHub release](https://img.shields.io/github/release/ohtorii/everything.svg)
![Maintenance](https://img.shields.io/maintenance/yes/2025.svg)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)


# はじめに

ファイルを探す時間を大きく削減するために、<br>
ファイル検索ソフトの[Everything](http://www.voidtools.com/)を秀丸エディタから利用するマクロを書きました。

## そもそもEverythingとは何？

[窓の杜の記事](https://forest.watch.impress.co.jp/docs/serial/winbasic2018/1125142.html)を参照して下さい。

# 動作イメージ

## ファイル検索→対象の決定→ファイルを開く

![動作イメージ](images/everything.gif "動作イメージ")

## 検索対象のフォルダ切り替え

![動作イメージ](images/everything_bf.gif "動作イメージ")

## 正規表現
![動作イメージ](images/everything_r.gif "動作イメージ")

## 検索履歴

![動作イメージ](images/everything_pn.gif "動作イメージ")


# Everythingの導入方法

まずは、Everythingアプリを導入して利用できるようにします。

その後で秀丸マクロを導入します。

## ステップ 1/2

まずは、[Everything本体](http://www.voidtools.com/)を公式サイトからダウンロードしてインストールして下さい。<br>
インストール中のオプションは既定値で構いません。（後で設定することが出来ます）

## ステップ 1/2

`es.exe`のインストール方法<br>
次に、[Everything](http://www.voidtools.com/)から`ES-バージョン番号.zip`をダウンロードします。<br>
zipファイル中の`es.exe`をEverythingをインストールしたフォルダへコピーして下さい。<br>

     (例)
     C:\Program Files\Everything\es.exe

[最新版への直リン（2018年10月25日　現在）](https://www.voidtools.com/ES-1.1.0.10.zip)

# 秀丸マクロの導入

## ステップ 1/2

全ファイルを秀丸エディタのマクロファイル用のフォルダにコピーしてください。<br>
`everything.mac`マクロにキーを割り当ててご使用下さい。<br>

*コピー後のフォルダ構成*

    └─hidemaru-macro-folder
        └─everything
            ├─everything.mac
            ├─everything.mac.config.ini
            └─everything_internal
                ├─search_project_folder.mac
                └─search_project_folder.mac.config.ini

## ステップ 1/2

[でんがくDLL](http://www.ceres.dti.ne.jp/~sugiura/)を秀丸エディタにインストールして下さい。<br>
ダイアログを表示するために必要なDLLです。

# 操作方法

|ショートカットキー|機能|
|:---|:---|
|Ctrl-b,Ctrl+f|検索パス（通常、プロジェクトフォルダ、カレントフォルダ）の切り替え|
|Ctrl-r|「通常の検索モード、正規表現」の切り替え|
|Ctrl-d|フルパス、ファイル名検索の切り替え|
|Ctrl-p,Ctrl-n|検索履歴を進める/戻す|
|Ctrl-1 ～ Ctrl-9|検索履歴を選択します|
|Ctrl-s,Alt-s|検索ボックスに入力フォーカスを移動する|
|Ctrl-c,esc|キャンセルして終了|
|ctrl-m,enter|確定して終了|
|F1|ヘルプ表示|

操作方法はVIMの[ctrlp.vim](https://github.com/ctrlpvim/ctrlp.vim)と概ね同じです。


# カスタマイズ

## everything.mac.config.ini

マクロ本体のカスタマイズを行うことが出来ます。

es.exeへのパスは必要に応じて書き換えてください。
> command=C:\Program Files\Everything\es.exe

マッチしたファイルの表示数を調整するには 100 の数値を書き換えてください。
> argument_default=-s -n 100 %s 	<br>
> argument_regex=-s -n 100 -r %s

## everything_internal\search_project_folder.mac.config.ini

プロジェクトフォルダをカスタマイズできます。

> [project_folder]	<br>
> _0=.git	<br>
> _1=.hg	<br>
> _2=.svn	<br>
> _3=.bzr	<br>
> _4=_darcs	<br>


# 注意事項

本マクロが意図したとおりに動かないときはまず、Everythingが意図したとおりに動くかどうかを確認し原因の切り分けを行って下さい。


# ダウンロード

こちらから動作確認済みのアーカイブをダウンロードして下さい。<br>
https://github.com/ohtorii/everything/releases

*注意*
masterブランチを取得しても多分動作しないです。<br>
一人で開発しているのでブランチを作らずに気楽に開発してます。（仕事じゃないしね😉）


# 更新履歴

## 2022/04/24 ver 2.1.1

### バグ修正🐛

- ” 新規ファイル、かつ、入力文字あり”の条件でファイル内容を検索結果で上書き視してしまう問題を修正しました。

## 2019/02/09 ver 2.1.0

- 検索に集中できるようにGUIのレイアウトを変更しました😘
	- 機能名とショートカット名を全てGUIに表示しました。
- キーボードショートカットの追加
	- Ctrl-1～Ctrl-9キーで検索履歴を選択できるようにしました。
	- Ctrl-mをエンターキーとして認識するようにしました。
	- 「Alt-Sキー・Ctrl-Sキー」でキーボードフォーカスを検索ボックスに移動できるようにしました。

## 2019/01/20 ver 2.0.4

- エスケープキーを連打したときにマクロを終了するかどうかをユーザーに問い合わせていましたが、今回から問い合わせないようにしました。
- ダイアログが秀丸エディタの裏側に隠れることがあったので常に前面に表示するようにしました。

## 2018/10/27 ver 2.0.3

v2.0.2の対応が不十分でした、更に修正しました。

## 2018/10/27 ver 2.0.2

正規表現の検索結果をEverythingのGUI版と同じになるように修正しました。

## 2018/10/25 ver 2.0.1

説明文を修正。

## 2018/10/08	v2.0.0 

- ファイルを高速に見付けるために全て作り直しました。
	- リアルタイムで絞り込み検索が出来るようにしました。
	- その他機能は操作方法を参照して下さい。

## 2014/09/15	v1.0.1

コメントの編集

## 2014/05/10	v1.0.0 

公開

# バージョン番号のルール

バージョン番号の表記方法

バージョン番号は version 1.2.3 のように表記され、それぞれ major.minor.revision を表します。

|番号|説明|
|:--:|:--:|
|major|互換性が失われる大きな変更を表します|
|minor|機能追加のように互換性のある更新を表します|
|revision|バグ修正のように機能そのものに変化が無い軽微な更新を表します|


# 動作確認を行った環境

- Windows 10 64bit
- 秀丸エディタ ver 8.83 64bit
- [田楽DLL Ver.3.20 64bit](http://www.ceres.dti.ne.jp/~sugiura/)
- [Everything ver 1.4.1895(x64)](http://www.voidtools.com/)
- [ES.exe ver 1.1.0.10](http://www.voidtools.com/)

# リンク

[Everything](http://www.voidtools.com/)

# 連絡先

<https://ohtorii.hatenadiary.jp/> <br>
<https://github.com/ohtorii/everything> <br>
<https://twitter.com/ohtorii>
