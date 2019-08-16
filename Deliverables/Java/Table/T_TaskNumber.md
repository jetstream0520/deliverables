
 # テーブル名
 - タスク管理テーブル
 - T_TASKNUMBER

 # 運用目的
    登録されたタスクを管理するテーブル。
    主キーはタスク担当ユーザIDとタスクナンバーとなる。

 # テーブル構造

|項目名|カラム名|データ型|項目長|NULL許可|主キー|用途|
|:--|:--|:--:|:--:|:--:|:--:|:--|
|ユーザID|UserId|Varchar|6|×|1|タスクを担当するユーザIDが設定される。基本的にはログインしたユーザIDが設定される。|
|タスクナンバー|TaskNum|INTEGER|5|×|2|g|
|タスク期限日付|DeadlineDay|Varchar|6|○| |g|
|タスク期限時刻|DeadlineTime|Varchar|4|○| |g|
|タスク内容|TaskDetails|Varchar|100|×| |g|
|タスク状態フラグ|TaskFlag|Varchar|1|○| |0:未完了、1:完了 デフォルト値は0となる。|
|登録担当者|AddUserId|Varchar|6|×| | |
|登録日付|AddDay|Varchar|8|×| | |
|登録時刻|AddTime|Varchar|6|×| | |
|更新担当者|UpdUserId|Varchar|6|×| | |
|更新日付|UpdDay|Varchar|8|×| | |
|更新時刻|UpdTime|Varchar|6|×| | |

 # CREATE文
> CREATE TABLE T_TASKNUMBER (
>     UserId        VARCHAR(6) NOT NULL,
>     TaskNum       INTEGER NOT NULL IDENTITY(1,1),
>     DeadlineDay   VARCHAR(8) NULL,
>     DeadlineTime  VARCHAR(4) NULL,
>     TaskDetails   VARCHAR(100) NULL,
>     TaskFlag      VARCHAR(1) NULL DEFAULT (0),
>     AddUserId     VARCHAR(6) NOT NULL,
>     AddDay        VARCHAR(8) NOT NULL,
>     AddTime       VARCHAR(4) NOT NULL,
>     UpdUserId     VARCHAR(6) NOT NULL,
>     UpdDay        VARCHAR(8) NOT NULL,
>     UpdTime       VARCHAR(6) NOT NULL,
> 	PRIMARY KEY(UserId,TaskNum)
> );




