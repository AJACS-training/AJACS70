# 統合データベース講習会：AJACS筑波４
* 日時：2018年7月10日（火）14:20-15:50
* 会場：物質・材料研究機構 千現地区研究本館1階第2会議室
# 「**化合物データベース**」

* 公益財団法人野口研究所　山田一作（やまだいっさく） issaku@noguchi.or.jp

# 内容

1. 概要
2. 関連データ
3. 表記
4. ファイル形式
5. 使ってみよう
6. ツール

# 1. 概要

## 化合物データベース

* 化合物とは？

    化合物には[有機化合物](https://ja.wikipedia.org/wiki/%E6%9C%89%E6%A9%9F%E5%8C%96%E5%90%88%E7%89%A9)や[無機化合物](https://ja.wikipedia.org/wiki/%E7%84%A1%E6%A9%9F%E5%8C%96%E5%90%88%E7%89%A9)が含まれます。
    本講習会で扱う化合物は、主に原子数1000以下の低分子有機化合物です。

* 化合物データベースのリスト
    * [Integbioデータベースカタログ](https://integbio.jp/dbcatalog/?lang=ja) https://integbio.jp/dbcatalog/?lang=ja
        * 文部科学省、厚生労働省、農林水産省、経済産業省による、生命科学系データベース統合のための合同ポータルサイト内のDBカタログ事業
        [![https://gyazo.com/5c7c1df9b4e588869d4dd75becbb1cd3](https://i.gyazo.com/5c7c1df9b4e588869d4dd75becbb1cd3.png)](https://gyazo.com/5c7c1df9b4e588869d4dd75becbb1cd3)
        
        * [国内](https://integbio.jp/dbcatalog/dbsearch?cck=database_catalog&order_ja=1&dbcat_search_all=&tag2=%7C%E5%8C%96%E5%AD%A6%E7%89%A9%E8%B3%AA%7C&tag3=&inst_country=%E6%97%A5%E6%9C%AC&inst_country_others=&dbarchive=&data_downloadable=&togotv=&biosharing=&record_creation=&status=&dbcat_ministry=&taxonomy=&search=database_catalog_search&task=search)
        [![https://gyazo.com/7dee15fc0240cd48940437eecce943a3](https://i.gyazo.com/7dee15fc0240cd48940437eecce943a3.png)](https://gyazo.com/7dee15fc0240cd48940437eecce943a3)
        
        * [日本以外の国地域](https://integbio.jp/dbcatalog/dbsearch?cck=database_catalog&order_ja=1&dbcat_search_all=&tag2=%7C%E5%8C%96%E5%AD%A6%E7%89%A9%E8%B3%AA%7C&tag3=&inst_country=&inst_country_others=%E6%97%A5%E6%9C%AC&dbarchive=&data_downloadable=&togotv=&biosharing=&record_creation=&status=&dbcat_ministry=&taxonomy=&search=database_catalog_search&task=search)
        [![https://gyazo.com/99b1cc815a04a5d7b6ab9ff402a74568](https://i.gyazo.com/99b1cc815a04a5d7b6ab9ff402a74568.png)](https://gyazo.com/99b1cc815a04a5d7b6ab9ff402a74568)
    
    * 本講習会ではPubChemの使い方を説明します。
    [![https://gyazo.com/d77c84c047e124715010673ce529bb34](https://i.gyazo.com/d77c84c047e124715010673ce529bb34.png)](https://gyazo.com/d77c84c047e124715010673ce529bb34)
        * [PubChem Substance](https://integbio.jp/dbcatalog/record/nbdc00642)
        * [PubChem Compound](https://integbio.jp/dbcatalog/record/nbdc00641)
        * [PubChem BioAssay](https://integbio.jp/dbcatalog/record/nbdc00640)




# 2. 関連データ

## [化学構造式](https://ja.wikipedia.org/wiki/%E5%8C%96%E5%AD%A6%E5%BC%8F#%E6%A7%8B%E9%80%A0%E5%BC%8F)


* 原子の元素記号と単結合（一重線）、二重結合（二重線）、三重結合（三重線）を組み合わせて分子構造を表す。 


    [![Image from Gyazo](https://i.gyazo.com/8ae8b941097efe826cff8f9a2e4cb469.png)](https://gyazo.com/8ae8b941097efe826cff8f9a2e4cb469)

    * [デオキシアデノシン](https://pubchem.ncbi.nlm.nih.gov/compound/2_-deoxyadenosine#section=Top)

## 物性値（[沸点](https://ja.wikipedia.org/wiki/%E6%B2%B8%E7%82%B9)、[融点](https://ja.wikipedia.org/wiki/%E8%9E%8D%E7%82%B9)、[溶解度](https://ja.wikipedia.org/wiki/%E6%BA%B6%E8%A7%A3%E5%BA%A6)）

## [バイオアッセイ](https://ja.wikipedia.org/wiki/%E3%83%90%E3%82%A4%E3%82%AA%E3%82%A2%E3%83%83%E3%82%BB%E3%82%A4)

## 化合物同定

* [核磁気共鳴分光法](https://ja.wikipedia.org/wiki/%E6%A0%B8%E7%A3%81%E6%B0%97%E5%85%B1%E9%B3%B4%E5%88%86%E5%85%89%E6%B3%95)

* [質量分析法](https://ja.wikipedia.org/wiki/%E8%B3%AA%E9%87%8F%E5%88%86%E6%9E%90%E6%B3%95)

## 安全性
* 有害性情報、法規制情報など
    * 独立行政法人製品評価技術基盤機構 (NITE) 化学物質総合情報提供システム
        * 化学物質の番号や名称等から、有害性情報、法規制情報及び国際機関によるリスク評価情報等を検索することができるシステム
        * https://www.nite.go.jp/chem/chrip/chrip_search/srhInput
* [化学物質等安全データシート (Safety Data Sheet, SDS)](https://ja.wikipedia.org/wiki/%E5%AE%89%E5%85%A8%E3%83%87%E3%83%BC%E3%82%BF%E3%82%B7%E3%83%BC%E3%83%88)
    * 一般社団法人日本試薬協会 SDS検索
        * https://www.j-shiyaku.or.jp/Sds

## その他



# 3. 表記

* [IUPAC命名法](http://www.sbcs.qmul.ac.uk/iupac/)
    * 化合物を命名する際の基本となる、国際純正・応用化学連合（International Union of Pure and Applied Chemistry、IUPAC)の命名法
    * 化学構造式が複雑な化合物になると正しい命名をするのが簡単ではない。

    * [日本語による化合物命名法](http://cicsj.chemistry.or.jp/14_5/hata.html)
        * http://cicsj.chemistry.or.jp/14_5/hata.html

    * (2*R*,3*S*,5*R*)-5-(6-aminopurin-9-yl)-2-(hydroxymethyl)oxolan-3-ol

    ---

* 慣用名

    * `デオキシアデノシン`
    * `2'-deoxyadenosine`

    ---

* ID

    * PubChem Compound CID
        * 0-9の数字のみでを利用
    * PubChem Substance SID
        * 0-9の数字のみでを利用

    * [CAS 登録番号](https://www.jaici.or.jp/casproducts/rn/index.html)
    * その他のデータベースのID

    ---

* SMILES

    * `C1[C@@H]([C@H](O[C@H]1N2C=NC3=C2N=CN=C3N)CO)O`
    * 混合物の場合
        `CO.CCO.OCCC.C1CCCCC1.C2=CC=CC=C2`

    ---

* CTFile (Molfile, SDfile)

    * 古くから利用されている。バージョンとしてV2000とV3000がある。一般的にはV2000が利用されているが、原子数、結合数が各999個までの制限がある。V3000にはこの制限はない。
    * ファイル形式の説明でもう少し詳しく説明します。

    ---

*  IUPAC International Chemical Identifier (InChI<sup>TM</sup>)

    * `InChI=1S/C10H13N5O3/c11-9-8-10(13-3-12-9)15(4-14-8)7-1-5(17)6(2-16)18-7/h3-7,16-17H,1-2H2,(H2,11,12,13)/t5-,6+,7+/m0/s1`

    ---

* InChIKey

    * `OLXZPDWKRNYJJZ-RRKCRQDMSA-N`

    ---


# 4. ファイル形式

* .smi
    * SMILESを格納、複数行にSMILESを記載することで一つのファイルに複数の化学構造を記述することができる。

```
CO
CCO
OCCC
C1CCCCC1
C2=CC=CC=C2
```

[![Image from Gyazo](https://i.gyazo.com/3dba74f046db054537dd620752484de1.png)](https://gyazo.com/3dba74f046db054537dd620752484de1)

---

* .mol

```
887
  -OEChem-07031813262D

  6  5  0     0  0  0  0  0  0999 V2000
    2.5369   -0.2500    0.0000 O   0  0  0  0  0  0  0  0  0  0  0  0
    3.4030    0.2500    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
    3.7130   -0.2869    0.0000 H   0  0  0  0  0  0  0  0  0  0  0  0
    3.9399    0.5600    0.0000 H   0  0  0  0  0  0  0  0  0  0  0  0
    3.0930    0.7869    0.0000 H   0  0  0  0  0  0  0  0  0  0  0  0
    2.0000    0.0600    0.0000 H   0  0  0  0  0  0  0  0  0  0  0  0
  1  2  1  0  0  0  0
  1  6  1  0  0  0  0
  2  3  1  0  0  0  0
  2  4  1  0  0  0  0
  2  5  1  0  0  0  0
M  END
```

[![Image from Gyazo](https://i.gyazo.com/80b795c3979bead01535bde52d9c863b.png)](https://gyazo.com/80b795c3979bead01535bde52d9c863b)

---

* .sdf

```
887
  -OEChem-07031813262D

  6  5  0     0  0  0  0  0  0999 V2000
    2.5369   -0.2500    0.0000 O   0  0  0  0  0  0  0  0  0  0  0  0
    3.4030    0.2500    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
    3.7130   -0.2869    0.0000 H   0  0  0  0  0  0  0  0  0  0  0  0
    3.9399    0.5600    0.0000 H   0  0  0  0  0  0  0  0  0  0  0  0
    3.0930    0.7869    0.0000 H   0  0  0  0  0  0  0  0  0  0  0  0
    2.0000    0.0600    0.0000 H   0  0  0  0  0  0  0  0  0  0  0  0
  1  2  1  0  0  0  0
  1  6  1  0  0  0  0
  2  3  1  0  0  0  0
  2  4  1  0  0  0  0
  2  5  1  0  0  0  0
M  END
> <PUBCHEM_COMPOUND_CID>
887

> <PUBCHEM_IUPAC_INCHI>
InChI=1S/CH4O/c1-2/h2H,1H3

> <PUBCHEM_IUPAC_INCHIKEY>
OKKJLVBELUTLKV-UHFFFAOYSA-N

$$$$
888
  -OEChem-07031813262D

  6  5  0     0  0  0  0  0  0999 V2000
    2.5369   -0.2500    0.0000 O   0  0  0  0  0  0  0  0  0  0  0  0
    ...
    ...
$$$$
```


[![Image from Gyazo](https://i.gyazo.com/4eecaa26d46c6eb4840f829507578677.png)](https://gyazo.com/4eecaa26d46c6eb4840f829507578677)

* [他の形式例](http://openbabel.org/docs/2.3.0/FileFormats/Overview.html)


# 5. 使ってみよう

## PubChem

* PubChemとは？



    * 統合TVを見てみましょう
        * [2017-12-08 PubChemを利用して化学物質やアッセイの結果を調べる 2017]( http://togotv.dbcls.jp/20171208.html)
            * http://togotv.dbcls.jp/20171208.html
[![Image from Gyazo](https://i.gyazo.com/dd9616fac93a903519ba6e8e7cca85fc.png)](https://gyazo.com/dd9616fac93a903519ba6e8e7cca85fc)

* [Compound, Substance, BioAssay](https://pubchemdocs.ncbi.nlm.nih.gov/about)

    * Substance   SID (SubstanceID)
    * Compound    CID (CompoundID)
    * BioAssay    AID (AssayID)

        [![Image from Gyazo](https://i.gyazo.com/1be913ae900eaca8772cdfde5bca42c2.png)](https://gyazo.com/1be913ae900eaca8772cdfde5bca42c2)

* [Data Sources](https://pubchem.ncbi.nlm.nih.gov/sources)

* [Chemical structure representation in PubChem](https://www.slideshare.net/NextMoveSoftware/chemical-structure-representation-in-pubchem?from_action=save)

---

## ブラウザからの利用

### 化合物のページ

* [ゲフィチニブ（Gefitinib)](https://pubchem.ncbi.nlm.nih.gov/compound/123631#section=Top)

* [beta-D-Glucopyranose](https://pubchem.ncbi.nlm.nih.gov/compound/beta-D-glucose#section=Top)

---

### データの取得方法

## [PubChem’s PUG (Power User Gateway)](http://pubchemdocs.ncbi.nlm.nih.gov/programmatic-access)

* [PUG-REST](https://pubchemdocs.ncbi.nlm.nih.gov/pug-rest)

    * URL

    `https://pubchem.ncbi.nlm.nih.gov/rest/pug/<input specification>/<operation specification>/[<output specification>][?<operation_options>]`

    * レコード検索

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/sourceid/DTP.NCI/747285/SDF

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/sourceid/DTP.NCI/747285/PNG

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/2244/SDF

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/2244/PNG

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/2244/SDF?record_type=3d

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/2244/PNG?record_type=3d&image_size=small

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/name/aspirin/SDF

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/inchikey/BPGDAMSIGCZZLK-UHFFFAOYSA-N/SDF

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/1000/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/1000/CSV?sid=26736081,26736082,26736083

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/1000/concise/CSV

    * Compound Property Tables

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/1,2,3,4,5/property/MolecularFormula,MolecularWeight,InChIKey/CSV

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/1,2,3,4,5/property/MolecularFormula,MolecularWeight,InChIKey/JSON

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/1,2,3,4,5/property/IsomericSMILES,XLogP,TPSA,HBondDonorCount,HBondAcceptorCount,RotatableBondCount,AtomStereoCount,BondStereoCount/JSON

    * Synonyms

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/name/aspirin/synonyms/JSON

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/smiles/CCCC/synonyms/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/sid/53789435/synonyms/TXT

    * Description

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/1983/description/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/1983/description/JSON


    * SIDS / CIDS / AIDS

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/name/glucose/sids/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/name/glucose/sids/XML?list_return=listkey

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/name/glucose/cids/XML?list_return=grouped

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/name/glucose/cids/XML?list_return=flat

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/sourceall/MLSMR/sids/JSON?list_return=listkey

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/sourceall/R%26D%20Chemicals/sids/XML?list_return=listkey

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/sid/123061,123079/cids/XML?cids_type=all

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/2244/sids/JSON

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/192180/cids/TXT?cids_type=component

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/2244/aids/JSON?aids_type=active

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/2244/sids/JSON?sids_type=component

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/2244/cids/TXT?cids_type=same_connectivity

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/21145249/cids/XML?cids_type=parent

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/1000/sids/XML?sids_type=inactive

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/504526/sids/JSON?sids_type=doseresponse

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/type/doseresponse/aids/JSON

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/sourceall/DTP.NCI/aids/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/xref/PatentID/EP0711162A1/sids/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/name/myxalamid/cids/XML?name_type=word

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/name/myxalamid/cids/XML?name_type=complete

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/target/genesymbol/USP2/aids/TXT

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/target/gi/116516899/aids/JSON

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/activity/EC50/aids/TXT

    * Assay Description

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/490/description/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/490/description/JSON

    * Assay Targets

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/490,1000/targets/ProteinGI,ProteinName,GeneID,GeneSymbol/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/490,1000/targets/ProteinGI,ProteinName,GeneID,GeneSymbol/JSON

    * Assay Summary

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/1000,1001/assaysummary/CSV

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/sid/104234342/assaysummary/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/sid/104234342/assaysummary/JSON

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/1000/summary/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/1000/summary/JSON

    * Assay Dose-Response

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/504526/doseresponse/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/504526/doseresponse/CSV?sid=104169547,109967232

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/assay/aid/602332/sids/XML?sids_type=doseresponse&list_return=listkey

    * Classification

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/sid/1917/classification/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/cid/1983/classification/JSON?classification_type=original

    * XRefs

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/substance/sid/127378063/xrefs/PatentID/XML

        https://pubchem.ncbi.nlm.nih.gov/rest/pug/compound/name/vioxx/xrefs/RegistryID,RN,PubMedID/JSONP

    * Example Scripts

        * [pug_rest_scripts_nar_2018.zip](https://pubchemdocs.ncbi.nlm.nih.gov/pug-rest$example_scripts)

---

* [PUG-SOAP](https://pubchemdocs.ncbi.nlm.nih.gov/pug-soap)

    * web service definition language (WSDL)
        * https://pubchem.ncbi.nlm.nih.gov/pug_soap/pug_soap.cgi?wsdl
    * PUG SOAP Client Help
        * https://pubchem.ncbi.nlm.nih.gov/pug_soap/client_help.html

        [![Image from Gyazo](https://i.gyazo.com/48e67fd5c2f87368065df64cc65a417d.png)](https://gyazo.com/48e67fd5c2f87368065df64cc65a417d)

---


## [PubChemRDF](http://pubchemdocs.ncbi.nlm.nih.gov/rdf)

*  RESTful Interface

    `curl -L -H "Accept: text/rdf" -o CID2244.rdf http://rdf.ncbi.nlm.nih.gov/pubchem/compound/CID2244`

    http://rdf.ncbi.nlm.nih.gov/pubchem/compound/CID2244.rdf

    http://rdf.ncbi.nlm.nih.gov/pubchem/compound/CID2244.html

    http://rdf.ncbi.nlm.nih.gov/pubchem/compound/CID2244.turtle

    http://rdf.ncbi.nlm.nih.gov/pubchem/compound/CID2244.json

    http://rdf.ncbi.nlm.nih.gov/pubchem/compound/CID2244.jsonld

    http://rdf.ncbi.nlm.nih.gov/pubchem/compound/CID2244.ntriples

* Query RESTful Interface

    https://pubchem.ncbi.nlm.nih.gov/rest/rdf/query?graph=synonym&name=aspirin

    https://pubchem.ncbi.nlm.nih.gov/rest/rdf/query?graph=synonym&name=aspirin&contain=true

    https://pubchem.ncbi.nlm.nih.gov/rest/rdf/query?graph=synonym&name=aspirin&return=compound

    https://pubchem.ncbi.nlm.nih.gov/rest/rdf/query?graph=synonym&name=aspirin&format=json

    https://pubchem.ncbi.nlm.nih.gov/rest/rdf/query?graph=substance&predicate=rdf:type&offset=10000

    https://pubchem.ncbi.nlm.nih.gov/rest/rdf/query?graph=synonym&pred=rdf:type&obj=sio:CHEMINF_000561

    https://pubchem.ncbi.nlm.nih.gov/rest/rdf/query?graph=synonym&pred=rdf:type&object=sio:CHEMINF_000446,sio:CHEMINF_000447&offset=1275000

---

* [Classification Browser](https://pubchem.ncbi.nlm.nih.gov/classification/#hid=1)

        * オントロジーや分類法から、化合物のデータセットを絞り込み、絞り込んだデータセットをダウンロードすることができます。
    
    1. 右の`Classification`をクリック
    [![Image from Gyazo](https://i.gyazo.com/02deb07e9c325c38e1a845427a839e2f.png)](https://gyazo.com/02deb07e9c325c38e1a845427a839e2f)

    2. `Select classification`から、データセットを選ぶ。
    [![Image from Gyazo](https://i.gyazo.com/8171df0099bdaaebae99420f83521439.png)](https://gyazo.com/8171df0099bdaaebae99420f83521439)

    3. 今回はChEBIを選択してみます。
    [![Image from Gyazo](https://i.gyazo.com/c3db102bfc7449a9266358e1c293a5e2.png)](https://gyazo.com/c3db102bfc7449a9266358e1c293a5e2)

    4. `Data type counts to display`で、`Substance`と`Compound`を切り替えると、下のカウントの数値が変わります。

    5. Treeの ▶ をクリックして、目的のセットを探します。
    [![Image from Gyazo](https://i.gyazo.com/af8d4ddf8e5f2a03bd0cdbcc24104e41.png)](https://gyazo.com/af8d4ddf8e5f2a03bd0cdbcc24104e41)

    6. 5.以外の方法として、`Search selected classification by`で、`Keyword`を選択（デフォルト）で、キーワード（ここでは、`glycolipid`）を入力し`Search`します。
    [![Image from Gyazo](https://i.gyazo.com/ec239987348227ce88abf784c43a002d.png)](https://gyazo.com/ec239987348227ce88abf784c43a002d)

    7. `Classification`の左のプラスのアイコンをクリックします。
    [![Image from Gyazo](https://i.gyazo.com/b512fa324124aade67907f5c7bf4ef5f.png)](https://gyazo.com/b512fa324124aade67907f5c7bf4ef5f)

    8. 展開された状態で、ブラウザの検索機能で`glycolipid`を検索します。
    [![Image from Gyazo](https://i.gyazo.com/1ee1f5b22e78d8e17aaddc6b4f87147b.png)](https://gyazo.com/1ee1f5b22e78d8e17aaddc6b4f87147b)

    9. 検索した`glycolipid`をクリックすると、ウインドウが開きます。`glycolipid`の左の青い数字をクリックします。
    [![Image from Gyazo](https://i.gyazo.com/0295c4554e5a972adb45b8930f7135f3.png)](https://gyazo.com/0295c4554e5a972adb45b8930f7135f3)

    10. 検索（選択）された化合物のリストが表示されます。右の`Structure Download`をクリックします。
    [![Image from Gyazo](https://i.gyazo.com/9b0d71c3e5475c34b26095a11c0f7d37.png)](https://gyazo.com/9b0d71c3e5475c34b26095a11c0f7d37)

    11. 検索（選択）した化合物のリストをダウンロードするためのサイトが開きます。必要に応じでformatなどを変更し、`Download`ボタンを押します。
    [![Image from Gyazo](https://i.gyazo.com/c6747251202079b73f1849eacc58f11a.png)](https://gyazo.com/c6747251202079b73f1849eacc58f11a)

    12. 自動的に選択した形式でデータのダウンロードが開始されます。この場合は、ファイル名`4363722229543774033.sdf.gz`としてダウンロードされます。
    [![Image from Gyazo](https://i.gyazo.com/2fee934fcd9fbac02c1e830c6724674e.png)](https://gyazo.com/2fee934fcd9fbac02c1e830c6724674e)

    13. ダウンロードされたファイルを解凍すると、エディタなどでデータを見ることができます。

    14. データセットとして、`Gene Ontology:　biological process`を選択してみます。Data typeとして、PubMed, Gene, Protein, Taxonomyが選択できるようになります。
    [![Image from Gyazo](https://i.gyazo.com/99754ac29478b468acd7dfe9231efa9e.png)](https://gyazo.com/99754ac29478b468acd7dfe9231efa9e)

    15. ここでは、Geneを選択し、Biological Process > metabolic process > glycosylation を選択してみます。

        [![Image from Gyazo](https://i.gyazo.com/91d7521e82dc98bafcb326d58e262eca.png)](https://gyazo.com/91d7521e82dc98bafcb326d58e262eca)

    16. glycosylationの右の「520」をクリックすると、新しいウインドウが開きます。Geneのリストが表示されます。Gene IDのリンクをクリックすると詳細画面を見ることができます。
    [![Image from Gyazo](https://i.gyazo.com/e04dbd581ed4173fd9664d4b7040c486.png)](https://gyazo.com/e04dbd581ed4173fd9664d4b7040c486)

    * SDFを選択した場合の例

        ```
        350080125
        -OEChem-07041809452D

        59 60  0     1  0  0  0  0  0999 V2000
        15.5021  -26.1389    0.0000 O   0  0  0  0  0  0  0  0  0  0  0  0
        17.2204  -26.1388    0.0000 O   0  0  0  0  0  0  0  0  0  0  0  0
        ...
        13.7741  -22.6873    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
        14.6327  -23.1842    0.0000 C   0  0  0  0  0  0  0  0  0  0  0  0
        1 12  1  0  0  0  0
        1 15  1  0  0  0  0
        ...
        56 57  1  0  0  0  0
        57 58  1  0  0  0  0
        58 59  1  0  0  0  0
        M  END
        ...
        > <PUBCHEM_SUBSTANCE_ID>
        350080125

        > <PUBCHEM_EXT_DATASOURCE_NAME>
        ChEBI

        > <PUBCHEM_EXT_DATASOURCE_REGID>
        CHEBI:139221

        > <PUBCHEM_SUBSTANCE_SYNONYM>
        CHEBI:139221
        N-[(1S,2S,3R)-1-[(alpha-D-galactopyranosyloxy)methyl]-2,3-dihydroxy-10-phenyldecyl]hexacosanamide
        N-[(2S,3S,4R)-1-(alpha-D-galactopyranosyloxy)-3,4-dihydroxy-11-phenylundecan-2-yl]hexacosanamide
        N-[(2S,3S,4R)-1-(alpha-D-galactosyloxy)-3,4-dihydroxy-11-phenylundecan-2-yl]hexacosanamide

        ...

        $$$$
        350080124
        -OEChem-07041809452D
        ...
        ```

    * SMILESを選択した場合の例
        * 化学構造がSMILESへ変換できない場合は、ID(SID)のみ出力されます。
    [![Image from Gyazo](https://i.gyazo.com/941f927ef7619cc3d7254e49fa79accb.png)](https://gyazo.com/941f927ef7619cc3d7254e49fa79accb)

        ```
        350080125 CCCCCCCCCCCCCCCCCCCCCCCCCC(=O)N[C@@H](CO[C@@H]1[C@@H]([C@H]([C@H]([C@H](O1)CO)O)O)O)[C@@H]([C@@H](CCCCCCCC2=CC=CC=C2)O)O
        350080124 CC(CC/C=C(\C)/CC/C=C(\C)/CC/C=C(\C)/CCC=C(C)C)CCOP(=O)(O)OP(=O)(O)O[C@@H]1[C@@H]([C@H]([C@@H]([C@H](O1)CO)O[C@H]2[C@@H]([C@H]([C@@H]([C@H](O2)CO)O[C@H]3[C@H]([C@H]([C@@H]([C@H](O3)CO[C@@H]4[C@H]([C@H]([C@@H]([C@H](O4)CO[C@@H]5[C@H]([C@H]([C@@H]([C@H](O5)CO)O)O)O[C@@H]6[C@H]([C@H]([C@@H]([C@H](O6)CO)O)O)O)O)O[C@@H]7[C@H]([C@H]([C@@H]([C@H](O7)CO)O)O)O[C@@H]8[C@H]([C@H]([C@@H]([C@H](O8)CO)O)O)O)O)O)O[C@@H]9[C@H]([C@H]([C@@H]([C@H](O9)CO)O)O)O[C@@H]1[C@H]([C@H]([C@@H]([C@H](O1)CO)O)O)O[C@@H]1[C@H]([C@H]([C@@H]([C@H](O1)CO)O)O)O)O)O)NC(=O)C)O)NC(=O)C
        332875751 
        329737157 CCCCCCCCCCCCCCCCCCCCCCCC(=O)N[C@@H](CO[C@H]1[C@@H]([C@H]([C@@H]([C@H](O1)CO)O[C@H]2[C@@H]([C@H]([C@H]([C@H](O2)CO)O[C@H]3[C@@H]([C@H]([C@H]([C@H](O3)CO)O)O)NC(=O)C)O[C@@]4(C[C@@H]([C@H](C(O4)[C@@H]([C@@H](CO)O[C@@]5(C[C@@H]([C@H](C(O5)[C@@H]([C@@H](CO)O)O)NC(=O)C)O)C(=O)O)O)NC(=O)C)O)C(=O)O)O)O)O)[C@@H](/C=C/CCCCCCCCCCCCC)O
        ...
        ```

    ---

* PubChem FTP

    * FTPサイトからデータセットをダウンロードすることができます。
    
    1. 右の`PubChem FTP`をクリック
    
    [![Image from Gyazo](https://i.gyazo.com/02deb07e9c325c38e1a845427a839e2f.png)](https://gyazo.com/02deb07e9c325c38e1a845427a839e2f)
    
    2. FTPサイトが表示されます。
    
    [![Image from Gyazo](https://i.gyazo.com/4ae0fb53636aa99a62b41acbf879a607.png)](https://gyazo.com/4ae0fb53636aa99a62b41acbf879a607)

    3. アッセイデータの例、AID-AID.zip のリストが表示されます。必要なデータをクリックするとダウンロードできます。
    
    [![Image from Gyazo](https://i.gyazo.com/d567b89af9b67ed9931f02604f42d864.png)](https://gyazo.com/d567b89af9b67ed9931f02604f42d864)

    4. 以下のようにディレクトリをたどると、Compoundの2018-06-28更新データをSDF形式でダウンロードできます。ダウンロードしたデータは、上述のように解凍することでエディタなどでデータを見ることができます。
    
    [![Image from Gyazo](https://i.gyazo.com/fa193c7fc567a0591ddcd05a53de847e.png)](https://gyazo.com/fa193c7fc567a0591ddcd05a53de847e)

---

# 6. ツール

* 化合物をコンピュータで扱うためのソフトウェア

    * データベースとは別の話なので、興味がある人はリンクなどを参考ください。これらのツールを利用すると簡単なデータベースを自分で作ることができます。構造の類似度の計算や構造検索、ファイル形式変換、図の生成などが可能です。

        * [Open Banel](http://openbabel.org/wiki/Main_Page)
        * [RDKit](http://www.rdkit.org/)
        * [Chemistry Development Kit (CDK)](https://cdk.github.io/)
    ---

    * 分子表示

        * PubChem 3D Viewer
            * 右の`3D Conformer Tools`をクリック

        [![Image from Gyazo](https://i.gyazo.com/02deb07e9c325c38e1a845427a839e2f.png)](https://gyazo.com/02deb07e9c325c38e1a845427a839e2f)
        
            * 表示したいCIDまたはSIDを入力し、Viewをクリック

        [![Image from Gyazo](https://i.gyazo.com/77a62b290a196d5c35bd2d5c967922ec.png)](https://gyazo.com/77a62b290a196d5c35bd2d5c967922ec)

            * 表示されるウインドウで、化合物のコンフォマーの構造を見ることができます。また、左のツールをクリックして、画像やデータの保存することができます。

        [![Image from Gyazo](https://i.gyazo.com/8ed4e106d2a27edfd0314b24d3402d38.png)](https://gyazo.com/8ed4e106d2a27edfd0314b24d3402d38)

        ---

        * [GLmol - Molecular Viewer on WebGL/Javascript](http://webglmol.osdn.jp/index-ja.html)

            * http://webglmol.osdn.jp/glmol/viewer.html
        
        1. サイトを開く
        [![Image from Gyazo](https://i.gyazo.com/8c42be6984f08224c4eccc9c09a636ef.png)](https://gyazo.com/8c42be6984f08224c4eccc9c09a636ef)

        2. https://pubchem.ncbi.nlm.nih.gov/compound/13730 のダウンロード、3D ConformerのSDFで Display をクリックします。
        [![Image from Gyazo](https://i.gyazo.com/39c17594df8cb8b526fc7c8882254f20.png)](https://gyazo.com/39c17594df8cb8b526fc7c8882254f20)
        
        3. 表示されたSDFデータをクリップボードにコピーします。
            [![Image from Gyazo](https://i.gyazo.com/e67b7ec9fcac730f723da023c4f3f93c.png)](https://gyazo.com/e67b7ec9fcac730f723da023c4f3f93c)

        4. 1.のサイトの Loadをクリックします。
        [![Image from Gyazo](https://i.gyazo.com/4ec8af59d093a81fd36019f779556b9a.png)](https://gyazo.com/4ec8af59d093a81fd36019f779556b9a)

        5. 緑で選択された入力欄に、コピーしたSDFデータをペーストします。
        [![Image from Gyazo](https://i.gyazo.com/275d8aac697cef306dc649b7519224e5.png)](https://gyazo.com/275d8aac697cef306dc649b7519224e5)

        6. `Reload molecule from textarea`をクリックして、SDFデータを読み込みます。
              [![Image from Gyazo](https://i.gyazo.com/537a93e131badfc45e438800d3849267.png)](https://gyazo.com/537a93e131badfc45e438800d3849267)

        7. Load をクリックして、メニュをたたみます。
        [![Image from Gyazo](https://i.gyazo.com/cc307fc4da4a50ddf01f0208b8ee3839.png)](https://gyazo.com/cc307fc4da4a50ddf01f0208b8ee3839)

        8. Rotate, Translate, Zoom, Slab を選択して、適当に分子の表示を変更してください。

    ---

* ID変換サービス
    * [リンク自動管理システム（Hyperlink Management System）](http://biodb.jp/)
        * http://biodb.jp/

---
