---
title: CSVインポート(eAMUプレミアム)
weight: 1
---

beatmania IIDX 公式サイトからダウンロードできる CSV データを用い、 BPIM へスコアを登録する方法です。

## 特徴

### メリット

- CSV ダウンロードページへアクセスするだけでデータ取り込みができます。
- スコアの更新時刻や ミスカウント など、詳細情報をセットで取り込みができます。

### デメリット

-  [eAMUSEMENT プレミアムコース](https://p.eagate.573.jp/gate/pub/course/eapremium/index.html)への加入が必要です。

## 手順

1. [こちらのページ](https://p.eagate.573.jp/game/2dx/28/djdata/score_download.html?style=SP) へアクセスし、CSVをテキストデータとしてコピーします。
2. [BPIM 取り込みページ](https://bpi.poyashi.me/data) へアクセスします。
3. 「取り込み実行」ボタンをタップします。

### ご注意

- CSV ダウンロードページの読み込みが完了していない状態で CSV をコピーし、 BPIM にインポートすると、本来存在しない楽曲が取り込みエラーに表示される場合があります。
- 低速モードでの通信の場合、ダウンロードページの読み込みが完了したことを確認した上でお取り込みください。

### Tips: eAMU ベーシック会員で CSV インポートを利用する

{{% notice warning %}} 

BPIM はこの方法を利用したデータインポートに最適化されていません。  
eAMUSEMENT ベーシックコース加入済みで一括取り込みを行いたい場合、[こちらのブックマークレット](../bookmarklet/) のご利用を推奨します。

{{% /notice %}}

非公式ブックマークレットを利用し、 eAMUSEMENT プレミアムコースに加入していない場合でも CSV インポートをご利用いただけます。

```javascript
javascript:$.getScript('https://files.poyashi.me/csvGen/update.min.js?v=201213');
```

上記スクリプトを IIDX 公式サイト上で実行し、画面指示に従いダウンロードした CSV をテキストデータ化しインポートを実行してください。

{{% notice info %}}
スクリプトの原著作者は @lazykuna 氏であり、スクリプトの改変者は [Len](https://len-ch.com/) 氏です。  
poyashi.me は MIT ライセンスに基づき当該スクリプトを再配布しております。

{{% /notice %}}
