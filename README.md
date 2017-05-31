# ゲームデザイン実習
2017年度 デジタルアーツ東京 ゲームデザイン実習用リポジトリー。

本講義で利用するリポジトリーはこちら > https://github.com/datgd171/

# 講義予定
- [シラバス](syllabus.md)

# 6回目
## 話題
- https://unityroom.com/unity1weeks/3
- [田中作品](https://unityroom.com/games/teacup-bwl)

## 予定
- Phaserの開発環境をローカルで整える(VirtualBox)
  - 先週、Phaserのインストールまで終わらせて、状態を保存した。その続き
  - 画面の解像度を適正にする
  - ホストOS(Windows)からゲストOS(Lubuntu)のHTTPサーバーにアクセス
    - 参考URL http://the2g.com/75
  - 作成は Lubuntu、確認はWindows
- [2Dグラフィック(2)](05_dot.md)
  - [Photoshopでアニメーション](https://helpx.adobe.com/jp/photoshop/kb/5784.html)
    - ダウンロードフォルダーに保存した dude.psd を読み込んで再開
    - アニメのフレームの設定操作が途中でわからなくなったのでその確認から
      - ビデオタイムラインにしていたのが原因と思われる
      - タイムラインパネルを表示したら、右上の四本線のアイコンをクリックして、タイムラインを削除を選択
      - タイムラインパネルの中心にコンボボックスが表示されるので、[フレームアニメーションを作成]になっていたらクリック、[ビデオタイムラインを作成]になっていたら、右の下矢印ボタンをクリックして、フレームアニメーションを作成に変更して、そのボタンを押す
      - ここから先は、ドキュメントの通り
      - Web用に保存は、[ファイル]>[書き出し]メニューにある。左下の[プレビュー]ボタンで、事前にアニメを確認できる
    - Phaserのdude.pngを書き換えて、Phaserでアニメーションをさせてみる
  - [Tiled](http://www.mapeditor.org/)
    - フリーでも使えるタイルマップエディター
    - starstruckのマップを見る
    - 自分のマップを作成して、Phaserに読み込ませる

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
- [2Dグラフィック](05_dot.md)

# 4回目
## 内容
- [著作権概論](04_license.md)を右クリックして、新しいタブで開く
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
- [Tyrano Script](02_tyrano.md)

# 1回目
- ガイダンス
- [アカウントの登録](01.md)
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
