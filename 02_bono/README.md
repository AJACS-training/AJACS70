# ゲノムデータベースとそれを活用した配列解析入門 at AJACS筑波4

情報・システム研究機構 データサイエンス共同利用基盤施設 ライフサイエンス統合データベースセンター  
[坊農 秀雅](http://dbcls.jp/~bono/) bono@dbcls.rois.ac.jp  
2018年7月10日


----

これは統合データベース講習会AJACS筑波4「ゲノムデータベースとそれを活用した配列解析入門」の資料です。

----

## 概要

本講習は、だれでも自由に使うことができる公共DBやウェブツールを活用して、オミックス解析の基本であるゲノム配列のDBを簡単に調べるための方法と基礎知識について学びます。
とくに、それらを活用した配列解析の基礎に関して実例を交えながら詳しく説明、実習します。

----

## 講習の流れ
今回の講習では、以下の内容について順番に説明します。【実習】の部分はみんなでやる実習、【応用】は早くできてしまった人用の応用課題です。

- [研究現場で頻繁に使われるDBやツールを知る: 統合TV](#togotv)
- [ゲノムデータベースとゲノムブラウザ](#genome)
  - NCBI
  - ゲノムブラウザ
    - 【実習1】UCSC Genome Browserを使いこなす
    - 【応用1】Ensembl Genome Browserを使いこなす
- [塩基配列データベース](#insd)
  - 国際塩基配列データベース共同研究(INSDC)
    - DDBJ/EMBL/GenBank
    - Sequence Read Archive (SRA)
   - RefSeq
- [配列アラインメント](#sa)
  - 大域的アラインメントと局所的アラインメント
    - 【実習2】BLAST
    - 【応用2】BLAT
  - 多重配列アラインメントと分子系統樹
    - 【実習3】Clustalω
    - 【応用3】mafft
- [タンパク質モチーフ・ドメイン検索](#pmd)
  - 【実習4】Pfam
  - 【応用4】InterPro
    
----

### 講習に際しての注意とお願い

- みんなで同時にアクセスするとサイトにつながりにくくなることが予想されます。
    - 資料を見ながら自力で進められそうな方はどんどん先に、そうでない方は講師と一緒にすすめていきましょう。
    - サイトの反応が悪い時はタイミングをずらして実行してみてください。
    - 反応が無いからと言って何度もクリックするとますます繋がらなくなってしまいます。おおらかな気持ちで臨みましょう。
- わからないことがあったら挙手にてスタッフにお知らせください。
    - 遠慮は無用です(そのための講習会です!)。おいてけぼりは楽しくありません。

----

## <a name="togotv">研究現場で頻繁に使われるデータベースやツールを知る</a>
### [統合TV](https://dbcls.rois.ac.jp/services.html#TogoTV_ja)
- 生命科学分野の有用なデータベースやツールの使い方を動画で紹介するウェブサイト
    - http://togotv.dbcls.jp/ [![https://gyazo.com/acd9a661ebb043e62cc50176d6ad69ca](https://i.gyazo.com/acd9a661ebb043e62cc50176d6ad69ca.png)](http://togotv.dbcls.jp/)
    - YouTube版もあります　http://youtube.com/togotv/
    - ウェブサイトへのアクセスから結果の見方まで、操作の一挙手一投足がわかります。
        - 講義・講習などの参考資料や後輩指導の教材として利用できます。
        - 本講習中、本家サイトが繋がらない時は、統合TVのYouTube版を見ればおおよその内容がわかるようになっています。
        - 今回の講習に関連する内容の多くは、「発現解析」タグのついた動画にあります。
        - 過去の講習会の内容はそのほとんどが統合TVに収録されており、いつでもどこでも繰り返し復習できるようになっています。
    - お探しの動画が見つからない or 統合TV未掲載の場合は、[統合TV番組リクエストフォーム](http://togotv.dbcls.jp/ja/contact.html)へどうぞ!
    - [統合TVを作ってくれる方、募集中!!](https://twitter.com/bonohu/status/747954940157399040)

----

## <a name="genome">ゲノムデータベースとゲノムブラウザ</a>
### ゲノムデータベースとは？
- ゲノム配列を始めとした（遺伝）情報を生物種ごとにまとめたデータベース
- 狭義にはゲノム配列のデータベースをいう

#### さまざまなゲノムデータベース
- [NCBI](https://www.ncbi.nlm.nih.gov/) (National Center for Biotechnology Information) の [**Genome**](https://www.ncbi.nlm.nih.gov/genome/)
  - [生物種ごと(Browse by Organism)](https://www.ncbi.nlm.nih.gov/genome/browse#!/overview/)
- [PlantGDB](http://www.plantgdb.org)
  - [Plant Genome Database Japan(PGDB)](http://pgdbj.jp/)
- 等々

### ゲノムブラウザとは？

- 塩基配列解読したゲノム配列とそこに付与（アノテーション）された情報を見るための仕組み
- オンライン型とローカル型
  - オンライン型：ウェブブラウザ上で。サーバにあるゲノムデータベースから必要な情報を取り出してこれる
    - UCSC Genome Browser https://genome.ucsc.edu/
    - Ensembl Genome Browser https://www.ensembl.org/
    - NCBI Genome Data Viewer https://www.ncbi.nlm.nih.gov/genome/gdv/
    - TOGO GENOME http://togogenome.org/
  - ローカル型：手元のコンピュータにインストールして使用
    - Integrative Genomics Viewer(IGV) https://software.broadinstitute.org/software/igv/

#### 【実習1】UCSC Genome Browser

1. **"UCSC Genome Browser"** でググって、そのトップページを開く。
2. トップページにはツール名がリストされている。一番上にある **"Genome Browser"** をクリックする。
[![https://gyazo.com/df2e2e72be244cf4060bba364fc542e3](https://i.gyazo.com/df2e2e72be244cf4060bba364fc542e3.jpg)](https://gyazo.com/df2e2e72be244cf4060bba364fc542e3)
3. 最寄りのミラーサイトに接続するか訊いてくるので、指示に従う。
[![https://gyazo.com/0a10cb8a25d2a3919506b7ab6fb5335f](https://i.gyazo.com/0a10cb8a25d2a3919506b7ab6fb5335f.png)](https://gyazo.com/0a10cb8a25d2a3919506b7ab6fb5335f)
4. Genome Browserのページが開くので、生物種(**Human**)とアッセンブリ(**Feb.2009/(GRC37/hg19)**)を選んで、検索後を入力する。[![https://gyazo.com/05ab6f4871c60485d4c54828a7f5f972](https://i.gyazo.com/05ab6f4871c60485d4c54828a7f5f972.png)](https://gyazo.com/05ab6f4871c60485d4c54828a7f5f972)
5. FAM32A遺伝子のゲノム領域が表示される。[![https://gyazo.com/2032119adde3af87b91266dc6197e0a5](https://i.gyazo.com/2032119adde3af87b91266dc6197e0a5.png)](https://gyazo.com/2032119adde3af87b91266dc6197e0a5)
6. "Regulation"の"ENC TF Binding..."を"hide"から"show"に変更して、"refresh"ボタンを押す。[![https://gyazo.com/ef4f449cc185c0cd917c978ed356ff93](https://i.gyazo.com/ef4f449cc185c0cd917c978ed356ff93.png)](https://gyazo.com/ef4f449cc185c0cd917c978ed356ff93)
7. 転写因子結合サイトの情報が追加される。[![https://gyazo.com/703be239476dfeae1985eb0348048bc2](https://i.gyazo.com/703be239476dfeae1985eb0348048bc2.png)](https://gyazo.com/703be239476dfeae1985eb0348048bc2)
8. いろいろ変更して表示してみましょう。わからなくなったら、図の下に並んでいるボタンの"default tracks"を押すと最初の状態に戻せます。

##### 【復習】 UCSC Genome Browserの統合TV

- 様々な目的の配列を取得する https://doi.org/10.7875/togotv.2017.098
- 様々な組織、細胞における遺伝子発現データをゲノムブラウザで表示する https://doi.org/10.7875/togotv.2017.111
- UCSC ゲノムブラウザとともに開発されてきた関連ツールを使った統合TV
  - UCSC VisiGeneを使って生体内におけるmRNAの局在を調べる https://doi.org/10.7875/togotv.2017.084
  - UCSC Gene Sorterを使って遺伝子間の関連性を検索する https://doi.org/10.7875/togotv.2017.083

#### 【応用1】Ensembl Genome Browserを使いこなす

Ensembl Genome Browser でも上記のFAM32Aを検索してみよう。

##### 【参考】 Ensembl Genome Browserの統合TV
- 配列を取得する〜 https://doi.org/10.7875/togotv.2017.046
- 様々な生物種間の配列を比較する http://doi.org/10.7875/togotv.2017.097
- 過去のバージョンのゲノムアノテーションを調べる http://doi.org/10.7875/togotv.2017.088
- 遺伝子の場所や周辺情報を調べる http://doi.org/10.7875/togotv.2017.082


----

## <a name="insd">塩基配列データベース</a>

塩基配列(DNAやRNA)のデータベースで、上述のゲノムデータベースやゲノムブラウザの元になっているデータがここに一次ソースとしてバンク（アーカイブ）されている。

### 国際塩基配列データベース共同研究(INSDC)

- [International Nucleotide Sequence Database Collaboration (INSDC)](http://www.insdc.org/) によって、1987年より日欧米の3箇所で塩基配列の登録、**データの交換**、維持管理を行っている。
  - つまり、どこに登録してもデータは他の2つに反映される
- 日本では、国立遺伝学研究所の[DDBJセンター](https://www.ddbj.nig.ac.jp/)に
  - 日本語での対応をしてもらえる
- INSDC DBのTable （http://www.insdc.org/ より）
  - 現在は、表の5種類のDBがINSDCの対象
[![https://gyazo.com/50a7d496b881d2c022bf9a15fecf893c](https://i.gyazo.com/50a7d496b881d2c022bf9a15fecf893c.png)](https://gyazo.com/50a7d496b881d2c022bf9a15fecf893c)


#### DDBJ/EMBL/GenBank
- 今はAnnotated sequencesと呼ばれている昔からあるDB

#### Sequence Read Archive (SRA)
- SRAデータも交換されている
  - DDBJにもあるので、そこから取ると早くダウンロードできる。
  - DDBJではDDBJ Sequence Read Archive (DRA)と呼ばれることも。 
- 次世代シークエンサーのデータは以下の3つに収められている
    - Next Generation reads (=SRA)
    - Samples
    - Studies 

上述以外のDB(GEOやPubMedなど)はINSDCの枠外＝データ交換などがなされていない


### RefSeq

- DDBJ/EMBL/GenBankに登録されたデータを **NCBIが独自に** curationした二次データベース
	- RefSeqはINSDには入ってないが、DDBJからもリンクしているDBCLS謹製の[GGRNA](http://ggrna.dbcls.jp/)を使うと検索可能
- 【統合TV】 遺伝子のRefSeq IDを調べ、そのmRNA、アミノ酸配列を取得する http://doi.org/10.7875/togotv.2017.086 

----

## <a name="sa">配列アラインメント</a>

配列解析の基本である配列アラインメントについて、BLASTを例にその検索アルゴリズムを解説する。

### 大域的アラインメントと局所的アラインメント

![大域的アラインメントと局所的アラインメント](http://upload.wikimedia.org/wikipedia/commons/4/4b/Global-local-alignment.png)

- 大域的アラインメント(Global alignment)
	- 配列中の全塩基(アミノ酸)がアラインされるようにしたもの
	- Needleman-Wunsch algorithm
- 局所的アラインメント(Local alignment)
	- 部分的な類似が見つけられるようにしたもの
	- Smith-Waterman algorithm
	- Goad-Kanehisa algorithm
	- 配列類似性検索へ応用
		- [なぜ相同性じゃなく類似性か](http://togetter.com/li/307635)

#### 【実習2】BLAST

- BLASTとは
	- Basic Local Alignment Search Tool
	- 配列類似性検索のデファクトスタンダード
- BLASTの動作原理
	- 質問配列(Query)
	- 検索対象DB(Sbjct)

[![https://gyazo.com/d832c82d9dc711abbfe0c7ef8951e72f](https://i.gyazo.com/d832c82d9dc711abbfe0c7ef8951e72f.png)](https://gyazo.com/d832c82d9dc711abbfe0c7ef8951e72f)

- 質問配列とDBの組み合わせ→使うプログラム名が異なる
	- blastnだけが核酸配列レベルでの比較
	- 残り全てはアミノ酸配列レベルの比較

[![https://gyazo.com/1b65876d8b7842b6428a1706e1927b52](https://i.gyazo.com/1b65876d8b7842b6428a1706e1927b52.png)](https://gyazo.com/1b65876d8b7842b6428a1706e1927b52)

1. **"BLAST"** でググって、そのトップページを開く。

#### 【応用2】BLAT

### 多重配列アラインメントと分子系統樹

#### 【実習3】Clustalω

#### 【応用3】mafft

## <a name="pmd">タンパク質モチーフ・ドメイン検索</a>

### 【実習4】Pfam

### 【応用4】InterPro
