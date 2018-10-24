秀丸エディタからEverythingを使用する秀丸マクロ
========

# はじめに
秀丸エディタでファイル検索を高速に行う目的で、ファイル検索ソフトの[Everything](http://www.voidtools.com/)を利用するマクロを書きました。<br>
秀丸エディタから一瞬たりとも抜けたくない方のマクロです。

### そもそもEverythingとは何？
[窓の杜の記事](https://forest.watch.impress.co.jp/docs/serial/winbasic2018/1125142.html)を参照して下さい。

## 動作イメージ
あとで

# Everythingの導入方法
## Everythingのインストール
まずは、[Everything](http://www.voidtools.com/)をダウンロードしてインストールして下さい。<br>
インストール中のオプションは既定値で構いません。（後で設定することも出来ます）

`es.exe`のインストール<br>
次に、[Everything](http://www.voidtools.com/)から`es.zip`をダウンロードします。<br>
zipファイル中の`es.exe`をEverythingをインストールしたフォルダへコピーして下さい。<br>
  (例)C:\Program Files\Everything\es.exe

# 秀丸マクロの導入
全ファイルを秀丸エディタのマクロファイル用のフォルダにコピーしてください。<br>
`everything.mac`マクロにキーを割り当ててご使用下さい。<br>

## コピー後のフォルダ構成
	└─hidemaru-macro-folder
	    ├─everything.mac
	    ├─everything.mac.config.ini
	    └─everything_internal
	        └─search_project_folder.mac

# 操作方法
|ショートカットキー|機能|
|:---|:---|
|F1|ヘルプ表示|
|Ctrl-r|「通常の検索モード、正規表現」の切り替え|
|Ctrl-f,Ctrl-b|検索パス（通常、プロジェクトディレクトリ、カレントディレクトリ）の切り替え|
|Ctrl-d|フルパス、ファイル名検索の切り替え|
|Ctrl-n,Ctrl-p|検索履歴を進める/戻す|
|Ctrl-c,esc|キャンセルして終了|
|enter|確定して終了|

## カスタマイズ(everything.mac.config.ini)
es.exeへのパスは必要に応じて書き換えてください。
> command=C:\Program Files\Everything\es.exe

マッチしたファイルの表示数を調整するには 100 の数値を書き換えてください。
> argument_default=-s -n 100 %s 	<br>
> argument_regex=-s -n 100 -r %s

# 注意事項
本マクロが意図したとおりに動かないときはまず、Everythingが意図したとおりに動くかどうかを確認し原因の切り分けを行って下さい。

# 更新履歴
### 2018/10/08	v2.0.0 
＜＜＜＜後で書く＞＞＞＞
### 2014/09/15	v1.0.1
コメントの編集
### 2014/05/10	v1.0.0 
公開

# 動作確認を行った環境
- Windows 10 64bit
- 秀丸エディタ ver 8.83 64bit
- [Everything ver 1.4.1895(x64)](http://www.voidtools.com/)
- [ES.exe ver 1.1.0.10](http://www.voidtools.com/)

# リンク
[Everything](http://www.voidtools.com/)

# 連絡先
<http://d.hatena.ne.jp/ohtorii/> <br>
<https://github.com/ohtorii/everything> <br>
<https://twitter.com/ohtorii>
