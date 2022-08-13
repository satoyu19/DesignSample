 Androidスタイリングシステム
 ------------------
・Androidはアプリ内の全てのビューの見た目を制御するための豊富なスタイリングシステムを備えています。テーマやスタイル、スタイリングに影響を与えるビューの属性などを使用することができます。<br>
参考URL:https://developer.android.com/guide/topics/ui/look-and-feel/themes?hl=ja

 以下のダイアグラムはスタイリングのそれぞれのメソッドの優先順位をまとめたものです。
 ピラミッドダイアグラムはシステムによって下から上に順番に適用されるスタイリングメソッドの順番を示しています。例えば、テーマの中でテキストサイズを設定し、それからビューの属性の中で異なるテキストサイズを設定した場合、ビューの属性がテーマのスタイルを上書きします。
![image](https://user-images.githubusercontent.com/96398365/184465484-7433d6d8-f789-4f3b-af87-480bd24c9fb2.png)

##### Theme
・テーマはデフォルトフォントや原色のような一般的な設定をアプリに適用するのに適している。<br>

注意： テキストの設定にテーマとスタイルの両方を使用する際、テーマのテキストプロパティにスタイル中で設定/継承されているものを上書きさせたい場合はテキストプロパティをtextAppearance属性として適用させる必要があります。

### マテリアルデザイン
----------------
・MaterialComponentsテーマは制御用のマテリアルデザインを実装しており、テーマの属性を使用しており、カスタマイズ可能です。<br>

マテリアルデザインの実装例
  ・https://design.google/library/
  ・https://design.google/library/material-design-awards-2018/
  
##### 依存関係の追加
 
 バージョン参考https://developer.android.com/jetpack/androidx/releases/compose-material?hl=ja
 
 implementation 'com.google.android.material:material:1.2.0'
 
