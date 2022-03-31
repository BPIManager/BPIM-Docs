---
title: ブックマークレット(eAMUベーシック)
weight: 2
---

beatmania IIDX 公式サイト上で BPIM 用ブックマークレットを実行し、 BPIM へスコアを登録する方法です。

## 特徴

### メリット

- 迅速に複数楽曲のスコアを登録いただけます。
- スコアと一緒にクリアランプをお取り込みいただけます。

### デメリット

-  [eAMUSEMENT ベーシックコース](https://p.eagate.573.jp/payment/p/select_course.html?course=eaBASIC)への加入が必要です。
-  スコアの更新日時が、ブックマークレット実行日時となります。(正確な更新日時が反映されません)

## 手順

```javascript
javascript:(function() { javascript: (function(d, s) { s = d.createElement('script'); s.src = 'https://files.poyashi.me/bpim/index.js?v=' + String(Math.floor(Math.random() * 10000000)); d.body.appendChild(s); })(document) })();
```

1. 上記ブックマークレットをお使いのブラウザに登録します。
2. [beatmania IIDX](https://p.eagate.573.jp/game/2dx/28/top/index.html) 公式サイトを開き、ブックマークレットを実行します。
3. データ取得完了後、自動的に [BPIM 取り込みページ](https://bpi.poyashi.me/data) へ移動しデータのインポートが開始されます。


### ご注意

- インポート用ブックマークレットは SP のスコア取り込みのみ対応しています。
- ブックマークレットを用いた場合、スコアの更新日時はブックマークレットの実行時刻になります。（実際のスコア更新時刻は反映されません）
- ミスカウントはインポートされません。

