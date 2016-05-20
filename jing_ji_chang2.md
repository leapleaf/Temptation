#比牌 fight/card_versus





API編碼:2.9.0

> 


更新日期:

> 

SVN版本:

> 

發布版本:2.0.2
### 1.路徑:fight/card_versus

### 2. 說明

取得聯盟科技資訊,取得的是可研發科技清單,會執行達到升級時的tech_id升級
### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
|nickname|暱稱|int|--|被挑戰者|


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |版本|
| -- | -- | -- | -- | -- |--|
| err_code | 回傳參數碼 | string |  |--|
| err_desc | 回傳參數碼說明 | string | -- |--|
|attacker_score|挑戰者分數|int|目前|--|
|defender_score|防禦者分數|int|--|--|
|win|挑戰結果|boolean||--|


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|601|權限不足|
|602|不屬於任何聯盟|
|642|科技尚未開放|

### 6.回傳格式範例

```
array (size=13)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'exp' => int 12999
  'threshold' => int 13000
  'benefit' => int 50
  'next_benefit' => int 60
  'remaining_time' => int 0
  'can_levelup' => boolean false
  'donate_cdtime' => int 0
  'can_donate_item' => 
    array (size=7)
      'item_id1' => int 100014
      'item_id1_can_donate' => boolean true
      'quantity1' => int 10
      'item_id2' => int 100014
      'quantity2' => int 15
      'item_id2_can_donate' => boolean false
      'goladleaf' => int 0
  'character' => 
    array (size=3)
      'in_stock1' => int 110
      'in_stock2' => int 0
      'goldleaf' => int 28
  'open' => boolean true
  'donate_lock' => boolean false
```

