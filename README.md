# ゲームデザイン実習
2017年度 デジタルアーツ東京 ゲームデザイン実習用リポジトリー。

# 講義予定
- [シラバス](syllabus.md)

# 参考URL
- [Phaserのスプライト画像の用意の仕方](docs/06_phaser-sprite.md)
- [LubuntuでPhaserのExampleを動かす手順](docs/06_phaser_boot.md)
- [GitHubにUnityのプロジェクトを新規に作成する手順(VisualStudioも同様)](http://am1tanaka.hatenablog.com/entry/2016/02/05/102508)
- [GitHub Desktopで.gitignoreが作られなかった場合の対処](http://am1tanaka.hatenablog.com/entry/2017/06/09/234448)
- [魔王魂](http://maoudamashii.jokersounds.com/)
- [効果音ラボ](http://soundeffect-lab.info/)
- [甘茶の音楽工房](http://amachamusic.chagasi.com/)
- [PANICPUMPKIN ファミコン風オリジナル音楽](http://pansound.com/panicpumpkin/)

# 15回目
## 予定
- [今日の動画](https://www.youtube.com/watch?v=bqXG2PzKxWI)
- JekyllによるWebページ作成 / Jekyllの使い方を調べながら学んでみよう
  - https://jekyllrb-ja.github.io/
  - [ドットインストール Jekyll](http://dotinstall.com/lessons/basic_jekyll)
  - Jekyllにはブログスタイルのポスト(Posts)と、静的ページスタイルのページ(Pages)がある。作品ページなどは、Pagesになる http://jekyllrb-ja.github.io/docs/pages/
- 夏休みに作ったものを、GitHub Pagesで公開する。できればJekyllで。無理そうならマークダウンで
- 企画を検討

本講義の成績は、これまでの日常点と、夏休みの作品ページによって決める。

# 14回目
## 話題
- [4Gamer.net CEDEC 2017:ヘキサドライブが新人教育のために導入した「若手小規模プロジェクト」とは何か](http://jp.gamesindustry.biz/article/1708/17083104/)
- [ソフトウェアテスト SHIFT](http://www.shiftinc.jp/topics/game-saiyo/?m=tw002)

## 金曜日の確認
- 発表会の仕上げの確認
  - 発表内容は以下の通り
    - 作品名
    - 作品の概要
    - 操作方法
    - ゲームのルール
    - どこを自分で開発したか
    - 利用したアセットやチュートリアルを、全て紹介
  - 各内容については、 https://unityroom.com/ の作品を何本か確認して、どのように書けば分かりやすいかを研究して、工夫すること

## 内容
- [ドットインストール. Markdown記法](http://dotinstall.com/lessons/basic_markdown_v2)
- [MagicaVoxel](https://ephtracy.github.io/)
  - [だいし. MagicaVoxelで作ったプリキュアをUnityで動かす](http://github.dev7.jp/b/2015/12/15/precureadv20151213/#.WYNRTC70CQo.twitter)
- [ドット絵ツール piskel](http://www.piskelapp.com/)
- [フリーフォント一覧 fontbear](https://fontbear.net/)
- 発表準備

# 13回目
- [13回目の講義内容](docs/13_live.md)

## 前回の動画の目次
- [12回目の講義内容](docs/12_live.md)
- 前回の金曜日欠席の人
  - https://github.com/dat17/yoketoru を開く
  - 右の[Clone or Download]ボタンをクリックして、[Download ZIP]をクリックしてダウンロード
  - ダウンロードが完了したら、ファイルを開く
  - スタートメニューから、コンピュータを開いて、[ライブラリ]>[ドキュメント]>[パブリックのドキュメント]>[Unity17]フォルダーを開いておく
  - フォルダーが開くので、[yoketoru-master]フォルダーをドラッグして、上で開いた[Unity17]フォルダーにドロップしてコピー

以上で準備完了。Unityを開いて、[OPEN]をクリックして、[ライブラリ]>[ドキュメント]>[パブリックのドキュメント]>[Unity17]>[yoketoru-master]フォルダーを開く

## 補足
- [前回、講義中に開けなかったPhaserのシーン管理ドキュメント](https://github.com/am1tanaka/phaser-javascript/blob/master/StateMachine.md)

## 内容
- [今回の画面のライブ配信](https://www.youtube.com/watch?v=ON5X-LRJBQs)
- [Unityのよけとるの仕上げ](https://github.com/dat17/gp1/blob/master/docs/13-shiage.md)
- 夏休み企画

## 話題
- [染谷翔 スキルがない人のための企画アイディア出しのコツ](https://drive.google.com/file/d/0B7bGK4Tdb-GqZDM0UWRaOTZqdE0/view)
- [C#言語機能　もくもく+ＬＴ会](https://togebu.doorkeeper.jp/events/62479)
- [Unity3D Japan 【Unite 2017 Tokyo】Unityで楽しむノンフォトリアルな絵づくり講座：トゥーンシェーダー・マニアクス](https://www.youtube.com/watch?v=6aNB9LhSx7g)
- [学生時代に知っておきたかったWeb技術の学び方の学び方 | リブセンス](https://www.slideshare.net/livesense/web-49772012)

## 夏休みの課題：ミニゲームの開発
Unity、Phaserのいずれかで、ミニゲームを開発する。

- 完全なオリジナルでなくてもよい
  - 講義で作成したyoketoruを改造したもの
  - Webで見つけたチュートリアルを改造したもの
  - AssetStoreのプロジェクトを改造したもの
  - 書籍のサンプルを改造したもの
- yoketoruの場合、以下のような要素を追加してみよう
  - 障害物を作る
  - 弾を撃つ
  - 敵の動きのバリエーションを増やす
  - 演出(パーティクル)
  - 画面を綺麗にする
- チュートリアルの例
  - ひよこのたまご http://hiyotama.hatenablog.com/
  - Unityの公式 https://unity3d.com/jp/learn/tutorials
  - AssetStore https://www.assetstore.unity3d.com/jp/#!/search/page=1/sortby=popularity/query=price:0&category:98
  - 本棚の書籍

### 夏休み明け
夏休み明けに、以下の要領で発表会を行う。

- 一人5分～10分程度で発表
- 作品をネットドライブにコピーしておいて、教卓PCで実行して、解説
- 発表内容は以下の通り
  - 作品名
  - 作品の概要
  - 操作方法
  - ゲームのルール
  - どこを自分で開発したか
  - 利用したアセットやチュートリアルを、全て紹介
- 各内容については、 https://unityroom.com/ の作品を何本か確認して、どのように書けば分かりやすいかを研究して、工夫すること

---

# 12回目
## 前回の動画の目次
- [11回目の講義内容](docs/11_live.md)
- 前回のマウスなど
  - game.input.activePointerを使うと、マウスとスマホを共存できるかも

## 話題
- [unity道場 ゲーム開発者のためのタイポグラフィ講座](https://www.slideshare.net/UnityTechnologiesJapan/ss-77467062)

## 内容：Phaser版よけとるの開発
- [今回の画面のライブ配信](https://www.youtube.com/watch?v=eWYYoveeJ5U)
- [Phaserでシーン管理 state](https://github.com/am1tanaka/phaser-javascript/blob/master/StateManager.md)
- [シーン対応のプロジェクトをダウンロードして、Lubuntuに移動](https://github.com/am1tanaka/phaser-template-small)
  - 共有フォルダーに入れる
  - secoundフォルダーから、`_site`フォルダー内の`assets`フォルダーと`js/vendor`フォルダーを上書きコピーする
  - 共有フォルダー内のまま、作業
  - GitHubなどへの反映は、Windows側で行う
- ゲームの企画
  - ミニゲーム
    - yoketoru(UnityでもPhaser)を改造したもの(ルールを追加するなど)
      - 障害物を作る
      - 弾を撃つ
      - 敵の動きのバリエーションを増やす
      - 演出(パーティクル)
      - 画面を綺麗にする
    - あるいは、インターネット上にチュートリアル
      - ひよこのたまご http://hiyotama.hatenablog.com/
      - Unityの公式 https://unity3d.com/jp/learn/tutorials
      - AssetStore https://www.assetstore.unity3d.com/jp/#!/search/page=1/sortby=popularity/query=price:0&category:98
      - 本棚の書籍
    - 使ったアセットや参考にしたサイトの作者とURLをメモしておくこと
  - 何を改造、あるいは追加したのかを明確にする

# 11回目
## 前回の動画の目次
- [10回目の講義内容](docs/10_live.md)

## 内容
- [今回の画面のライブ配信](https://www.youtube.com/watch?v=jvhJIO3qAcI)
- [手順メモ](docs/11_memo.md)
  - プレイヤーがマウスをクリックした場所を目指すように変更
  - 星を全て取ったらclearと表示
  - 敵を追加
  - 敵にぶつかったらmissと表示
- Tyrano ScriptやUnity、Phaserで自分のキャラクターや背景を表示する

# 10回目
## 前回の動画の目次
- [9回目の講義内容](docs/09_live.md)

## 話題
- [Unity1週間ゲームジャム 3回目](https://unityroom.com/unity1weeks/4)
  - [田中の作品 Unite Star Dust!](https://unityroom.com/games/unite-star-dust)

## 参考URL
- [Phaser](http://phaser.io/docs/2.6.2/index)

## 内容
- [ライブ配信](https://www.youtube.com/embed/nFcjEF5DPqg)
- [Phaserでの乱数](https://github.com/am1tanaka/phaser-javascript/blob/master/Random.md)
- [複数のキャラクターを表示～for文～](https://github.com/am1tanaka/phaser-javascript/blob/master/Kurikaeshi.md)
- [グループ/当たり判定](http://am1tanaka.hatenablog.com/entry/2017/04/18/180408)
  - http://phaser.io/docs/2.4.4/Phaser.Group.html
- [前回の写真をイラスト調にするのをやり直す](http://otarunet.com/it/webdesign/photoshop-photo-suisai/)

# 9回目
## 前回の動画
- [8回目の講義内容](https://www.youtube.com/embed/gM2vFEWG_NE)

## 話題
- [バンダイナムコ VR ZONE SHINJUKU 7/14から](http://www.phileweb.com/news/d-av/201706/13/41416.html)

## 内容
- [ライブ配信](https://www.youtube.com/embed/ClfbhgLK4Cw)
- 前回の復習
  - secondを作成して、最初からやり直す
  - [メモ](docs/07_phaser01.md)
- マウスカーソルをdudeに追わせる
- キャラクター同士の当たり判定
- 立ち絵や背景の作成

### イラスト関連
- [Photoshop Illustrator 名人会 GIF, JPEG, PNGの違いを理解して軽くてきれいな画像を作ろう](http://photoshop-illustrator-meijinkai.info/photoshop-train/file-formats)
- [ティラノスクリプト 便利サイトリンク集](http://tyrano.jp/commu/link)
- [小樽総合デザイン事務局 初心者でもできる！写真をイラスト風に加工するチュートリアルまとめました：Photoshop](http://otarunet.com/it/webdesign/photoshop-photo-illustration/)
- [小樽総合デザイン事務局 Photoshop　5分でできる写真をドット絵風に加工する方法](http://otarunet.com/it/webdesign/photoshop-photo-dotto/)
- [面白法人KAYAC ドット絵描く楽な方法見つけた！気がする](http://design.kayac.com/topics/2012/02/post-47.php)
  - イラストをドット絵にする


# 8回目
## 話題
- [Unity Technologies Japan G.K. Unityインターハイ　ブログ](http://inter-high-blog.unity3d.jp/2017/06/05/blogopen/)
  - 企画の出し方など

## 内容
- [ライブ配信](https://www.youtube.com/embed/PAtsq8Ubye4) 右クリックして、新しいウィンドウで開く
- Lubuntuの修正
  - ログイン後に画面が黒くなったときの対処
    - Lubuntuを再起動して、すぐに右の[Shift]キーを押し続ける
    - 起動するOSの選択画面が表示されるので、[E]キーを押す
    - カーソルキーでカーソルを移動して、「linux」から始まる行を探して、行の最後に半角スペースを空けたあとに`nomodeset`を追加する
    - [Fn]+[F10]キーを押して、再起動
  - Guest Additions CDのインストール
    - Lubuntuが起動したら、[デバイス]メニューを選択して、[Guest Additions CD イメージの挿入]を選択
    - デスクトップに[VBOXADDITIONS_・・・]というアイコンが表示されて、[リムーバブルメディアの挿入]というウィンドウが表示されたら、[OK]をクリック
    - [VBoxLinuxAdditions.run]ファイルを右クリックして、[パスをコピーする]を選択
    - [スタート]メニューをクリックして、[実行]をクリック
    - `lxte`と入力して、LXTerminalを起動
    - `sudo`と入力したあとに、[スペース]キーを押してから、画面を右クリックして、[貼り付け]を選択して、[Enter]キーを押す
    - パスワードを入力して、[Enter]キーを押す
  - Phaserのシンプルプロジェクトの修正
    - 引き続き、LXTerminalで作業する
    - `cd ~/phaser/phaser-template-simple`と入力して、[Enter]キーを押して、パスを移動
    - `mv phaser-boilerplate ..`と入力して、[Enter]キーを押す
- [Phaser](http://phaser.io/docs/2.6.2/index)
  - [メモ](docs/07_phaser01.md)
  - プロジェクトのはじめ方
  - デバッグ文字の表示
  - 文字の表示
  - イメージの表示(自分で描いたdude.pngを表示する)
  - ArcadePhysicシステムによる移動
  - 画面内の跳ね返らせ方

## 時間があれば
- 立ち絵や背景の作成
  - Tyrano Scriptに組み込む

# 7回目
## 内容
- 作成したドット絵を、差し替えてPhaserで動かす
  - WindowsとLubuntuでデータをやり取りする時は、zip圧縮する
  - [ドット絵の読み込ませ方](docs/06_phaser-sprite.md)
- [Tiled](http://www.mapeditor.org/)
  - フリーでも使えるタイルマップエディター
  - starstruckのマップを見る
  - 自分のマップを作成して、Phaserに読み込ませる
  - LubuntuでWebブラウザーを起動して、Tiledで検索
  - ダウンロードしたら、展開して、Tiledを起動

# 6回目
## 話題
- https://unityroom.com/unity1weeks/3
- [田中作品](https://unityroom.com/games/teacup-bwl)

## 内容
- Phaserの開発環境をローカルで整える(VirtualBox)
  - 先週、Phaserのインストールまで終わらせて、状態を保存した。その続き
  - 画面の解像度を適正にする
  - ホストOS(Windows)からゲストOS(Lubuntu)のHTTPサーバーにアクセス
    - 参考URL http://the2g.com/75
    - アクセス許可が必要だったので、Lubuntuで行う
- [2Dグラフィック(2)](docs/05_dot.md)
  - [Photoshopでアニメーション](https://helpx.adobe.com/jp/photoshop/kb/5784.html)
    - ダウンロードフォルダーに保存した dude.psd を読み込んで再開
    - アニメのフレームの設定操作が途中でわからなくなったのでその確認から
      - ビデオタイムラインにしていたのが原因と思われる
      - タイムラインパネルを表示したら、右上の四本線のアイコンをクリックして、タイムラインを削除を選択
      - タイムラインパネルの中心にコンボボックスが表示されるので、[フレームアニメーションを作成]になっていたらクリック、[ビデオタイムラインを作成]になっていたら、右の下矢印ボタンをクリックして、フレームアニメーションを作成に変更して、そのボタンを押す
      - ここから先は、ドキュメントの通り
      - Web用に保存は、[ファイル]>[書き出し]メニューにある。左下の[プレビュー]ボタンで、事前にアニメを確認できる
    - Phaserのdude.pngを書き換えて、Phaserでアニメーションをさせてみる

# 5回目
## 話題
- [テラシュールブログ 【Unity】1週間ゲームジャムに参加しました。メイキング・オブ・超速ブロック崩し（仮）](http://tsubakit1.hateblo.jp/entry/2017/05/01/230531)
- [技術用語の発音](http://webrocketsmagazine.com/entry/20111201/what-do-you-read-css-property.html)
- [BuzzFeed Japan. 京都大学の入学式の式辞の顛末](https://headlines.yahoo.co.jp/hl?a=20170519-00010003-bfj-soci)
- [ITmedia ソースコードまで酷似　「堀江貴文プロデュース」アイドルサイトに盗用多数　運営者が謝罪](http://www.itmedia.co.jp/news/articles/1705/22/news063.html)
- [有賀正博 NAVERまとめのライターに無断転載の損害賠償を支払っていただいた件](https://www.photo-yatra.tokyo/blog/archives/12696)

## 内容
- Phaserの開発環境をローカルで整える(VirtualBox)
  - VirtualBoxで開発環境を構築
    - ダウンロードフォルダーにコピーしたisoファイルを仮想CDに設定
    - 仮想PCを起動して、lubuntu 16.04(64bit) をインストール
    - [インストールスクリプトをダウンロードして、インストール](https://github.com/am1tanaka/10k-gamedev/)
    - Phaserの動作確認
- Phaserを学ぶ(1)～公式チュートリアル～
  - キャラクターのパターンを確認する
- [2Dグラフィック](docs/05_dot.md)

# 4回目
## 内容
- [著作権概論](docs/04_license.md)を右クリックして、新しいタブで開く
  - 開いたページで[Raw]ボタンをクリック
  - [Ctrl]+[A]キーで全て選択したら、コピー([Ctrl]+[C]キー)
  - 自分のアカウントに戻る
  - designというリポジトリーを作成
  - 04_license.md というファイルを create
  - 先ほどコピーした文章を貼り付ける
  - Commitする
  - README.md にリンクを作成する
- Phaserの開発環境をローカルで整える(VirtualBox)
  - BIOS設定
    - 再起動して、[Fn]+[F1]と[Fn]+[F2]を何度か押して、BIOSを起動
    - AdvancedSettingのIntel Virtualization technologyをEnableにする
    - [Fn]+[F10]を押して、[Enter]キーで保存
  - VirtualBoxで仮想PC作成
  - Lubuntu16.04(64bit)をダウンロードフォルダーにコピー

# 3回目
## 話題
- [テラシュールブログ Unity2017](http://tsubakit1.hateblo.jp/entry/2017/05/08/224037)
- [東京インディーフェス2017](http://www.tokyosandbox.com/tokyo-indie-fest/)
- [F1-Gate マクラーレン、F1シミュレータードライバーを賭けたゲーム大会を開催](https://f1-gate.com/mclaren/f1_36286.html)

## 作業
- ゲームデザイン概論と企画書の書き方
  - シート2をソートして、ジャンルを決める
  - ５つの要素と、ジャンルを組み合わせてゲームを考えて、ゲームを企画する
- 企画案の提出

### 企画
- ゲームのコア 1～2行でゲームの要素
- ゲーム画面
- フィーチャーセット(あれば)
- 操作方法
- ゲームオーバー条件（あれば）
- 得点方法（あれば）
- 登場するもの（オブジェクト）リスト

# 2回目
## 話題
- https://unite.unity.com/ja/2017/tokyo

## 概要
- e-typingの練習2回目
  - しばらくやって、今日の最高スコアをGoogleスプレッドシートのC列の自分の出席番号の行に書き込む
- [Phaserを続きから](http://am1tanaka.hatenablog.com/entry/2017/04/18/141813)
- [Tyrano Script](docs/02_tyrano.md)

# 1回目
- ガイダンス
- [アカウントの登録](docs/01.md)
  - Gmail / Microsoft Account / GitHub / e-typing
- e-typingでキータッチの練習
- [HTML5ゲームエンジン Phaserを試す](http://am1tanaka.hatenablog.com/entry/2017/04/19/211234)

## 終わったこと
- Gmail, Microsoftアカウント, GitHub, e-typingの登録(1名金曜日に)
- Phaserの最初をやって、保存して、Gmailに下書き保存

# 参考URL
- [Phaserをサンドボックスで試すチュートリアル](http://am1tanaka.hatenablog.com/entry/2017/04/19/211234)
- [Phaser](https://phaser.io)
- [https://www.e-typing.ne.jp/](e-typing)
- [Tiled](http://www.mapeditor.org/)
