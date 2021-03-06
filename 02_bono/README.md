# ゲノムデータベースとそれを活用した配列解析入門 at AJACS筑波4

[情報・システム研究機構](http://www.rois.ac.jp) [データサイエンス共同利用基盤施設](https://ds.rois.ac.jp) [ライフサイエンス統合データベースセンター](https://dbcls.rois.ac.jp)
[坊農 秀雅](http://data.dbcls.jp/~bono/) bono@dbcls.rois.ac.jp  
2018年7月10日 11:10-14:10

----

これは統合データベース講習会AJACS筑波4「ゲノムデータベースとそれを活用した配列解析入門」の資料です。

© 2018 DBCLS, licensed under [Creative Commons Attribution 4.0 International license (CC-BY-4.0)](https://creativecommons.org/licenses/by/4.0/)

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
- [配列解析入門](#sa)
  - [大域的アラインメントと局所的アラインメント](#psa)
    - 【実習2】BLAST
    - 【応用2】BLAT
  - [多重配列アラインメントと分子系統樹](#msa)
    - 【実習3】Clustal Omega
    - 【応用3】mafft
  - [タンパク質モチーフ・ドメイン検索](#pmd)
  	- 【実習4】Pfam
  	- 【応用4】InterPro
    
参考図書：[Dr. Bonoの生命科学データ解析](https://www.amazon.co.jp/dp/4895929019/)

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
### [統合TV](https://dbcls.rois.ac.jp/services.html#TogoTV_ja)とは？
- 生命科学分野の有用なデータベースやツールの使い方を動画で紹介するウェブサイト http://togotv.dbcls.jp/

[![Image from Gyazo](https://i.gyazo.com/64aee461a45a447ecfad95be2dcd42ef.jpg)](https://gyazo.com/64aee461a45a447ecfad95be2dcd42ef)

- **本講習のすべての課題** に対応するチュートリアル動画が統合TVがあります
	- ウェブサイトへのアクセスから結果の見方まで、操作の一挙手一投足がわかります。
	- 講義・講習などの参考資料や後輩指導の教材として利用できます。
    - 本講習中、本家サイトが繋がらない時は、統合TVのYouTube版を見ればおおよその内容がわかるようになっています。
    - その他、今回の講習に関連する内容の多くは、[「ゲノム、核酸配列・構造解析」のカテゴリ](http://togotv.dbcls.jp/genome.html)にあります。
 - **過去の講習会の内容はそのほとんどが統合TVに収録**されており、いつでもどこでも**繰り返し復習できる**ようになっています。
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
4. Genome Browserのページが開くので、生物種(**Human**)とアッセンブリ(**Feb.2009/(GRC37/hg19)**)を選んで、検索語を入力する。[![https://gyazo.com/05ab6f4871c60485d4c54828a7f5f972](https://i.gyazo.com/05ab6f4871c60485d4c54828a7f5f972.png)](https://gyazo.com/05ab6f4871c60485d4c54828a7f5f972)
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

- アクセッション番号
	- INSDの登録(accession)番号（例: AB016472.1）
		- 論文掲載の必須条件
		- データを他の研究者に再利用してもらうことが研究の価値を高める上でとても大事
	- 日本だとDDBJへ。日本語でのやりとり可

#### DDBJ/EMBL/GenBank
- 今はAnnotated sequencesと呼ばれている昔からあるDB

#### Sequence Read Archive (SRA)
- SRAデータも交換されている
  - DDBJにもあるので、そこから取ると早くダウンロードできる。
  - DDBJではDDBJ Sequence Read Archive (DRA)と呼ばれることも。 
- 次世代シークエンサーのデータは以下の3つに収められている
    - [Next Generation reads (=SRA or DRA)](https://www.ddbj.nig.ac.jp/dra/index.html)
    - [Samples](https://www.ddbj.nig.ac.jp/biosample/index.html)
    - [Studies](https://www.ddbj.nig.ac.jp/bioproject/index.html) 

上述以外のDB(GEOやPubMedなど)はINSDCの枠外＝データ交換などがなされていない


### RefSeq

- DDBJ/EMBL/GenBankに登録されたデータを **NCBIが独自に** curationした二次データベース
	- RefSeqはINSDには入ってないが、DDBJからもリンクしているDBCLS謹製の[GGRNA](http://ggrna.dbcls.jp/)を使うと検索可能
- 【統合TV】 遺伝子のRefSeq IDを調べ、そのmRNA、アミノ酸配列を取得する http://doi.org/10.7875/togotv.2017.086 

----

## <a name="sa">配列解析入門</a>

配列解析の基本である配列アラインメントについて、BLASTを例にその検索アルゴリズムを解説する。

- ファイルフォーマット

| ファイルフォーマット | ファイル拡張子|用途など|
|----|----|----|
|FASTA	| .fa .fasta | 塩基配列、アミノ酸配列 |
|FASTQ|	.fq .fastq | NGSからの塩基配列とそのquality |
|DDBJ(Genbank)|	.dbj (.gbk) | メタデータを含んだ塩基配列やアミノ酸配列の記述 |
|SRA|	.sra | FASTQを圧縮したファイル形式|
|SAM/BAM|	.sam .bam |リファレンスゲノム配列へのアラインメント|
|GFF(GTF)|	.gff .gtf |ゲノムアノテーション|
|BED|	.bed |ゲノムアノテーション|
|VCF|	.vcf |バリアントの記述|

### <a name="psa">大域的アラインメントと局所的アラインメント</a>

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

#### BLAST

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

#### 【実習2】BLAST

1. **"NCBI BLAST"** でググって、そのトップページを開く 
[![https://gyazo.com/3533a201cd0309b58da2a344b8a4d552](https://i.gyazo.com/3533a201cd0309b58da2a344b8a4d552.png)](https://gyazo.com/3533a201cd0309b58da2a344b8a4d552)
2. Nucleotide BLASTを選ぶ 
[![https://gyazo.com/3f19305b9ec6f99922af952ee1f7c340](https://i.gyazo.com/3f19305b9ec6f99922af952ee1f7c340.png)](https://gyazo.com/3f19305b9ec6f99922af952ee1f7c340)
3. FASTA sequence(query)をペーストする。興味ある配列がない場合は、[例1](http://getentry.ddbj.nig.ac.jp/getentry/na/LC170036/?format=fasta&filetype=html&trace=true&show_suppressed=false&limit=10)か[例2](http://getentry.ddbj.nig.ac.jp/getentry/na/AB281053/?format=fasta&filetype=html&trace=true&show_suppressed=false&limit=10)を使いましょう。
4. 検索対象DBを選ぶ。まずは、デフォルトのまま(nr/nt)で。
5. BLASTボタンを押すと、検索が始まり、以下のような結果が得られる。
[![https://gyazo.com/3aa5210a48beb6d0efb1634b16e119f7](https://i.gyazo.com/3aa5210a48beb6d0efb1634b16e119f7.png)](https://gyazo.com/3aa5210a48beb6d0efb1634b16e119f7)
[![https://gyazo.com/00a4946753a82898c6370643d152cd4e](https://i.gyazo.com/00a4946753a82898c6370643d152cd4e.png)](https://gyazo.com/00a4946753a82898c6370643d152cd4e)
[![https://gyazo.com/25e505d625c7b585cd8befa67909158f](https://i.gyazo.com/25e505d625c7b585cd8befa67909158f.png)](https://gyazo.com/25e505d625c7b585cd8befa67909158f)
6. 検索対象DBを'Human genomic + transcript'にするなど、パラメータを変えて検索してみよう。

##### 【復習】NCBI BLASTの統合TV

- NCBI BLASTの使い方〜基本編〜2017 https://doi.org/10.7875/togotv.2017.023

##### 【発展】localBLASTと配列操作
- 大量にBLAST検索する際には自分のパソコンにインストールして使う(**localBLAST**)
	- Local BLASTの使い方〜導入・準備編(MacOSX版)〜2017 https://doi.org/10.7875/togotv.2017.031
	- Local BLASTの使い方〜検索実行・オプション(MacOSX版)〜2017 https://doi.org/10.7875/togotv.2017.045
- その際に必要になっている配列やファイル操作はBiopythonで処理することも
	- https://qiita.com/search?q=biopython
	- https://youtu.be/FQabMlA5esM?t=2h55m04s

#### BLAT

- The BLAST-like alignment tool
- DBがgenomeに特化した配列類似性検索
	- genome landing toolとも呼ばれる
- 企業には有償のライセンス
	- 依然としてBLASTを使う例も多く

#### 【応用2】BLAT

BLASTと同じ検索を、BLATを用いてやってみよう。統合TVを参考に。
- 【統合TV】UCSC BLATを使って、ウイルスの持ち出した宿主の遺伝子配列がコードされている領域をアミノ酸配列レベルでゲノム中から探し当てる　 https://doi.org/10.7875/togotv.2017.124


### <a name="msa">多重配列アラインメントと分子系統樹</a>

3本以上の配列でできる限りギャップを入れないようにして、似たアミノ酸や塩基を並べる手法が多重配列アラインメント(multiple sequence alignment)である。

#### 【実習3】Clustal Omega

これまで広く使われてきたClustalWという多重配列アラインメントソフトウェアの後継がClustal Omegaである。


1. **clustal omega** でググって、[そのトップページ(EBIのサイト)](https://www.ebi.ac.uk/Tools/msa/clustalo/)を開く
[![https://gyazo.com/8e04289430f4608fd5f426fb85c47a91](https://i.gyazo.com/8e04289430f4608fd5f426fb85c47a91.png)](https://gyazo.com/8e04289430f4608fd5f426fb85c47a91)
2. 多重配列アラインメントしたい配列群(multi-FASTAフォーマット)を貼り付ける（[テスト配列（真核高等生物のHIF1A）](https://raw.githubusercontent.com/AJACS-training/AJACS70/master/02_bono/HIF1A.txt)）
[![https://gyazo.com/1dc45c4c68badee0e2b7af0b2db12d0e](https://i.gyazo.com/1dc45c4c68badee0e2b7af0b2db12d0e.png)](https://gyazo.com/1dc45c4c68badee0e2b7af0b2db12d0e)
3. Submitを押して計算結果が得られるのを待つ
4. しばらく待つと以下のような多重配列アラインメントが得られる
[![https://gyazo.com/f06e0e06226e8d992f5bc570991e0ada](https://i.gyazo.com/f06e0e06226e8d992f5bc570991e0ada.png)](https://gyazo.com/f06e0e06226e8d992f5bc570991e0ada)
5. Phylogenetic Treeを押すと分子系統樹が得られ、Tree Dataにあるファイルを使って他の系統樹描画ソフトウェアで利用することもできる
[![https://gyazo.com/f514194cf26002a70ab2b2eb5322b7da](https://i.gyazo.com/f514194cf26002a70ab2b2eb5322b7da.png)](https://gyazo.com/f514194cf26002a70ab2b2eb5322b7da)
6. Download Alignment Fileを押すと、この結果がテキスト形式で得られる


##### 【復習】Clustal Omegaの統合TV

- Clustal Omegaを使ってマルチプルアラインメントを行う　 https://doi.org/10.7875/togotv.2015.019

#### 【応用3】mafft

Clustal Omegaと同じマルチプルアラインメントを、MAFFTを使ってやってみよう。以下の統合TVを参考に。
- 【統合TV】MAFFTを使ってマルチプルアラインメントを行う 　https://doi.org/10.7875/togotv.2015.035

### <a name="pmd">タンパク質モチーフ・ドメイン検索</a>

#### 【実習4】InterProとPfam
InterProは数多くあるタンパク質モチーフやドメインの統合データベースです。

1. **interproscan** でググって、[そのトップページ(EBIのサイト)](https://www.ebi.ac.uk/interpro/search/sequence-search)を開く
[![https://gyazo.com/965eb18e02f6187d562ca82769ba0e5a](https://i.gyazo.com/965eb18e02f6187d562ca82769ba0e5a.png)](https://gyazo.com/965eb18e02f6187d562ca82769ba0e5a)
2. 検索したいタンパク質配列を貼り付ける。自らの配列を持ってない場合は、[上で使ったテスト配列（真核高等生物のHIF1A）の一番先頭のエントリだけをコピー＆ペーストしてみましょう](https://raw.githubusercontent.com/AJACS-training/AJACS70/master/02_bono/HIF1A.txt)
3. Submitを押してしばらく待つ。サーバーの混み具合によっては、時間がかかるときもあります。
[![https://gyazo.com/cb6e94df908c5cdd62f6ae6be11d146a](https://i.gyazo.com/cb6e94df908c5cdd62f6ae6be11d146a.png)](https://gyazo.com/cb6e94df908c5cdd62f6ae6be11d146a)
4. 結果が得られる
[![https://gyazo.com/a83b60680841f2134da300a775921f9e](https://i.gyazo.com/a83b60680841f2134da300a775921f9e.png)](https://gyazo.com/a83b60680841f2134da300a775921f9e)
5. PFで始まるIDがPfamのエントリです。クリックしてみましょう。
[![https://gyazo.com/0b7f8655899a33348e21185776948425](https://i.gyazo.com/0b7f8655899a33348e21185776948425.png)](https://gyazo.com/0b7f8655899a33348e21185776948425)
6. 左のタブの'Domain organisation'をクリックするとこのドメインを持つ公共DB中のタンパク質がそのドメイン構成とともに表示されます
[![https://gyazo.com/238a2a6347f1495d4a0225e0e7c8579a](https://i.gyazo.com/238a2a6347f1495d4a0225e0e7c8579a.png)](https://gyazo.com/238a2a6347f1495d4a0225e0e7c8579a)

##### 【復習】InterProとPfamの統合TV

- Pfamを使ってタンパク質のドメインを調べる 2017　http://doi.org/10.7875/togotv.2017.125


#### 【応用4】DoMosaics

手持ちのタンパク質配列セットに対して、そのドメイン構造をPfamのDB全てに対して検索し、それらの系統関係もローカルに計算して併せて表示するというツールです。実行にはJavaのプログラムが実行できる環境が必要です。

- 【統合TV】 DoMosaicsを使ってドメイン構造と系統樹を可視化する http://doi.org/10.7875/togotv.2017.077

----
