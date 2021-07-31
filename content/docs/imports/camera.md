---
title: BPIカメラ
weight: 4
---

BPI カメラ機能を用いてスコアを登録する方法です。

## 特徴

### メリット

- eAMUSEMENT に追加課金する必要がありません。
- 手動入力に比べ、楽曲を探す手間やスコアを入力する手間が省けます。
- プレイしたその場でBPIを調べることができます。

### デメリット

-  手ブレなどにより、楽曲名の誤検知を起こす場合があります。

## 手順

1. [BPI カメラ](https://bpi.poyashi.me/camera) を起動します。
2. リザルトを撮影します。
3. 読み取り結果が表示されますので、正しい場合は「スコアを保存」ボタンをタップします。

画面サンプルは下記ツイートをご参照ください。（プロトタイプ版のため、最新版とはUIが異なります）

<blockquote class="twitter-tweet"><p lang="ja" dir="ltr">【本体更新】v0.0.8.0<br>・BPIカメラをリリースしました。リザルト画面を撮影いただくだけでBPIを判定いただけます。（動作イメージは画像参照）<br>・詳しい使い方はこちら（<a href="https://t.co/dLceOcTF30">https://t.co/dLceOcTF30</a>）をご参照ください。 <a href="https://t.co/TrVdwuvjnS">pic.twitter.com/TrVdwuvjnS</a></p>&mdash; BPIManager (@BPIManager) <a href="https://twitter.com/BPIManager/status/1398288234489159680?ref_src=twsrc%5Etfw">May 28, 2021</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### 設定項目

撮影ボタン右側の歯車アイコンをタップして、 BPI カメラの設定を変更します。

- カメラ選択 : 撮影に使用するカメラを変更します。(インカメラまたはアウトカメラ)
- 撮影後のアクション : 撮影した写真を自動で端末にダウンロードします。
- データの提供 : 楽曲・スコアの読み取り精度を向上させるため、撮影データをサーバーに送信します。
