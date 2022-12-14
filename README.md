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
  ・https://design.google/library/<br>
  ・https://design.google/library/material-design-awards-2018/
  
##### 依存関係の追加
 
 バージョン参考https://developer.android.com/jetpack/androidx/releases/compose-material?hl=ja
 
 implementation 'com.google.android.material:material:1.2.0'<br>
 
 ・?attrを使ってマテリアルテーマの属性をビューに適用
 
### タイポグラフィーテーマ
------------------
・マテリアルデザインコンポーネントを最大限に活用するにはテーマの属性を利用します。テーマの属性とは、アプリにおける主要な色など、異なるタイプのスタイリング情報を示す変数のことです。MaterialComponentsテーマの属性を指定することで、アプリのスタイリングを簡素化することができます。色やフォントに設定した値は全てのウィジェットに適用されるので、一貫したデザインやブランディングができます。<br>

・マテリアルテーマで使用できる全てのスタイルが表示される。↓
参考URL:https://material.io/develop/android/theming/typography

適用箇所：home_fragment.xml

### テーマオーバーレイ
-----------------
・時には画面全体ではなく、一部分のテーマのみを変更したい場合もあるかもしれません。例えば、ツールバーにダークマテリアルコンポーネントテーマを使用することができます。これはテーマオーバーレイを使用することで実現できます。
・Themeはアプリ全体のグローバルテーマを設定するために使われます。ThemeOverlayは特定のビュー、特にツールバーを上書き（オーバーレイ）するために使われます。<br>

参考箇所；activity_main.xml(Toolbar, ImageView)

### ディメンション
-----------------
・ディメンス(dimens)、またはディメンション(dimension)を使うとアプリ用に再利用可能な寸法を指定できるようになります。マージン、高さ、パッディングなどはdpという単位を使って指定します。フォントサイズに関してはspを使います。

参考箇所：dimens.xml

### カラーリソース
-----------
使用ツール：https://material.io/resources/color/#!/?view.left=1&view.right=1&primary.color=666699&secondary.color=a142f4&primary.text.color=ffffff<br>
簡易使用方法：https://qiita.com/hideaki_sago/items/ccf0b46563f903e61df0<br>

以上から配色を決めたらAndroidファイルでダウンロードをして、プロジェクトで利用する。<br>

・widgetの重なり等で適切な色にしたい場合などは以下を参照↓<br>
参考URL:https://material.io/develop/android/theming/color

### ユーザーエクスペリエンス
----------------
・RTLサポートを追加する。(コンテンツを右から左に読む)<br>
  参考URL:https://developer.android.com/training/basics/supporting-devices/languages?hl=ja<br> 
・アクセシビリティの検査<br>
・コンテンツの説明文を読むTalkBackに対応させる<br>
・ナイトモードに対応させる<br>

