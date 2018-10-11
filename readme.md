秀丸エディタからEverythingを使用する秀丸マクロ
========

# はじめに
秀丸エディタでファイル検索を高速に行う目的で、ファイル検索ソフトの[Everything](http://www.voidtools.com/)を利用するマクロを書きました。
秀丸エディタから一瞬たりとも抜けたくない方のマクロです。

### Everythingとは？
疑問に思った方は[窓の杜の記事](https://forest.watch.impress.co.jp/docs/serial/winbasic2018/1125142.html)を参照して下さい。


## 動作イメージ
あとで

# 導入手順
## Everythingの導入
`Everythingのインストール`<br>
まずは、[Everything](http://www.voidtools.com/)をダウンロードしてインストールして下さい。<br>
インストール中のオプションは既定値で構いません。（後で設定することも出来ます）

`es.exe`のインストール<br>
次に、[Everything](http://www.voidtools.com/)から`es.zip`をダウンロードします。<br>
zipファイル中の`es.exe`をEverythingをインストールしたフォルダへコピーして下さい。<br>
  (例)C:\Program Files\Everything\es.exe

## 秀丸マクロの導入
macroフォルダ中の全ファイルを秀丸エディタのマクロファイル用のフォルダにコピーしてください。<br>
`everything.mac`マクロにキーを割り当ててご使用下さい。<br>

### カスタマイズ
everything.mac を開き　＜＜＜＜あとでかく＞＞＞＞
本マクロ中の$g_exe変数（es.exeへのパス）を必要に応じて書き換えて下さい。
予め、Everything が正常動作することを確認して下さい。

# 操作方法

ESCで抜けると検索ウインドウを閉じます。
Enter 確定します、検索ウインドウは開いたままです。
		-> ファイルが一つなら開いて検索ウインドウを閉じます


# 更新履歴
2018/10/08	v2.0.0 ＜＜＜＜後で書く＞＞＞＞
2014/09/15	v1.0.1 コメントの編集
2014/05/10	v1.0.0 公開

# 動作確認を行った環境
- 秀丸エディタ ver 8.83 64bit
- Everything ver 1.4.1895(x64)
- ES.exe ver 1.1.0.10
- Windows 10 64bit

# リンク
[Everything](http://www.voidtools.com/)

# 連絡先
<http://d.hatena.ne.jp/ohtorii/> <br>
<https://github.com/ohtorii/everything> <br>
<https://twitter.com/ohtorii>
