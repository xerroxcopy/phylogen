# NeighborNetを使ったプロダクトの系統関係の可視化、分類

## イントロ

似た人工物の関係性は複雑に絡み合っている。それを分類することは有用なことがある。

有用なこと：
- なに？



### 今までの方法

数量化三類　系統関係としてはUPGMA?と同等か？

### 新しい方法

コーディングの方法は大して変わらないが、系統関係を前提とする。樹形図になることが多いが、考古学的なものと比べ現代的な造形物は水平転移が多そう。→ネットワークが適切なのではないか。
考古学的なものでもネットワークを使っているものはたくさんある。
たとえばCanterbury TalesやJordan (2009)　矢野(2006)の三十六歌仙絵巻　Warp Ikat(https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0052064)　など・・・
[日本語方言のネットワーク](https://drive.google.com/file/d/0BwIcSrwaDM7KZ0JoQWdROHNzWkk/view?resourcekey=0-lsiknww4qw6afrbbBUyijw)　自動車（http://www.sis.nagoya-u.ac.jp/~ari/stuff/papers/ipsjz09-meme.pdf）
[系統樹から迫る非生命進化:鳥居・雑煮・デジタルカメラ](https://drive.google.com/drive/u/0/search?q=%E9%B3%A5%E5%B1%85)
## やったこと

### スイスアーミーナイフ

まずはやってみた。別に答えが知りたい仮説があるわけではないが。まぁわけられたね。So what?な部分はあるが。Outgroupを入れてみたり、複数の方法で可視化してみたり。
SplitsTree v4 D. H. Huson and D. Bryant, Application of Phylogenetic Networks in Evolutionary Studies, Mol. Biol. Evol., 23(2):254-267, 2006.
[Application of Phylogenetic Networks in Evolutionary Studies](https://watermark.silverchair.com/msj030.pdf?token=AQECAHi208BE49Ooan9kkhW_Ercy7Dm3ZL_9Cf3qfKAc485ysgAAAsMwggK_BgkqhkiG9w0BBwagggKwMIICrAIBADCCAqUGCSqGSIb3DQEHATAeBglghkgBZQMEAS4wEQQMn1RjRElTkmZVeEyPAgEQgIICdpJd-VWbhixvioeyeimPJRDLrp2MaGup85XK9arxhZfhJC1JQhizDmsZ4xn2LEaJ6Zg6OOjW6jREtVtDLowSa2ngwEpjPyhHGWDfnisYrbsevsOyjoqPitlkePZdpI6Vc6ePVyEkF3ZIPQVAbPPV_cfunFbdAqq2qtZ1Mw6xz84OlcxHFNABHiS-kbS4ZaAVCwCICzG-PFaYo7quC20MVzkZpgEoZ7xjkuU1NYvbjX43rF-7ZyldNNstSZyEAQIHEvmydZZUhEC0c-8I0QpkvP_3SVWW-rF6lcHUXaw5jhl8wxPDHxdIFJTbjVUuQMvY8X8UpEryps8VingOmPmIHQ-A1vHKL7K9NVYTIqu9sAJeTQpX5iYelaeo4NBULjMKhqeHzEok_hgOs3tYGsXJ_f9JEUIpgMSWjmOKh_tWhhF7aU9XDqsmeS-ejrtwltZSbqm8z2xr7aSp3WytMicRGcErw9ZfulvffeU9gbr9WLuuGyz1BM9UmI4ibCaMfqI_qDmu0ik8iW4O9aTatML_QNEHG_z4HZJ2hBdyGAW-ZTvTX4euz0ROuKSceO5P5qkwT04tfCMod0Pgn3PgJuuHRLYRZZs64d4LHre2AcoiGk15NyDjsn7l7ws-u7ddZW0xTHu-gnHciwqKQ0579xt9zSlewBqUVTkMoVDsui62NOBF_PzYsXAn48tkfS06Yj-iiVBNQqIGMOCjht4-Rk6ARySCFf0SbUGvUVxOh5EcLsZ4VB_5B80NY5HMgniAIyyThUikjefw9e1j-7fBORpTksVM-LhEis5pt3TI2_MTTf7ne4P59aWRZrLfQc3mhvZuOj2tNR1Wyw)のFig. 8とかはすごい樹状。

### サフィのAnthropomorphicなもの

人はパターンを拾い上げるように進化した。たまにエラーが起きて、シグナルから拾ってしまうこともある。たとえば顔は顔認識アルゴリズムを考えれば容易にわかるように、人間にとって最も重要なパターンである。顔でないものに顔をみたり、人体でないものに人体をみる傾向には特に名前がついている。
- pareidolia (p15)は作者がそのようなパターンを認識してもらうことを意図していないにもかかわらず認識される場合。

MrBayesを使う。MCMCMCを使っている。
系統ネットワークではなく系統樹でやった。なぜなら：
とても長いスパンの考古学的なアプローチなので、時間的な推移を推定したかった。そのためにはBEASTにして有根にする必要がある。ネットワークではこういった方法はまだないはず。


### アイドルのlight stick/lightstick

ヤグァンボン、ウンウォンボンとして[韓国KPOPにも波及している](https://dareae.info/archives/fan-light)らしい。
ネットワークでやった。とても短い期間に（たかだか数十年）でてきたもので、相互に「こういった特徴をもたせよう」という
2こめのは同じグループのものは確かに近くにある気がする・・・　
誘導棒：Outgroupとして導入。
KingBlade:ジェネリックなペンライト。[オタクライブ初心者にオススメ！キングブレードの選び方をご紹介！](https://www.pen--light.com/entry/2017/01/30/222551)
>アニメ、声優系ライブに参加する人のほとんどの方が持ってるであろうキングブレードシリーズについてご紹介します

Idol group name (abbreviated as) (Jr.) Kis-My-Ft2(kismy) A.B.C-Z (abc-z) Sexy Zone (sexy) Hey! Say! JUMP (jump) NEWS, KAT-TUN (eito) (arashi) (taki) (V6) (kinki) (smap)

#### criteria

- どのグループのペンライトか
- 持ち手の形(四角いか丸いか持ち手なしか)
- 持ち手の色(白色か色付きか)
- 本体の形(ハート型、星型、棒型、丸型、スクエア型、モチーフ型、文字型、置物型)
- 本体の色(一色かカラフルか)
- 本体の厚さ(厚いか薄いか伸縮するか)
- ストラップの有無
- 装飾の有無
- 本体が不透明か透明か
- 光の色の種類(1 色か 2 色かメンバカラーか) 
- 光り方(常灯、点滅、ムービングライト、ウェーブ、制御)
- スイッチの種類(ボタン式かスライド式か)
- 電池の種類(単三電池か単四電池かボタン電池か)
- 光り方(一色か二色か三色か四色か五色以上か)
- コンサートツアー名の有無
- ライト部分が空洞かそうではないか

樹状ではなくもっとネットワーク状だ。たとえばIkatの例は明らかにもっと樹状。

これはとても期間が短く、昔のモデルを参照するような、親から子への一方向の影響のようなものがなく、少人数のデザイナーがいろいろやるせいだろう。それでもなお同じ時期の同じグループのものはネットワーク上の同じような場所にあらわれがちなのは、それらをてんでランダムに作っては命名するのではなく、「これはXXXグループのためにつくろう」とやっている、意図のあらわれといえるだろう（ほんま？）

Deltaは調べられるがどれも対して変わらんな。


## 考察

- クラスターで切る：真菌・ウィルス？のようなcontinuumなblobである、似た者同士の人工物においてはどこのチャンクで切るのかというのは本質的とは言い難く、クラスターで切るというのは不適切ではないか
- コーディングが主観的である問題は変わりない。かといって外形を楕円フーリエやランドマークで形態表形学やる・・・？やるの？それだけじゃないものに関してなるべく客観的になるような工夫（なるべく数値を使うとか、何人もでコーディングして共通部分をまとめるとか、ランダムでいくつか落とすとか・・・？）が必要になるかもねえ。