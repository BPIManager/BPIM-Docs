---
title: BPIM のご利用方法
weight: 2
---

BPIManager (以下 BPIM ) をお使いいただくための手順をご紹介します。  
各機能の詳しい仕様および使用方法については、メニュー「2. 利用マニュアル」をご確認ください。

## ご利用開始

BPIM は Web アプリケーションです。
特別な操作は必要なく、下記 URL にアクセスするだけで直ぐにご利用いただけます。

#### [https://bpi.poyashi.me](https://bpi.poyashi.me)

### ウェブ アプリケーションとしてインストール

BPIM は PWA に対応しています。  
お使いのスマートフォンで「ホーム画面に追加」することで、通常のネイティブアプリと同様にご利用いただけます。

インストール方法は、 BPIM トップページにアクセスした際に表示されます。

{{% notice note %}}
BPIM の一部機能は PWA として動作することを前提に設計されています。
{{% /notice %}}

### 更新情報

BPIM の更新情報は、Twitterにて随時告知しています。

[@BPIManager](https://twitter.com/BPIManager)

### 動作要件

- ブラウザのシークレットモードが無効になっていること
- IndexedDB が利用可能である環境
- fetch API が利用可能である環境
- 画面サイズ：横 360px 以上
- iOS 端末では、プッシュ通知など一部機能のご利用が制限されます。
- 動作確認は Android 9 、 Google Chrome (Windows)、 Firefox (Windows) で実施しています。

各機能の対応状況は下記URLをご確認ください。

- IndexedDB : [https://caniuse.com/indexeddb](https://caniuse.com/indexeddb)
- fetch API : [https://caniuse.com/fetch](https://caniuse.com/fetch)
- A2HS : [https://caniuse.com/web-app-manifest](https://caniuse.com/web-app-manifest)
- Firebase Cloud Messaging : [https://firebase.google.com/support/guides/environments_js-sdk?hl=ja](https://firebase.google.com/support/guides/environments_js-sdk?hl=ja)
