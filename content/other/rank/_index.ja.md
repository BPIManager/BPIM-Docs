---
title: BPIMRanks API
weight: 20
chapter: false
---

## はじめに

BPIMRanks API は、 BPIManager に蓄積されたデータを表示・集計する API です。  
データは個人利用に限り、自由にご活用ください。

**このページは書きかけです**

## 基本

- ベースURL

  [https://proxy.poyashi.me/bpim/api/v1/](https://proxy.poyashi.me/bpim/api/v1/)

- 使用制限 : 現在、ご利用にあたり認証の必要やレートリミットは設定がありません。

#### レスポンス形式

```
{
	"error": false, // リクエストにエラーが含まれる場合に true
	"maintenance": false, // 定時メンテナンス時のみ true
	"time": "20220131024953", // リクエストを処理した時点でのサーバー時間
	"body": [], // Response Body
	"meta": {
		"idx": "49",
		"latestVersion": "29", // サーバーに設定された最新のIIDXバージョン
		"updatedAt": "2022-01-31 03:16:36" // 最後にデータが更新された時刻
	}
}
```

## 楽曲

#### GET /songs/list ([Example](https://proxy.poyashi.me/bpim/api/v1/songs/list?level=12&store=29&offset=0&limit=10&withPlayerSum=1))

##### Queries

- level:"11"|"12" 集計対象の楽曲レベル
- store:"28"|"29" 集計対象のIIDXバージョン(28 BISTROVER または 29 CastHour のみ)
- offset:Number オフセットを指定
- limit:Number 表示件数を指定
- withPlayerSum?:boolean プレイヤー総数をデータに含む場合はクエリに含める　それ以外の場合はクエリを含めない

Notes

- withPlayerSum オプションを使用するとクエリが大変遅くなります。

Body

- レスポンス内 body は下記 Object の配列が返却されます。

```
{
		"uid": "JZOB00HuSfbYd7jPM7A1T7KsPVJ3", // 1 位プレイヤーの uid
		"title": "-65\u2103", // 楽曲名
		"difficulty": "another", //楽曲難易度 (hyper,another,leggendaria)
		"difficultyLevel": "12", //楽曲難易度 (12 段階表記)
		"exScore": "3768", // 1位プレイヤーの EX スコア
		"bpi": "112", // 1位プレイヤーの BPI
		"displayName": "SEIRYU", // 1位プレイヤーのユーザー名(非公開プレイヤーの場合 null )
		"photoURL": "https:\/\/pbs.twimg.com\/profile_images\/1395372542181871617\/zqCeVHNS_normal.jpg", // 1位プレイヤーのプロフィール画像(非公開プレイヤーの場合 null )
		"updatedAt": "2021-10-21 22:42:00", // 1位プレイヤーの更新日時
		"playerSum": "566" // プレイヤー総数 (withPlayerSum オプション使用時のみ)
}, ...
```

