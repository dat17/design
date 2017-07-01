# 10回目デスクトップ動画目次
## Phaser前回の確認
- https://youtu.be/nFcjEF5DPqg?t=13m23s

## Phaserで乱数を求める
- https://youtu.be/nFcjEF5DPqg?t=23m50s
- `game.rnd.integerInRange(最小値, 最大値);`で、最小値～最大値(どちらも指定の値含む)の正数値を返す
- `game.rnd.realInRange(最小値, 最大値);`で、最小値～最大値(最大値は含まない)の実数値を返す
- `game.rnd.pick([データをコンマ区切り]);`で、コンマ区切りした中から一つを返す
- 演習：ランダムで出現場所と移動速度を求める https://youtu.be/nFcjEF5DPqg?t=36m11s
  - 解答 https://youtu.be/nFcjEF5DPqg?t=40m12s
- じゃんけんの作り方考察 https://youtu.be/nFcjEF5DPqg?t=43m56s

## Phaserの繰り返し

https://youtu.be/nFcjEF5DPqg?t=48m48s

- 星を3つにしてみる https://youtu.be/nFcjEF5DPqg?t=49m10s
  - この方法で、動きなどにも対応するのは大変！
- JavaScriptのfor文 https://youtu.be/nFcjEF5DPqg?t=53m12s
- 10回繰り返す例文 https://youtu.be/nFcjEF5DPqg?t=58m1s
  - 0から数えることに慣れよう
- 星を10個作る https://youtu.be/nFcjEF5DPqg?t=1h2m1s
  - JavaScriptの配列は、予め個数を宣言する必要がない `var stars = [];`などでよい
  - 追加するときは`stars.push(データ);`で、最後尾に追加される
  - 配列にしたので、`star`の部分を全て書き換える必要がある https://youtu.be/nFcjEF5DPqg?t=1h6m23s
  - forに入れる https://youtu.be/nFcjEF5DPqg?t=1h14m16s
  - 100個にする https://youtu.be/nFcjEF5DPqg?t=1h15m23s
    - JavaScriptの配列は、予め個数を宣言する必要がないので、繰り返しを増やすだけで、数を増やすことができて楽
    - C#ではList<>型を使うと同様のことができる
- foreach文 https://youtu.be/nFcjEF5DPqg?t=1h23m12s
  - 回数を指示するのではなく、データの数だけ自動的に繰り返してくれる
  - マウスで取れるようにする https://youtu.be/nFcjEF5DPqg?t=1h39m28s

## グループ
UnityでLayerに該当するもの。

https://youtu.be/nFcjEF5DPqg?t=1h46m51s

- 配列からグループの宣言に変更 https://youtu.be/nFcjEF5DPqg?t=1h48m0s
- `stars = game.add.group()`でグループを作って、ゲームに追加。グループを操作するためのインスタンスを`stars`に代入 https://youtu.be/nFcjEF5DPqg?t=1h50m13s
- `stars.enableBody = true;`で、グループの物理挙動を有効にする
- `let star = stars.create(X, Y, 'スプライト名');`で、`stars`グループの指定座標にスプライトを追加して、そのハンドルを一時変数の`star`に代入
  - https://youtu.be/nFcjEF5DPqg?t=1h54m58s
- foreachをコメントアウトして、for文で処理。配列は不要になったので、インデックスを削除
- 個別に設定してた物理挙動の有効設定(`game.physics.arcade.enable(star[i]);`)を削除(動画では`physics`の綴りを間違えているので注意！)
- 更新処理(update.js)を一旦、コメントアウトしてエラーを出さないようにして、実行をチェック https://youtu.be/nFcjEF5DPqg?t=1h58m4s
- update.jsをグループに対応 https://youtu.be/nFcjEF5DPqg?t=2h9m19s 
  - `dude`と`stars`グループを接触設定。これで、dudeにぶつかった星が、跳ね返るようになる https://youtu.be/nFcjEF5DPqg?t=2h9m27s
  - 衝突時に関数を呼び出させる設定 https://youtu.be/nFcjEF5DPqg?t=2h15m45s
    - `game.physics.arcade.overlap(対象1, 対象2, 呼び出す関数, 呼び出し前のチェック(nullにすると、接触していたら無条件で呼び出す), 呼び出し関数内のthis(通常、thisでよい);`
  - 衝突時に呼び出す関数`pickStar`を作る https://youtu.be/nFcjEF5DPqg?t=2h18m15s

グループを使うことで、いくつかの初期化が楽になり、updateでは繰り返しが不要になった。

## 写真をイラスト風にするチュートリアル

https://youtu.be/nFcjEF5DPqg?t=2h28m44s

- 作成した背景を、ティラノスクリプトに読み込む　https://youtu.be/nFcjEF5DPqg?t=2h58m35s
- キャラクターを表示 https://youtu.be/nFcjEF5DPqg?t=3h5m20s

