# 11回目デスクトップ動画目次
- https://www.youtube.com/watch?v=jvhJIO3qAcI

## Phaser前回の確認
- https://youtu.be/jvhJIO3qAcI?t=5m32s
  - 乱数で星の座標と速度を変化させる
  - for文で沢山の星を登録
  - グループでまとめる
  - 画面を跳ね返らせる

## クリックした場所を目指してプレイヤーを移動させる
情報を自力で探す練習。

- https://youtu.be/jvhJIO3qAcI?t=8m26s
- PhaserのAPIリファレンスマニュアル https://youtu.be/jvhJIO3qAcI?t=9m7s
- Phaserのサンプル https://youtu.be/jvhJIO3qAcI?t=9m57s
- 見つけたサンプルをGistにコピー＆ペーストして、やっている内容を調べてコメントを書く https://youtu.be/jvhJIO3qAcI?t=17m7s
- 英文のページを和訳する https://youtu.be/jvhJIO3qAcI?t=28m16s
- 作業例 https://youtu.be/jvhJIO3qAcI?t=29m36s
  - アニメサンプルの一つで作業の内容を例示
  - 変数に代入されているのが何なのかをAPIリファレンスで調べる
  - 何かが分かったら、そのメンバー(member)プロパティーやメソッドから、使われているものを探して、引数や効果、戻り値を確認
  - 以上に基づいて、各行が何をしているのかを推定して、コメントを書く
  - コメント例 https://youtu.be/jvhJIO3qAcI?t=46m43s
- Gistの保存の仕方 https://youtu.be/jvhJIO3qAcI?t=1h2m7s
  - Description、ファイル名の順に上から並んでいるので入力して、右下の[Create Public gist]をクリック
- 調べがついたら、自分で調べた知識を基にして、追いかけるように改造する https://youtu.be/jvhJIO3qAcI?t=1h5m9s
- 英語の調べ方の例 https://youtu.be/jvhJIO3qAcI?t=1h8m28s
  - Chromeの右クリックで検索
  - Weblioを使う
- 実装後の動作例 https://youtu.be/jvhJIO3qAcI?t=1h11m59s

>> このあと、 1時間40分ぐらいまで、AtomのプラグインでGitHubに登録できないかを調べていた。結局、Windowsにファイルを共有して、Windows側でGitHub pagesに登録することにした。

## 作成したプログラムをスマートフォンで動かす
GitHubのサービスである`GitHub Pages`を使うと、Webページを公開することができる。Phaserで作成したデータをGitHub Pagesで公開すれば、スマートフォンで動作を確認できる。

- デスクトップにあるWindowsと共有しているフォルダーを開いて、必要なフォルダーをコピーする https://youtu.be/jvhJIO3qAcI?t=1h43m23s
  - ~/phaser/secondフォルダーをコピー
  - Windowsに切り替える
- Windows側で、Lubuntuとの共有フォルダーを開く https://youtu.be/jvhJIO3qAcI?t=1h50m19s
  - ドキュメント>自分の苗字のフォルダー>lubuntu
- もう一つエクスプローラーを開いて、コピー先を開く https://youtu.be/jvhJIO3qAcI?t=1h50m58s
- コピー https://youtu.be/jvhJIO3qAcI?t=1h51m17s
  - .gitフォルダーを削除
- GitHubにsecondを登録する https://youtu.be/jvhJIO3qAcI?t=1h54m33s
  - コミットして、Publishする
- アップロードした先をWebブラウザーで開く https://youtu.be/jvhJIO3qAcI?t=2h33s
- GitHub Pagesの登録　https://youtu.be/jvhJIO3qAcI?t=2h2m17s
- 登録が完了したら、設定の上にWebページのURLが表示される。これを開くと、ページが確認できる https://youtu.be/jvhJIO3qAcI?t=2h5m29
  - 見つからない。通常に公開するだけだと、プロジェクト直下のHTMLのみがWebページとして認識される
  - docsフォルダーを公開することにして、_siteフォルダーをリネームする
- `_site`フォルダーの名前を`docs`に変更 https://youtu.be/jvhJIO3qAcI?t=2h10m42s
  - GitHub DesktopでコミットしてSync
- GitHub Pagesの設定を変更 https://youtu.be/jvhJIO3qAcI?t=2h11m11s
  - 実行できるようになった。キャラクターが表示されなくなったので、設定をする
- `preload`に、読み込みもとの設定を追加して、パスを変更する https://youtu.be/jvhJIO3qAcI?t=2h20m40s
  - 変更したら保存して、コミットしてSync
  - Webブラウザーはキャッシュの削除とハード再読み込み https://youtu.be/jvhJIO3qAcI?t=2h26m
- このままではスマートフォンで操作が反映しなかったので、`pointer1`の`isDown`を追加 https://youtu.be/jvhJIO3qAcI?t=2h34m52s
  - GitHubにアップロードしたので、Webブラウザー上で直接プログラムを書き換えれば、すぐにスマートフォンの動作にも反映できる
  - この時点でのソースコードは、サンプルの`player`を`dude`に書き換えてなく、エラーが発生したためにスマートフォンに反映していなかった。修正が必要

## 星の数を数える
- https://youtu.be/jvhJIO3qAcI?t=2h43m55s
- 数える変数を`stars`グループに追加 https://youtu.be/jvhJIO3qAcI?t=2h47m3s
- 星を作るループ内でカウントアップ https://youtu.be/jvhJIO3qAcI?t=2h48m32s
- 星を取った処理の中で、カウントダウンと、0になったときの処理 https://youtu.be/jvhJIO3qAcI?t=2h51m55s

## 敵を出す
- 星を参考に作業をする https://youtu.be/jvhJIO3qAcI?t=2h56m23s


# まとめ
- この講義では、ただ写すのではなく、自分で調べて、考えて、サンプルを利用する練習をした
- 完成しなかった場合は、改めて動画を振り返って、作業をして、理解を深めておくこと
- 次回からは新しいプロジェクトを作成するので、今回のものが完成していなくても今後の作業に支障は出ない
