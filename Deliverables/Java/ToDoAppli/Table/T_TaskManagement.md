
 # テーブル名
 - タスク管理テーブル
 - T_TASKMANAGEMENT

 # 運用目的

タスクナンバーを採番して管理する。
ログインユーザID、タスクナンバーを持つ。
主キーはログインユーザIDとなる。


 # テーブル構造

|項目名|カラム名|データ型|項目長|NULL許可|主キー|用途|
|:--|:--|:--:|:--:|:--:|:--:|:--|
|ユーザID|UserId|Varchar|6|×|1|タスクを担当するユーザIDが設定される。基本的にはログインしたユーザIDが設定される。|
|タスク採番番号|TaskNumber|INTEGER|4|○| |g|
|登録担当者|AddUserId|Varchar|6|×| | |
|登録日付|AddDay|Varchar|8|×| | |
|登録時刻|AddTime|Varchar|6|×| | |
|更新担当者|UpdUserId|Varchar|6|×| | |
|更新日付|UpdDay|Varchar|8|×| | |
|更新時刻|UpdTime|Varchar|6|×| | |

 # CREATE文
> CREATE TABLE T_TASKMANAGEMENT (
>     UserId   VARCHAR(6) NOT NULL PRIMARY KEY,
>     TaskNumber    INTEGER NOT NULL,
>     AddUserId     VARCHAR(6) NOT NULL,
>     AddDay        VARCHAR(8) NOT NULL,
>     AddTime       VARCHAR(4) NOT NULL,
>     UpdUserId     VARCHAR(6) NOT NULL,
>     UpdDay        VARCHAR(8) NOT NULL,
>     UpdTime       VARCHAR(6) NOT NULL
> );



