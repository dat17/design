# 13回目デスクトップ動画目次
- https://www.youtube.com/watch?v=ON5X-LRJBQs

## Unityの仕上げ。金曜日の振り返り
- https://youtu.be/ON5X-LRJBQs?t=1m34s

## Unityで画面が暗くなる症状の解消
- 状況の確認 https://youtu.be/ON5X-LRJBQs?t=2m21s
- 原因の確認 https://youtu.be/ON5X-LRJBQs?t=31m8s
  - Unityは、Lightから直接あたる光以外に、グローバルイルミネーション(大域照明=GI)で照らされている
  - GIとは、大気による光の拡散や、周囲のものからの反射光など、間接的に届く光のこと
    - 光源であるDirectionalLightを消しても、GIが有効で、SkyBoxなどの影響を受けて真っ暗にはならない https://youtu.be/ON5X-LRJBQs?t=37m44s
  - GIは、様々な要素が影響するため、まじめに計算するのは大変なので、リアルタイムCGでは、予めおおよその光を計算しておいて、それをライティングに利用する
  - 計算には時間が多少かかるので、光やオブジェクトを変更するごとに毎回計算しなおしていては操作性が下がるため、Unityの編集中は、簡易な計算をしておいて、結果をキャッシュに入れて代用している
  - シーンが切り替わると、このキャッシュが破棄されるので、GIのデータがなくなり、その分、暗くなってしまう
    - DirectionalLightを無効にすると、最初はGIキャッシュが有効なのでオブジェクトは真っ黒にならないが、シーンが切り替わってキャッシュがクリアされると、オブジェクトが光を全く受けなくなり、黒くなる https://youtu.be/ON5X-LRJBQs?t=39m7s
- 解決策 https://youtu.be/ON5X-LRJBQs?t=40m4s
  - [Windows]メニューから[Lighting]を選択
  - ウィンドウ下の[Auto]のチェックを外して、GIキャッシュの自動生成を停止して、[Build]ボタンを押して、GIデータを生成する https://youtu.be/ON5X-LRJBQs?t=43m13s
  - 計算結果は、シーンと同じ場所にフォルダーが作られて、保存される https://youtu.be/ON5X-LRJBQs?t=44m14s
- 解決 https://youtu.be/ON5X-LRJBQs?t=44m36s
  - なお、これはUnityで開発中の症状。ビルドする時にGIデータは計算されるので、実行ファイルではこの症状は起きない

## ゲームオーバーやクリア時に動きを停止する
- https://youtu.be/ON5X-LRJBQs?t=48m38s
- `Time.timeScale` で、ゲーム中に流れる時間の速さを変えられる。スローモーションにしたり、早回しをするなどの演出に利用できる。これに`0`を設定して、時間を止める
- 実装 https://youtu.be/ON5X-LRJBQs?t=53m23s
  - ゲームからの状態遷移は、ゲームオーバーかクリアしかない。どちらもゲームを停止したいので、変更時に時間を停止させる
- ゲーム開始時に時間の流れを設定 https://youtu.be/ON5X-LRJBQs?t=58m13s
  - 上記のままでは、次にゲームを開始した時に時間が止まったままになるので、ゲームやタイトルの開始時などに、時間の経過を`1`に戻しておく

## アイテムを敵を出現させるオブジェクト Spawner(スポーナー)を作成する
ランダムで出現させるだけでは、細かい面作りができず、バランスの調整が難しい。キャラクターをタイミングや場所によって出現させる場合、単体であればエディター上で直接配置することもできるが、編隊を登場させたい場合や、出現座標や動きにランダム性を加えたい場合などは、キャラクターを出現させるためのオブジェクトを作って配置するとよい。

- https://youtu.be/ON5X-LRJBQs?t=59m52s
- Gizmoの説明 https://youtu.be/ON5X-LRJBQs?t=1h5m2s
  - 編集を支援するためのデバッグ表示機能
  - カメラのアイコンや、視界の範囲を線で表示しているのがGizmoで、自分で描画することが可能
  - 今回、出現範囲の`Bounds`を描画する

まずは`Spawner`オブジェクトを作成する。

- Spawnerのゲームオブジェクトを作成 https://youtu.be/ON5X-LRJBQs?t=1h6m3s
- Spawnerの座標を`0,0,0`にしておく https://youtu.be/ON5X-LRJBQs?t=1h6m33s
- スクリプトを作成 https://youtu.be/ON5X-LRJBQs?t=1h7m17s
- スクリプトを開いて、必要な変数を定義 https://youtu.be/ON5X-LRJBQs?t=1h8m12s
- Gizmoの描画 https://youtu.be/ON5X-LRJBQs?t=1h11m55s
  - UnityEditorで設定された出現範囲の`Bounds`をループで確認して、`center`と`size`で矩形を描画
- 出現させるプレハブを設定 https://youtu.be/ON5X-LRJBQs?t=1h15m43s
- 目印の枠を表示 https://youtu.be/ON5X-LRJBQs?t=1h17m57s
- 出現範囲の`Bounds`を設定 https://youtu.be/ON5X-LRJBQs?t=1h18m38s
- `GameManager`に実装していた敵やアイテムを出現させる処理は不要になったので、コメントアウト https://youtu.be/ON5X-LRJBQs?t=1h23m16s
- キャラクターに設定されている`MoveBall`スクリプトの出現座標と速度をランダムに設定する処理も不要になったのでコメントアウト https://youtu.be/ON5X-LRJBQs?t=1h24m27s

---
休憩
---

