# 9回目 デスクトップ動画

- Lubuntuの更新(基本的に毎回行う)
https://youtu.be/ClfbhgLK4Cw?t=5m00s
- Guest Additions CDの取り出し
https://youtu.be/ClfbhgLK4Cw?t=7m00s
- LXTerminalの起動
https://youtu.be/ClfbhgLK4Cw?t=8m03s
- 端末(LXTerminal)の操作
https://youtu.be/ClfbhgLK4Cw?t=10m32s
  - ディレクトリー一覧表示 `ls`
  - カレントディレクトリー移動 `cd フォルダー名`
- 前回作成したプロジェクト first を見る
https://youtu.be/ClfbhgLK4Cw?t=14m03s
  - Atomエディターの起動
  - HTTPサーバーとブラウザーの起動
  - HTTPサーバーの停止([Ctrl]+[X]キー)
- 新しいPhaserプロジェクトSecondを作成
https://youtu.be/ClfbhgLK4Cw?t=19m26s
- Webブラウザーのハード読み込みをしないと、前のプログラムが実行されるので注意

## 前回の復習
- 星を表示する座標を変更する(`game.load.image`)
https://youtu.be/ClfbhgLK4Cw?t=33m11s
- 複数のキャラクターのシートを利用する(`game.load.spritesheet`)
https://youtu.be/ClfbhgLK4Cw?t=35m25s
- アニメーション
https://youtu.be/ClfbhgLK4Cw?t=48m00s
- エラーの探し方
https://youtu.be/ClfbhgLK4Cw?t=57m53s
- Tabの字下げ文字数を4文字に設定
https://youtu.be/ClfbhgLK4Cw?t=1h5m50s
- updateで自前でキャラクターを移動させる
https://youtu.be/ClfbhgLK4Cw?t=1h7m50s
- 物理エンジンを使った移動
https://youtu.be/ClfbhgLK4Cw?t=1h11m19s
  - Arcade物理エンジンをスプライトで有効にする
  - スプライトのbodyプロパティーで速度や弾性係数を設定
  - 画面外で跳ね返るように設定(`dude.body.collideWorldBounds = true;`)

## プレイヤーと星の衝突
https://youtu.be/ClfbhgLK4Cw?t=1h24m20s
- 物理エンジンを星で有効にする
- dudeとstarが衝突する設定を行う `game.physics.arcade.collide(dude, star);`
- 星を跳ね返らせるために弾性係数を設定
- 衝突をifで判定する
https://youtu.be/ClfbhgLK4Cw?t=1h53m

## マウスの座標を読み取る
https://youtu.be/ClfbhgLK4Cw?t=1h56m14s
- `game.input.x`と`game.input.y`で確認できる
- マウスの場所にdudeを表示
https://youtu.be/ClfbhgLK4Cw?t=2h0m20s
- マウスのカーソルがキャラクターの中心をポイントするようにする(anchor)
https://youtu.be/ClfbhgLK4Cw?t=2h9m05s
- マウスカーソルがキャラクターに重なったことを判定する
https://youtu.be/ClfbhgLK4Cw?t=2h17m
  - `キャラクター.inputEnabled = true;`　を設定
  - `キャラクター.input.pointerOver()` で判定
  - `キャラクター.kill();` でキャラクターを削除
  - `キャラクター.visible = false;` でキャラクターを非表示

# 話題
- バンダイナムコのVR施設
https://youtu.be/ClfbhgLK4Cw?t=2h30m50s
- リクルートのキャプチャーやVR機器の提供
https://youtu.be/ClfbhgLK4Cw?t=2h34m30s

# グラフィック
- 画像フォーマットの復習
https://youtu.be/ClfbhgLK4Cw?t=2h37m28s
- 画像素材のリンク紹介と、立ち絵や背景のピクセル数
https://youtu.be/ClfbhgLK4Cw?t=2h41m28s
- 写真をイラスト的にするチュートリアル
https://youtu.be/ClfbhgLK4Cw?t=2h50m47s
