【テーマ名　】 basic5b
【バージョン】 1.03k
【作　成　者】 Toshihiro Takehara aka nouphet
【動作　環境】 XOOPS Cube Legacy 2.1x (HD1.04)、2.2
【ライセンス】 MIT
【公 開 日　】 2011-12-8
【修 正 日　】 2014-02-24

======================================================
説明（概要）
======================================================

　PCでもiPhone 等のスマートフォンでも使える XCL2.1x(HD1.04)・XCL2.2用テーマです。HTML5で作っています。
　閲覧環境に応じて、柔軟にページレイアウトを切り替えるレスポンシブ・ウェブデザイン（Responsive Web Design ）を採用しました。
　Xoops Cube Legacy 2.2 で動作確認しました。

　下記サイトのテンプレートを流用してXoops用のテーマとした basic5 をさらに発展させた３カラム対応のテーマです。
	http://www.onextrapixel.com/2011/09/12/create-a-responsive-web-design-template/

　ヘッダーには、xugj_assign プラグインを利用して、インストールされたモジュールに対応するメニューを自動表示するようにしています。
　また、フッターにユーザーメニュー項目も自動表示するので、xoopsの互換モジュールである「メインメニュー」「ユーザーメニュー」を利用しない運用が可能となっています。

　このテーマについては MIT ライセンスとさせていただきます。


======================================================
説明（詳細）
======================================================

　とりあえず、utf8とeucのlanguageファイルは用意しましたが、HTML5ということで utf8ベースで動作すると思います。eucでの動作は確認していません。

　メニューは、Xoops Users Group Japan(XUGJ) で GIJOEさんが提唱された xugj_assign.php を利用したメニューを採用しています。
　通常のメインメニューに表示されるのと同じ項目が自動で表示されるので、メニューの項目を編集する必要もありません。
　　http://www.xugj.org/modules/d3forum/index.php?topic_id=125

　なお、同封しているものは、オリジナルの xugj_assign.php から少し変更しているので、xugj_assign_basic.php という名称に変更しています。

　jQuery.js + jquery.jgrowlプラグインを利用して、画面遷移せずにリダイレクト表示できるので、スピーディーでセンスの良い表示が可能となっています。　なお、本テーマには、domifaraさん作成のphpファイルによるインクルード方法を用いております。
　domifaraさん、ありがとうございます。（javascriptオフ時には、リダイレクトの文字などがボックス表示されます。）