指定した範囲内にランダムで出現させる。

- 指定の個数、指定のプレハブを、指定の設定範囲内に出現させる https://youtu.be/ON5X-LRJBQs?t=1h38m51s
  - `Spawner`スクリプトの`Start`メソッドにコードを書く
  - `SpawnCount`の数だけ`for`文でループ
  - どの`Bounds`に出現させるかを乱数を求めて、`idx`に入れる
  - `idx`番目の範囲で乱数を作成して、`Instantiate()`で出現させる
- 動作確認 https://youtu.be/ON5X-LRJBQs?t=1h51m37s

### cos、sinを使う
速度を求める。

- 速度の求め方 https://youtu.be/ON5X-LRJBQs?t=1h52m33s
  - cosとsinを使って、ランダムな方向の、指定の長さのベクトルを求める
- 実装 https://youtu.be/ON5X-LRJBQs?t=2h2m27s
　　- 乱数で角度を`theta`に代入。単位はラジアン
  - 速さを求める
  - `theta`ラジアンの方向で、長さ`len`のベクトルを`vel`に求める
  - `Rigidbody`を取得して、`velocity`に`vel`を代入することで、速度の設定完了
- 動作確認 https://youtu.be/ON5X-LRJBQs?t=2h13m36s

## 跳ね返らなくなるボールを修正
しばらく見ていると、ボールが跳ね返らずに、壁に張り付いていく。Rigidbodyには、一定速度以下の跳ね返りを無視する設定がある。細かく跳ねてしまい、バウンドが収まらないことへの対策だが、今回はこの動きは要らない。

- 状況の確認 https://youtu.be/ON5X-LRJBQs?t=2h14m41s
- Physicsの設定で調整する https://youtu.be/ON5X-LRJBQs?t=2h15m2s
- Bounce Threshold(バウンドのいき値)を0にする https://youtu.be/ON5X-LRJBQs?t=2h17m7s

## アイテムを出現させる
Spawnerが完成したので、プレハブ化してから、アイテムを出現させるオブジェクトを作る。

- プレハブを作る https://youtu.be/ON5X-LRJBQs?t=2h19m6s
- プレハブから、新しいSpawnerを作る https://youtu.be/ON5X-LRJBQs?t=2h19m24s
- アイテムに設定を変更 https://youtu.be/ON5X-LRJBQs?t=2h19m49s
  - プレハブをアイテムにする
  - 出現数や、速度を調整
  
## プレイヤーを画面外に出ないように調整
プレイヤーのコライダーには`IsTrigger`が設定されているので、衝突で画面外に行くのを防ぐことはできない。プログラムで移動範囲を制限する。

- https://youtu.be/ON5X-LRJBQs?t=2h25m36s
  - 移動時に求めた移動先の座標の変数に対して、画面外に出ないような処理を加える
- `if`文は使わず、`Mathf.Clamp()`を使う https://youtu.be/ON5X-LRJBQs?t=2h28m44s
- 移動範囲を`Bounds`で設定する https://youtu.be/ON5X-LRJBQs?t=2h30m26s
- `Clamp`を使って、プレイヤーの座標を指定した`Bounds`内にする https://youtu.be/ON5X-LRJBQs?t=2h31m57s
- `Bounds`を設定 https://youtu.be/ON5X-LRJBQs?t=2h34m59s

## GitHub Desktopの古い方を使う
GitHub Desktopは新しいバージョンが提示されているが、リポジトリーの一覧が表示されないなど使い勝手が必ずしもよいとはいえない。以前の方がいい場合は、ページの下の方からまだダウンロードできる。

https://youtu.be/ON5X-LRJBQs?t=2h48m48s

ひとまず完成ということでコミット。 https://youtu.be/ON5X-LRJBQs?t=2h50m43s

## キャラクターの差し替え
仮作りしていたプリミティブ図形をモデルに差し替える。

- https://youtu.be/ON5X-LRJBQs?t=2h54m29s
- 2階層以上で構成する
  - 親は動きを司る。操作スクリプト、当たり判定、Rigidbodyなどを設定
  - 子供にモデルデータを配置する
    - モデルデータやアニメーションは、向き、座標、大きさなど、ゲーム空間に合致していない場合が多い
    - それを親のオブジェクトとで調整してしまうと、モデルやアニメーションの状態をスクリプトで考慮しなくてはならなくなるので、動かすのが難しくなる
    - そこで、親オブジェクトは移動のみの構成にして、子供のオブジェクトは自由にいじれるようにする

プレイヤーを調整する。

- https://youtu.be/ON5X-LRJBQs?t=2h58m45s
- 当たり判定の枠を見ながら、子供に加えたオブジェクトの向きや座標、大きさを調整して、当たり判定に合致するようにする

敵を設定する。この作業はプレハブのままではできない。[Hierarchy]ビューに移動させて、シーンビューに登場させて、それを調整する。作業が完了したら[Inspector]ビューの[Apply]を押す。

- https://youtu.be/ON5X-LRJBQs?t=3h3m6s

完了時間： 3:10:00

# まとめ
今回やったこと。

- GIについてと、調整方法
- ゲームオーバーやクリア時に動きを停止する
- アイテムを敵を出現させるオブジェクト Spawner(スポーナー)を作成する
- cos、sinを使って、自由な方向に、指定の長さのベクトルを作る
- ボールが跳ね返らなくなる症状の解消
- プレイヤーを画面外に出ないように調整
- GitHub Desktopの古い方を使う
- キャラクターの差し替え
