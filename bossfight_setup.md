# boss戰設置 boss_fight_setup


API編碼:2.2.1

更新日期:

SVN版本:

發布版本:2.0.6
### 1.路徑:fight/boss_fight_setup

### 2. 說明
設置boss戰,開戰前5分鐘才可設置,最後1分鐘關閉設置
### 3. 輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |
| -- | -- | -- | -- | -- |
|activity_id|目前boss活動id|int|2|與boss_id相同|


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |--|
| err_desc | 回傳參數碼說明 | string | -- |


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|910|版本已過期，需更新APP資料|
|124|You can't join this activity,because sign up time is over|
|122|Already joined this activity|
|194|開戰前五分鐘無法報名|




### 6.回傳格式範例

```

      ```





