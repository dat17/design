# 12回目デスクトップ動画目次
- https://www.youtube.com/watch?v=eWYYoveeJ5U

## Phaser前回の確認
- https://youtu.be/eWYYoveeJ5U?t=3m19s
  - ~/phaser/second が HTTPサーバーで起動していなければ、 `npm run serve`で起動して、Webブラウザーで確認する
  - 星とdroidが動く
  - 星と接触すると、星をとり、全て取り終えたら"clear"と表示
  - droidに接触すると、"gameover"と表示
  - 状態を１つしか持たない仕組みで作ったので、クリアーとゲームオーバーに移行できない。状態を持たせる

## 状態遷移を実装したプロジェクトのセットアップ
- プロジェクトのリポジトリーを開く https://youtu.be/eWYYoveeJ5U?t=8m13s
- リポジトリーをダウンロードする https://youtu.be/eWYYoveeJ5U?t=9m8s
- ダウンロードしたzipフィルを開く https://youtu.be/eWYYoveeJ5U?t=9m58s
- Lubuntuの共有フォルダーにドラッグ＆ドロップ
- フォルダー名を `phaser-template-small-master`から`phaser-template-small`に変更
- GitHubのプロジェクトを作成して、Publishする https://youtu.be/eWYYoveeJ5U?t=13m36s
- secondから必要なデータ(`assets`フォルダーと`_site/js/vendor`フォルダー)をコピー https://youtu.be/eWYYoveeJ5U?t=23m27s

## プロジェクトを開く
- 作業用のフォルダーを開く https://youtu.be/eWYYoveeJ5U?t=29m29s
- Atomでフォルダーを開いて、Webブラウザーで起動する https://youtu.be/eWYYoveeJ5U?t=33m35s
- デベロッパーツール(開発者ツール)を開く https://youtu.be/eWYYoveeJ5U?t=35m26s

## エラーの直し方
- エラーが発生したファイルと行を確認 https://youtu.be/eWYYoveeJ5U?t=35m54s
- エラー箇所を確認
  - `game`にすべきところを、`this`になっていたので修正
- バグを直した状態をコミット https://youtu.be/eWYYoveeJ5U?t=1h22m45s

## 以前作成したよけとるを移植
- `preload`を移植 https://youtu.be/eWYYoveeJ5U?t=1h24m29s
- `game`はグローバルじゃなくなったので、`this`に変更 https://youtu.be/eWYYoveeJ5U?t=1h26m49s
- `create`を移植 https://youtu.be/eWYYoveeJ5U?t=1h39m14s
  - 変数を定義 https://youtu.be/eWYYoveeJ5U?t=1h40m24s
  - グループの作成 https://youtu.be/eWYYoveeJ5U?t=1h44m27s
  - 星を数えるカウンター変数の定義と初期化 https://youtu.be/eWYYoveeJ5U?t=1h46m56s
  - 物理エンジンを設定 https://youtu.be/eWYYoveeJ5U?t=1h48m29s
  - 星の生成はあとで繰り返しで作り直すので削除 https://youtu.be/eWYYoveeJ5U?t=1h51m23s
  - いったん、ここで`star`をコメントアウトしたり、削除して、プログラムを動かして、バグがないか確認 https://youtu.be/eWYYoveeJ5U?t=1h57m51s
  - 星の作成をコピー https://youtu.be/eWYYoveeJ5U?t=1h59m53s
  - 星が沢山表示されるようになる
  - dudeを移植 https://youtu.be/eWYYoveeJ5U?t=2h11m35s
  - dudeを画面中心に出現 https://youtu.be/eWYYoveeJ5U?t=2h14m3s
- `update`を移植 https://youtu.be/eWYYoveeJ5U?t=2h22m5s
  - コメントアウトしたStarの行を復帰して、dudeに書き換える https://youtu.be/eWYYoveeJ5U?t=2h24m43s
  - 当たり判定 https://youtu.be/eWYYoveeJ5U?t=2h28m25s
  - 星と重なった時の処理`pickStar`の作成 https://youtu.be/eWYYoveeJ5U?t=2h31m2s
  - 星の数をカウントアップする式に間違いがあったので修正 https://youtu.be/eWYYoveeJ5U?t=2h34m51s
- Clear時の挙動
  - 物理エンジンを停止 https://youtu.be/eWYYoveeJ5U?t=2h39m19s
- 星を取ったらスコア加算 https://youtu.be/eWYYoveeJ5U?t=2h42m21s
- GitHubにコミットしてsync https://youtu.be/eWYYoveeJ5U?t=2h47m10s

## 予告
- 夏休みの課題に向けて https://youtu.be/eWYYoveeJ5U?t=2h52m42s

