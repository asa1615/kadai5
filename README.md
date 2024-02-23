# HTTPにまつわる用語について  

## HTTPとは  
ハイパーテキスト転送プロトコル  
HTMLなどのハイパーメディア文章を転送するためのアプリケーション層プロトコル  
HTTPは旧来のクライアントサーバーモデルに則っており、
クライアントはサーバーにリクエストを送信するためにポートを開き、  
サーバー側からのレスポンスが返ってくるまで待機する。  
HTTPはステートレスプロトコルであり、サーバーは2つの間で何もデータを保持しない。  

## URL
ホームページの住所に相当する情報  
ホームページの置いてある場所やファイル名を示す情報

## クエリ文字列
URLで?の後ろにくる部分  
ユーザーがどのようにしてWebコンテンツへたどり着いたか、流入経路を分析する際に活用できるもの

  （例） http\://〇〇.jp/?□＝△  
　　 □：クエリ文字列の名前  
　　 △：クエリ文字列の値  

 - パッシブパラメータ  
  Webページに固有のパラメータを付与し流入元を分析すること。
  パラメータの有無に関わらず、表示するページは同じものとなる。

 - アクティブパラメータ  
  付与するパラメータによって表示するページを変えること。
  主にブログやECサイトで活用される。

## パス変数
URLでドメインの後ろ、?の前にくる部分
特定のリソースを識別するために必要な情報

  （例）http\://〇〇.jp/◇/▽/?～  
　　◇：リソース名  
　　▽：ユーザーIDなどを表す変数

## クエリ文字列とパス変数の違い
- クエリ文字列 ・・・ 特定のものに条件を追加する際に必要
- パス変数 ・・・ 特定のものを判別する際に必要

## HTTPメソッド
WebブラウザからWebサーバに出されるお願いの種類

### GET
値をURLにくっつけてWebサーバに送るやり方。  
HTMLファイルや画像といったデータを取得する場合に利用する。  
Webサイト閲覧時において使用頻度が高い。

### POST
値を見えない所に隠してWebサーバに送るやり方。  
フォームに入力したパスワードといったデータを転送する場合に利用する。

### PUT
指定したリソースが無かったら新規作成、あったら更新。 
ファイルをアップロードするときに使う。  
Webサーバ上のファイルを置き換えることが出来るため、利用出来ないように制限されている場合が多い。

### PATCH
ソフトに変更を加える。

### DELETE
指定したファイルを削除する。  
利用出来ないように制限されている場合が多い。

### HTTPステータスコード  
HTTPリクエストの結果を表す3桁の数字  

100-199:情報レスポンス  
200-299:成功レスポンス  
300-399:リダイレクトメッセージ  
400-499:クライアントエラーレスポンス
500-599：サーバーエラーレスポンス  

## リクエストヘッダ
HTTPリクエストを構成する部品のひとつ。  
お願い事やお願い元に関することが書かれている場所。

## JSON  
JavaScript Object Notatin  
構造化したデータを表すためのデータ記述言語のひとつ。  

※書式がJavaScriptに従ったものとなっているだけで、JavaScript専用ということではない。  

特徴
- データとして文字列以外に、数値や空（Null）データなども扱うことが可能。
- データをカッコで囲んで構造を表すので、データファイルは小さめ。

（例）
{}の中にキーと値をコロンで区切って記述する。キーは必ずダブルクオーテーションで区切る必要がある。    
{“key1” : “value1”, “key2” : “value2”}  
```
[  
{"id":"1","name":"suzuki"},  
{"id":"2","name":"takahashi"}  
]  
```


参照資料  
https://developer.mozilla.org/ja/  
https://wa3.i-3-i.info/  
https://products.sint.co.jp/topsic/blog/json  
書籍  
イラスト図解式この一冊で全部分かるWeb技術の基本  

