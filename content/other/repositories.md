---
title: 関連リポジトリ
---

BPIManager で使用しているデータおよびマイクロサービスに関する情報を公開しています。  
これらにつき、ソフトウェア開発者は「各種規約」>「利用規約」に違反しない範囲における自由な利用を許諾します。

### bpimanager

https://github.com/potakusan/bpimanager

BPIManager のフロントエンド部分です。

### bpim-score-repo

https://github.com/potakusan/bpim-score-repo

BPIM で BPI の算出に用いている皆伝平均及び全国一位データが記載されたファイル群です。

### bpim-wrgetter

https://github.com/potakusan/bpim-wrgetter

BPIM の定義ファイルと IIDX 公式サイトの全1データを比較し、更新がある場合に定義ファイルを更新するためのスクリプトです。

### bpimanager-docs

https://github.com/potakusan/bpimanager-docs

このドキュメントです。

---

### proxy.poyashi.me

[https://proxy.poyashi.me/](https://proxy.poyashi.me/)

定義ファイルを読み込むための CORS 制限設定が解除されたプロキシサーバーです。
リクエストメソッドはすべて GET です。

また、指定した Twitter ユーザーの最新のアイコンを取得するためのスクリプトが実装されています。

- アイコン指定例 : https://proxy.poyashi.me/img?screen_name=R1muru_Temp3st&size=original
- BPIM 定義ファイル取得 : https://proxy.poyashi.me/?type=bpi
- BPIM 定義ファイルメタデータ取得 : https://proxy.poyashi.me/?type=bpiVersion
