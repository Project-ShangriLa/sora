#Sora 穹

ShangriLa API Server

## 概要
アニメの情報を返すREST型のAPIサーバーです。

Ruby Sinataで実装。

シンプルな実装にしてサーバーの実装は変更しやすいようにします。


## インストール

記述中

* mysql or mariadb インストール
* データベース作成
* マスターテーブルのインサート
* bundle install

## 起動方法

記述中

## V1 API リファレンス

### エンドポイント

http://api.moemoe.tokyo/anime/v1

### 認証

V1では認証を行いません、IP単位のリクエスト数は保存する計画です。

V2では認証ありを予定しています。

### レートリミット

なし

#### GET /anime/v1/master/list

ShangriLa API Serverサーバーが持っているマスターの情報のリストを返却します。

レスポンス例:curl

```
 $curl http://api.moemoe.tokyo/anime/v1/master/list
 
 {
  '2014' : [1,2,3,4],
  '2015' : [1]
 }
```


#### GET /aime/v1/master/YYYY

YYYY年アニメ1クール4クールの情報をすべて返却します

レスポンス例:curl

#### GET /anime/v1/master/YYYY/:n

YYYY年アニメのうちの指定されたクールの情報をすべて返します

レスポンス例:curl



#### GET /anime/v1/twitter_follwer/YYYY/:n

YYYY年アニメのうち指定されたクールのツイッターフォロワー数の情報を返します

レスポンス例:curl

