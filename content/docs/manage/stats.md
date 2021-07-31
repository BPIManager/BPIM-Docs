---
title: 統計を表示
weight: 2
---

BPI や EX スコアを各側面から分析するための機能です。

「基本」「レーダー」「推移」「分布」「自己歴代」の 5 タブから構成されます。 

## 基本

![/images/manual/stat/1.jpg](/images/manual/stat/1.jpg)

総合 BPI や DJ ランクなど、基本的な分析を表示します。  
画面右上の「表示対象」から統計を表示する難易度を選択します。

### 総合 BPI

[BPI の定義](http://norimiso.web.fc2.com/aboutBPI.html)に基づき、単曲 BPI の二乗平均平方根で算出されます。  
推定順位の算出方法についても同様に、 BPI の定義に依拠しています。

### BPI 分布

単曲 BPI の度数分布を表しています。  
グラフ中の縦実線は総合 BPI の位置を表しています。

### BPM 帯別総合 BPI

BPM 帯ごとの単曲 BPI の度数分布を表しています。  
SOF とはソフランを含む楽曲を示しています。

BPM 帯別総合 BPIにおける総合 BPI の算出式は、上記総合 BPI と同一です。

### DJ ランク・クリアタイプ

各楽曲の DJ ランクおよびクリアタイプを円グラフで表します。

## レーダー

![/images/manual/stat/2.jpg](/images/manual/stat/2.jpg)

beatmania IIDX のプレイスキルにおける代表的な要素ごとに代表楽曲を選出し、それぞれについて総合 BPI を算出したものがレーダーです。

### 対象楽曲

2021/7/30 時点における、各要素の対象楽曲は次のとおりです。

| ターゲット | 集計対象                                                     |
| ---------- | ------------------------------------------------------------ |
| NOTES      | B4U(BEMANI FOR YOU MIX)(L)<br />Chrono Diver -PENDULUMs-(A)<br />Elemental Creation(A)<br />perditus†paradisus(A)<br />Sigmund(L)<br />Verflucht(L) |
| CHARGE     | DIAMOND CROSSING(A)<br />ECHIDNA(A)<br />Snakey Kung-fu(A)<br />Timepiece phase II (CN Ver.)(A)<br />TOGAKUSHI(A) |
| PEAK       | KAMAITACHI(L)<br />X-DEN(A)<br />卑弥呼(A)<br />疾風迅雷(L)<br />天空の夜明け(A) |
| CHORD      | Beat Radiance(L)<br />Despair of ELFERIA(A)<br />Little Little Princess(L)<br />mosaic(A)<br />Rave\*it!! Rave\*it!!(A)<br />waxing and wanding(L) |
| GACHIOSHI  | 255(A)<br />BITTER CHOCOLATE STRIKER(A)<br />GRID KNIGHT(L)<br />VANESSA(L)<br />童話回廊(A) |
| SCRATCH    | BLACK.by X-Cross Fade(A)<br />Snake Stick(A)<br />Red. by Jack Trance(A)<br />灼熱Beach Side Bunny(A)<br />灼熱 Pt.2 Long Train Running<br />火影(A) |
| SOFLAN     | DAY DREAM(A)<br />Fascination MAXX(A)<br />ruin of opals(A)<br />Concertino in Blue(A)<br />PARANOiA ～HADES～(A)<br />冥(A) |
| DELAY      | DIAVOLO(A)<br />Mare Nectaris(A)<br />quell ～the seventh slave～(A)<br />Thor's Hammer(A) |
| RENDA      | IMPLANTATION(A)<br />Innocent Walls(H)<br />Scripted Connection⇛ A mix(A)<br />Sense 2007(A)<br />ピアノ協奏曲第１番”蠍火”(A)<br />ワルツ第17番 ト短調”大犬のワルツ”(A) |

対象楽曲は一定期間ごとに見直しを行っています。  
また、対象楽曲は [アンケート](https://docs.google.com/forms/d/e/1FAIpQLSfhJkZZp5K1ChbE5RH-f0hOIkGvGX-7tYCZMxzVlsHVAtZ6eg/viewform) の実施結果をもとに決定されます。

## 推移

![/images/manual/stat/3.jpg](/images/manual/stat/3.jpg)

過去の楽曲更新数や総合 BPI の推移をグラフで表示します。

### 設定項目

- 表示対象 : 更新履歴および総合 BPI 推移の対象とする難易度を変更します。
- プライマリグラフの表示項目 : 複合グラフに表示する内容を設定します。
- 表示期間 : データの集計期間を設定します。

## 分布

![/images/manual/stat/4.jpg](/images/manual/stat/4.jpg)

バージョン間におけるスコアの更新点数を分布図に表します。

前作に比べ、大幅に上達したのか、あまり上達していないのか、はたまた下手になっているのか、といった判断を、他の楽曲の上昇率と比較し相対的に判断することを目的として搭載されています。

## 自己歴代

各楽曲につき、自己歴代を表示します。
