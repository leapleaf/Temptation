# 合成寶石幫助 collect_gem_help





API編碼:2.3.2

> 


更新日期:2016/05/03

> 

SVN版本:15458 15537.

> 

發布版本:2.0.0
### 1.路徑:alliance_help/collect_gem_help

### 2. 說明
合成寶石幫助,先判斷有無可幫助序列,再判斷玩家是否同一聯盟,同一玩家同一序列僅能幫助一次,目前是幫助一次扣20秒


### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
| character_id | 腳色id | int | -- | 由token取得 |
| queue_id | 道具id | int | 6 | -- |
|nickname|玩家暱稱|string|11|被幫助者|

### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |  |
| err_desc | 回傳參數碼說明 | string | -- |


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|602|不屬於任何聯盟|
|419|沒物品合成中|
|605|該玩家不屬於此聯盟|
|612|已幫助過此玩家|
|629|幫助已達上限|




### 6.回傳格式範例

*

```
array (size=4)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  

```

