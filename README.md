# 課題
Mermaidを触ってみよう

マークダウンファイルを編集して、Mermaidで図を描いてみよう

# 取り組み方
* 本プロジェクトをforkしてください。
* README.mdを編集して、Mermaidを使いこなしてください
* できたらプルリクエストを出します

# 課題項目
## 流れ図
### 条件
- 開始と終了ノードをつける
- 条件分岐を組み込む
- 5ノード以上
- カッコいいほど高得点

## 解答
```mermaid
flowchart LR;
  A([開始])-->B[/弾を撃つ/];
  B-->C{当たり判定}
  C--真-->D[敵HP減少];
  D-->E([終了])
  C--偽-->E([終了])
```

## シーケンス図

- 3人以上
- メッセージをやり取りしない人がいないように
- 自己呼び出しを含むこと
- カッコいいほど高得点

## 解答
```mermaid
sequenceDiagram
participant player
participant　Event1
participant　Event2
participant  Event3
participant　BAD_END
participant　Normal_END
participant　HAPPY_END
player->>Event1:攻略対象と成功（+1ポイント）
player->>Event1:攻略対象と失敗
loop FRIEND_END
Event1->>Event1:必須クリア項目
end
Event1->>Event2:攻略対象と成功（+1ポイント）
Event1->>Event2:攻略対象と失敗
Event2->>Event3:攻略対象と成功（+1ポイント）
Event2->>Event3:攻略対象と失敗
Event3->>BAD_END:1ポイントの場合
Event3->>Normal_END:2ポイントの場合
Event3->>HAPPY_END:3ポイントの場合
BAD_END-->>Event2:中間ポイントからスタート
Normal_END-->>Event2:中間ポイントからスタート
```


## クラス図

### 条件
- 3つ以上
- 汎化と集約を含むこと
- カッコいいほど高得点

## 解答
```mermaid
classDiagram

ヴァロラントo-- エージェント
エージェント:役割[]
エージェント:+戦う()
エージェント--|>デュエリスト
エージェント--|>センチネル
エージェント--|>イニシエーター
エージェント--|>コントローラー
デュエリスト:戦闘アビリティ[]
センチネル:防御アビリティ[]
イニシエーター:索敵アビリティ[]
コントローラー:妨害アビリティ[]
デュエリスト--|>フェニックス
デュエリスト--|>ジェット
デュエリスト--|>レイズ
デュエリスト--|>レイナ
デュエリスト--|>ヨル
デュエリスト--|>ネオン
コントローラー--|>ヴァイパー
コントローラー--|>ブリムストーン
コントローラー--|>オーメン
コントローラー--|>アストラ
イニシエーター--|>ソーヴァ
イニシエーター--|>ブリーチ
イニシエーター--|>スカイ
イニシエーター--|>ケイオー
イニシエーター--|>フェイド
センチネル--|>セージ
センチネル--|>サイファー
センチネル--|>キルジョイ
センチネル--|>チェンバー
```