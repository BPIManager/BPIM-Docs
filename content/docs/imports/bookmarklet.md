---
title: ブックマークレット(eAMUベーシック)
weight: 2
---

beatmania IIDX 公式サイト上で BPIM 用ブックマークレットを実行し、 BPIM へスコアを登録する方法です。

## 特徴

### メリット

- CSV インポートほどではありませんが、迅速に複数楽曲のスコアを登録いただけます。
- スコアと一緒にクリアランプをお取り込みいただけます。

### デメリット

-  [eAMUSEMENT ベーシックコース](https://p.eagate.573.jp/payment/p/select_course.html?course=eaBASIC)への加入が必要です。
-  スコアの更新日時が、ブックマークレット実行日時となります。(正確な更新日時が反映されません)

## 手順

```javascript
javascript:(function() { javascript: (function(d, s) { s = d.createElement('script'); s.src = 'https://files.poyashi.me/bpim/index.js?v=' + Number(Math.floor(Math.random() * 10000000)); d.body.appendChild(s); })(document) })();
```

1. 上記ブックマークレットをお使いのブラウザに登録します。
2. [beatmania IIDX](https://p.eagate.573.jp/game/2dx/28/top/index.html) 公式サイトを開き、ブックマークレットを実行します。
3. 暫く待つと（参照）図のように実行結果が画面に表示されますので、結果をコピーします。
4. [BPIM 取り込みページ](https://bpi.poyashi.me/data) を開き、「取り込み実行」ボタンをタップします。

（参照）

![https://files.poyashi.me/bpim/sample_completed.jpg](https://files.poyashi.me/bpim/sample_completed.jpg)



### ご注意

- インポート用ブックマークレットは SP のスコア取り込みのみ対応しています。
- ブックマークレットを用いた場合、スコアの更新日時はブックマークレットの実行時刻になります。（実際のスコア更新時刻は反映されません）
- ミスカウントはインポートされません。