　jQueryについては、domifaraさんによるXCL2.2対応措置がとられており、jQueryの二重読み込み防止や他のjavascriptとのバッティングを可能な限り避ける仕組みが用いられております。　(xugj_already_js.php をXCL2.1対応版に差し替えております。）


【画面表示について】

　このテーマでは、メディア・クエリ（Media Queries）を利用して、表示するデバイス（ブラウザ）の画面幅によりスタイル（CSS）の切替を行います。

　基本は、左メイン・右サイドカラムの２カラム表示となっており、最大表示幅は９８０ｐｘでブラウザの幅を縮めるとそれに応じて横幅が狭まり、デバイスの幅が480px以下になると１カラム表示に切り替わります。

　なお、中央・中央カラムについては、表示順設定に応じて、トップとボットムに幅一杯にボックス表示することができます。

　■　　中央中央カラム　表示順 ０　（トップカラム）
　■　　中央中央カラム　表示順５００以上　（ボットムカラム）


======================================================
インストール
======================================================

　インストールは通常テーマと同じですが、主要モジュールのテンプレートを本テーマに最適化させ、テーマ下テンプレートとして利用する設定が可能ですので、その場合＋αの作業が必要となります。

　まずは、解凍してできあがったフォルダ「basic5a」をFTPにてサイトのテーマ・ディレクトリへコピーしてください。
　次に、次の手順でテーマ下テンプレート利用のための作業行ってください。

　完了したら通常のテーマと同様、管理画面の「互換モジュール」「テーマの管理」でこのテーマを使用する設定としてください。


【テーマ下テンプレートが利用可能な場合】

　ご利用になっている xoops がテーマ下テンプレート利用可能な場合は、本テーマディレクトリ下にある 「templates」ディレクトリに収納されたカスタマイズ済みのテンプレートを利用するようになります。

　この場合、xugj_date や xugj_block を利用しますので、本テーマ下の「up/plugin」フォルダに収納されている modifier.xugj_date.php と function.xugj_block.php をFTPにてサイトの「plugin」ディレクトリにコピーしてください。（既に存在する場合は不要）

　「plugin」ディレクトリは、XCL2.1x と XCL2.2 では場所が違うのでご注意ください。
　　　XCL2.1xの場合　/XOOPS_ROOT_PATH/class/smarty/plugins/ 
　　　XCL2.2の場合　 /XOOPS_TRUST_PATH/libs/smarty/plugins/　または
　　　　　　　　　　 /XOOPS_TRUST_PATH/libs/smartyplugins/  （preload「HdXoopsTplHook.class.php」を使っている場合）


【テーマ下テンプレートが利用できない場合】

　もし、テーマ下テンプレートを利用できない環境の場合、本テーマ下の「up/preload」フォルダにある HdXoopsTplHook.class.php をFTPにてサイトの「preload」ディレクトリに、本テーマ下の「up/plugin」フォルダにある resource.db.php をサイトの「plugin」ディレクトリにそれぞれコピーしてください。

　詳細はこちらを参照して下さい。
　　http://xoops.peak.ne.jp/md/news/index.php?page=article&storyid=450


【テーマ下テンプレート利用可能だが、本テーマのテーマ下テンプレートを使いたくない場合】

　逆に、ご利用になっている xoops がテーマ下テンプレート利用可能な状態であって、本テーマ下のテンプレートを使いたくない場合は、テーマ下にある「templates」ディレクトリを削除してください。（当該ディレクトリ内の個別のテンプレートを削除するのも良いでしょう。）
　ただし、webphotoモジュール使用時のギャラリー表示などはできなくなります。

■理由：テーマ下テンプレート利用可能なxoops（HDなど）では、次の優先順位でテンプレートを読み込むため
　１　テーマ下テンプレート
　２　現在ActiveなDBテンプレート
　３　Default(DB)テンプレート

　つまり、テンプレートを変更しようとして、Altsysで「現在ActiveなDBテンプレート」をいくら修正しても、テーマ下テンプレートがある場合はそちらが優先されてしまうのです。


【prettyPhotoを利用する場合】
　このテーマでは、jQuery のプラグインである prettyPhoto を利用するとお洒落なポップアップ画像表示ができるように設定しています。

　ご利用になるには、同封している jQuery_Pretty.class.php をサイトのプリロードディレクトリにアップロードしてください。
　xcl2.2の場合は、xoopsのcommonディレクトリに jQuery と一緒に prettyPhoto が入っていると思いますので、それで作動すると思います。もし、commonディレクトリに prettyPhoto がない場合は、このテーマに同封しているものをアップロードしてください。

　利用しているプリロードはdomifaraさん作のもので、最新のものは次のurlとなります。（domifaraさん、感謝します。）
　　　http://xodomifara.lolipop.jp/doxo/modules/d3downloads/index.php?page=singlefile&cid=3&lid=67


【webphotoの利用について】
　webphotoでprettyPhotoを利用する場合、webphotoの一般設定画面にて、次の設定を行ってください。
　　PopBoxを使用する　「いいえ」
	LightBoxを使用する「いいえ」

　一般設定画面にて設定する各種画像の大きさはデフォルトを想定しています。
　一覧表示の表示タイプは、「テーブル表示」「説明文付きリスト表示」のいずれでも prettyPhoto が動作するように設定していますが、テーブル表示を選択した場合、テーブルではなく div（ボックス）を利用した表示としており、画面幅に応じてボックスが並ぶように設定していますので、テーブル表示時のカラム数欄の数値は意味をなしません。
	LightBoxを使用する「いいえ」

　一般設定画面にて設定する各種画像の大きさはデフォルトを想定しています。
　一覧表示の表示タイプは、「テーブル表示」「説明文付きリスト表示」のいずれでも prettyPhoto が動作するように設定していますが、テーブル表示を選択した場合、テーブルではなく div（ボックス）を利用した表示としており、画面幅に応じてボックスが並ぶように設定していますので、テーブル表示時のカラム数欄の数値は意味をなしません。

　なお、このテーマでは、webphotoモジュールを「webphoto」ディレクトリ名にて利用する場合を想定して、テンプレート等の設定を行っています。もし、違うディレクトリ名でご利用の場合は、別途カスタマイズが必要となりますので、ご了承ください。


======================================================
カスタマイズ
======================================================

【メニュー表示項目の変更】

　このテーマでは、xugj_assign_phpを用いたメニュー表示を行いますが、インストールして初回表示した時に、メインメニュー表示する設定となっているメニュー項目を自動で引用してきます。（表示用のキャッシュファイルを自動作成して利用）

　従って、モジュールの管理にてモジュールの表示名を変えたり、並び順を「０」として非表示指定した場合でも、テーマのメニュー表示は以前作成したキャッシュファイルを利用することから、変更した表示となりません。

　そのような場合、FTPソフトを使って、cacheディレクトリ内の theme_basic_menus_****.php を削除してください。
　再度、サイトを表示した際に、新しくメニュー用のキャッシュファイルが自動生成されます。

　なお、domifaraさん作成の「xugjメニューキャッシュリフレシュ　管理画面モジュール」を利用すると、FTPソフトを使わずにキャッシュファイルの削除ができるので、便利だと思います。（domifaraさん、ありがとうございます。）
　　http://xodomifara.lolipop.jp/doxo/modules/d3downloads/index.php?cid=2


======================================================
利用について
======================================================

　このテーマは、MIT ライセンスです。ご自由に改変するなどしてご利用ください。

　なお、雑誌・書籍への掲載の場合には、あらかじめ当サイト管理人へご一報いただけると嬉しいです。
　　連絡先：http://xoops123.com/modules/liaise/



======================================================
バージョンアップ履歴
======================================================

2011-11-13 ver0.01
　とりあえず公開してみる。

2011-11-13 ver0.02
	480px以下のブラウザ表示の場合、CenterL、R をフロートさせて、下に回り込む設定とした。

2011-11-13 ver0.03
	各所を調整してみた。ナビの下にサブメニューを表示するようにした。

2011-11-15 ver0.03a
　画面幅調整の説明などを追記

2011-12-05 ver0.04
　xugj_already_js.php を新版に差し替えた。
　jquery.jgrowl.js を最小版に差し替えた。
　jGrowlの動作を中央上に表示するようにし、横幅を広げて透過度変更、boxshadowを表示するようにした。
　テーマ下言語ファイルに english を追加。
　style.cssにつき、次の記述間違いを修正

  　間違い
		-webkit-transition-timing function: linear, ease-in;
		-moz-transition-timing function: linear, ease-in;
		transition-timing function: linear, ease-in;

　　正解（functionの前にハイフンあり）
		-webkit-transition-timing-function: linear, ease-in;
		-moz-transition-timing-function: linear, ease-in;
		transition-timing-function: linear, ease-in;

2011-12-05 ver0.05
　basic5を３カラム対応に改造、basic5aとした。
　３カラム対応に伴い、cssの各所を修正。
　さらに、iPad等の画面幅が狭いデバイス利用の場合、リンク部分の選択可能幅を広げるようにした。
　CSS3のtransition設定をメインカラム部分等にも指定した。

change log

2013/01/14 Modified template of pico, change editor from fckeditor to ckeditor4.

