# 升級獎勵 receive_level_gift



API編碼:3.0.1

> 


更新日期:

> 

SVN版本:


發布版本:2.2.0

### 1.路徑:reward/receive_level_gift

### 2. 說明
取得升級獎勵,在每次升級後call這支API,若有獎勵會吐獎勵道具,沒有吐280
若升級後斷線請用get_character的level_gift_can_received判斷

### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |版本|
| -- | -- | -- | -- | -- |--|
| err_code | 回傳參數碼 | string |  |--|
| err_desc | 回傳參數碼說明 | string | -- |--|
|nickname|暱稱|string|--|--|
|no|場次|int|--|--|
|top_damage|總傷害量|int|--|--|
|model|模型|int|--|--|
|lv|等級|int|--|--|



### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|280|沒有獎勵道具|
|281|已領過此獎勵|



### 6.回傳格式範例



```
array (size=8)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'reward_item'=>
array (size=8)
  0 => 
    array (size=2)
      'item_id' => int 100078
      'num' => int 15
  1 => 
    array (size=2)
      'item_id' => int 100079
      'num' => int 5
  2 => 
    array (size=2)
      'item_id' => int 100077
      'num' => int 10
  3 => 
    array (size=2)
      'item_id' => int 100128
      'num' => int 2
  4 => 
    array (size=2)
      'item_id' => int 100002
      'num' => int 6
  5 => 
    array (size=2)
      'item_id' => int 100009
      'num' => int 4
  6 => 
    array (size=2)
      'item_id' => int 100137
      'num' => int 1
  7 => 
    array (size=2)
      'item_id' => int 100154
      'num' => int 1
```