---
title: 定義ファイルの記述
---

BPIM では、カスタム定義ファイルを作成しアプリケーション上で利用できます。

## 定義ファイルの仕様について

BPIM では楽曲に関する一連のデータを定義ファイルと称するファイルにまとめて公開しています。  
このファイルはJSONで記述されています。

### 公式定義ファイル

BPIM が公式で用意している定義ファイルは、下記 URL から確認できます。

[https://proxy.poyashi.me/?type=bpi](https://proxy.poyashi.me/?type=bpi)

リポジトリ : [https://github.com/potakusan/bpim-score-repo](https://github.com/potakusan/bpim-score-repo)

### 仕組み

JSONの仕組みは次のようになっています。

    {
      "version":"20191109", //定義データのバージョン名
      "requireVersion":"8", //要求するBPIManager本体のバージョン(例:v0.0.0.8ならば8,v0.0.2.0ならば20)
      "body":[
    	{  
          "title": "(This Is Not) The Angels", //楽曲名
          "difficulty": "4", //楽曲難易度(詳細は下)
          "wr": "2716", //歴代1位
          "avg": "2398", //皆伝平均
          "notes": "1364", //ノート数
          "bpm": "33-130", //BPM
          "textage": "24/theangel.html?1AB00", //TexTageのURL
          "difficultyLevel": "11", //楽曲難易度(詳細は下)
          "dpLevel": "0", //DP非公式難易度
          "coef": -1, //譜面係数
    	},...
      ]
    }
### 型について
JSONに記述する定義データの型は次のようにします。

| キー            | バリュー                       | 備考                                                         |
| --------------- | ------------------------------ | ------------------------------------------------------------ |
| title           | String                         | 楽曲名                                                       |
| difficulty      | "3"\|"4"\|"8"\|"9"\|"10"\|"11" | 楽曲難易度(下記参照)                                         |
| difficultyLevel | "11"\|"12"                     | ゲーム内楽曲難易度                                           |
| wr              | String\|Number                 | 全1スコア                                                    |
| avg             | String\|Number                 | 皆伝平均                                                     |
| notes           | String\|Number                 | 楽曲総ノート数                                               |
| bpm             | String                         | BPM<br />(ソフランする場合は最小BPMと最大BPMを半角ハイフンで区切って入力。例:33-130) |
| textage         | String                         | TexTageのURL                                                 |
| dpLevel         | String                         | DP非公式難易度<br />SP譜面の場合必ず0<br />DP譜面の場合は必ず0以外を入力 |
| coef            | Number                         | 譜面係数<br />未設定の場合は-1とする                         |
| removed         | ?Boolean                       | 削除曲の場合はtrue<br />それ以外の場合はキーを含めない(後述) |

{{% notice note %}}
"wr","avg","notes"はデータベースに登録される際、Number型にキャストされます。
{{% /notice %}}

### 楽曲難易度
楽曲難易度はdifficultyおよびdifficultyLevelの2つが必要です。  
difficultyではいわゆるHYPER,ANOTHER,LEGGENDARIAを識別し、difficultyLevelでは☆換算の難易度を識別します。  
difficultyの対応表は次のようになります。

| 難易度      | SP   | DP   |
| ----------- | ---- | ---- |
| HYPER       | 3    | 8    |
| ANOTHER     | 4    | 9    |
| LEGGENDARIA | 10   | 11   |

difficultyLevelには11または12を指定してください。  
すなわち、実際には☆10の楽曲であっても、便宜上☆11または☆12として登録する必要があるということです。  

### メタデータ

定義ファイルのメタデータとして、version および requireVersion を指定します。

version には任意のバージョン名を入力します。  
BPIM では読み込み済みの定義データバージョン名と異なるバージョン名の定義ファイルをフェッチした際にデータをアップデートします。

requireVersion には BPIM 本体の要求バージョンを入力します。  
古いバージョンの BPIM では一部の機能に対応していない場合があります (DP 譜面や譜面係数など)。  
そのため、一般的に requireVersion は最新の BPIM のバージョンを指定することが望ましいでしょう。  

最新の BPIM バージョンは、[こちらのファイル](https://proxy.poyashi.me/?type=bpiVersion)の requireVersion から確認できます。

### removed キーについて

端末に登録済みの楽曲について、楽曲データベースから削除したい場合、楽曲オブジェクトに "removed" キーを含めます。   
removed キーの型は Boolean が予定されますが、型チェックはしていません。
このキーが存在していれば無条件で楽曲データが削除されます。 

リストから楽曲を削除しない場合は removed : false とするのではなく、**絶対に removed キーを追加しないでください**。

removed キーが新たに認識された際、 BPIM は楽曲データとともに、その楽曲に紐付けられたスコアデータおよびスコアログデータが削除します。

## カスタム定義ファイルの登録

### 設定

カスタム定義ファイルを BPIM に読み込むには、定義ファイル URL の設定が必要です。

BPIM の「設定」から「定義ファイルURLを変更する」をクリックし、カスタム定義ファイルの URL を入力してください。

### 制限

BPIM からカスタムされた定義ファイルを読み込むためには、セキュリティの制約から一定の条件を満たす必要があります。 

fetch APIを用いて定義ファイルを取り込んでいるため、CORSを許可する必要があります。  

| Key                          | Value          |
| ---------------------------- | -------------- |
| Access-Control-Allow-Origin  | bpi.poyashi.me |
| Access-Control-Allow-Methods | GET,OPTIONS    |

以下に、 nginx サーバーにおける設定例を示します。

```
server {
	location / {
		if ($request_method = 'OPTIONS') {
			add_header 'Access-Control-Allow-Origin' 'https://bpi.poyashi.me';
			add_header 'Access-Control-Allow-Methods' 'GET, OPTIONS';
			add_header 'Content-Length' 0;
			return 204;
		}
		if ($request_method = 'GET') {
			add_header 'Access-Control-Allow-Origin' 'https://bpi.poyashi.me';
			add_header 'Access-Control-Allow-Methods' 'GET, OPTIONS';
		}
	}
}
```



## その他
すでに登録されている楽曲データとの混合を避けるため、定義ファイルURLを変更する前に楽曲データベースをリセットすることを推奨します。  
(設定->データリセット->Songs Database)
