# 設定Boss排程 boss_fight_set_schdule
##client不用接


API編碼:2.2.0

更新日期:

SVN版本:

發布版本:2.0.6
### 1.路徑:fight/boss_fight_set_schdule

### 2. 說明
設定boss排程,輸入boss_id,報名時間,開始時間,結束時間,會寫入boss_activity table,

要注意每一筆boss_activity raw報名時間跟結束時間要完全錯開 ,並且間隔5分鐘以上
### 3. 輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |
| -- | -- | -- | -- | -- |
|boss_activity_id|boss_id|int|1|對應boss_id,目前只有1~4|
|signup_time|報名開始時間|datetime|--|ex:2016-06-15 03:50:00|
|start_time|boss戰開始時間|datetime|--|ex:2016-06-15 03:58:00|
|end_time|boss戰結束時間|datetime|--|ex:2016-06-15 03:59:00|

### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
|ORMobj|改變前boss狀態|ORM|--|
|ORMobj|改變後boss狀態|ORM|--|
| err_code | 回傳參數碼 | string |--|
| err_desc | 回傳參數碼說明 | string | -- |




### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|


### 6.回傳格式範例

```array (size=2)

  'err_code' => string '000' (length=3)
  
  'err_desc' => string 'success' (length=7)```

