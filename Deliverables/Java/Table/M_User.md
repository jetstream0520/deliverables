
 # テーブル名
 - ユーザ管理マスタ
 - M_USER

 # 運用目的

ユーザー情報を管理するためのテーブル。
主キーはユーザIDとなる。

 # テーブル構造

|項目名|カラム名|データ型|項目長|NULL許可|主キー|用途|
|:--|:--|:--:|:--:|:--:|:--:|:--|
|ユーザID|LoginUserId|Varchar|6|×|1|タスクを担当するユーザIDが設定される。基本的にはログインしたユーザIDが設定される。|
|ログインパス|LoginPass|Varchar|20|○| |g|
|登録担当者|AddUserId|Varchar|6|×| | |
|登録日付|AddDay|Varchar|8|×| | |
|登録時刻|AddTime|Varchar|6|×| | |
|更新担当者|UpdUserId|Varchar|6|×| | |
|更新日付|UpdDay|Varchar|8|×| | |
|更新時刻|UpdTime|Varchar|6|×| | |


 # CREATE文
> 	CREATE TABLE M_USER (
> 		LoginUserId   VARCHAR(6) NOT NULL PRIMARY KEY,
> 		LoginPass     VARCHAR(20) NOT NULL,
> 		AddUserId     VARCHAR(6) NOT NULL,
> 		AddDay        VARCHAR(8) NOT NULL,
> 		AddTime       VARCHAR(4) NOT NULL,
> 		UpdUserId     VARCHAR(6) NOT NULL,
> 		UpdDay        VARCHAR(8) NOT NULL,
> 		UpdTime       VARCHAR(6) NOT NULL
> 	);




