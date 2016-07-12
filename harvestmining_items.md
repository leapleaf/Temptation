#收成採礦 harvest_mining_items



API編碼:2.9.2

> 


更新日期:

> 

SVN版本:

> 

發布版本:2.2.0
### 1.路徑:mining/harvest_mining_items

### 2. 說明
收成採礦,時間到時會call此api

### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |版本|
| -- | -- | -- | -- | -- | -- |


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |版本|
| -- | -- | -- | -- | -- |--|
| err_code | 回傳參數碼 | string |  |--|
| err_desc | 回傳參數碼說明 | string | -- |--|
|queue|採礦佇列|array|目前最多8組|--|
|remaining_time|剩餘時間|int|--|--|
|rare_type|採礦類型|int|1~3|--|
|mining_items|採礦佇列詳細|array|目前固定3組|--|
|item_id|道具ID|int|--|--|
|num|道具數量|int|--|--|




### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|140|the character does not exist|

### 6.回傳格式範例
####收成3個部隊,一個在佇列中
```
array (size=4)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'harvest_report_mail' => 
       array (size=3)
        0=> 109858 int
        1=> 109859 int
        2=> 109860 int
  'queue' => 
    array (size=4)
      0 => 
        array (size=3)
          'mining_items' => 
          array (size=3)
            0 => 
              array (size=2)
                'item_id' => int 100011
                'num' => int 5
            1 => 
              array (size=2)
                'item_id' => int 100131
                'num' => int 4
            2 => 
              array (size=2)
                'item_id' => int 100133
                'num' => int 2
          'remaining_time' => int 0
          'rare_type' => int 3
 
```

