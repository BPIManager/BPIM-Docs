---
title: BPIM アカウントの管理(Sync)
weight: 5
---

![/images/manual/stat/10.jpg](/images/manual/stat/10.jpg)

BPIM アカウントの設定は Sync 機能から行います。  
Sync は BPIM 画面右上のアカウントアイコンをタップし、メニューから「 Sync 」を選択してアクセスします。

## プロフィール

![/images/manual/stat/11.jpg](/images/manual/stat/11.jpg)

BPIM アカウントの公開設定および公開する情報を設定します。

- 表示名 : BPIM アカウントを公開する際、他人から表示されるニックネームを設定します。
  - 16文字以内、英数字で設定します。
  - 既に他人が利用しているニックネームは設定することができません。

- 最高アリーナランク : アリーナランクを設定します。
- 自己紹介を入力 : プレイヤー一覧やプロフィール画面で表示される文章を設定します。
  - @から始まる Twitter ID を入力すると、プロフィール画面に Twitter アカウントへのリンクが表示されます。
    - 例： @R1muru_Temp3st
  - IIDX IDを入力すると、プロフィール画面に IIDX 公式サイトのプロフィール画面へのリンクが表示されます。
    - 例： 6196-0282 または 61960282
    - ハイフンの有無は問いません。
- 投稿ノートを一般公開 : Notes 機能で投稿したノート一覧をプロフィール画面に表示します。
- プロフィールを一般公開 : プロフィールの公開設定を選択します。これがオフになっている場合、他のプレイヤーはあなたのプロフィールを確認できません。

プロフィールの変更点は「変更を保存」ボタンをタップして即時反映されます。

## データ

クラウド上にスコアデータを保存、またはクラウド上のスコアデータをローカルにダウンロードします。

設定画面より「 Auto-sync 」をオンにすることで、スコアの更新をこの画面からアップロードする必要はなくなります。

## ライバル

クラウド上のライバルデータとローカル上のライバルデータを同期するための画面です。  
BPIM v0.0.4.2 以降では、クラウドとローカルのライバルデータは自動で同期されるため、基本的に触る必要のない画面です。

複数端末で同一の BPIM アカウントを利用している場合、この画面から端末間のライバルデータを同期できます。

## プッシュ通知

ライバルがスコアを更新した際、端末へ通知を送信する機能です。  
通知を受け取りたいライバルのトグルをオンにしてください。

- iOS 端末ではプッシュ通知機能をご利用いただけません
- 最短通知間隔は 30 分です。
