# boss戰設置 boss_fight_setup


API編碼:2.2.3

更新日期:

SVN版本:

發布版本:2.0.6
### 1.路徑:fight/boss_fight_setup

### 2. 說明
設置boss戰,開戰前5分鐘才可設置,最後1分鐘關閉設置,只能設一個部隊
### 3. 輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |
| -- | -- | -- | -- | -- |
|pet1|部隊|int|--|若玩家未設置,boss戰開始時|
|items|道具|jsoncode|最大數量30 |ex:[{\"item_id\":1,\"num\":3},{\"item_id\":2,\"num\":3},{\"item_id\":3,\"num\":3}]|
|


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |--|
| err_desc | 回傳參數碼說明 | string | -- |


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|910|版本已過期，需更新APP資料|
|123|You don't joined this activity|
|195|開戰前1分鐘無法配置|
|182|You can't use special pet in this fight mode|




### 6.回傳格式範例

```

      ```





