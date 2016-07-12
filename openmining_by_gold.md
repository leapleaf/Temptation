#金幣開啟佇列 open_mining_by_gold



API編碼:2.9.3

> 


更新日期:

> 

SVN版本:

> 

發布版本:2.2.0
### 1.路徑:mining/open_mining_by_gold

### 2. 說明
用金幣開啟下一佇列
### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |版本|
| -- | -- | -- | -- | -- | -- |


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |版本|
| -- | -- | -- | -- | -- |--|
| err_code | 回傳參數碼 | string |  |--|
| err_desc | 回傳參數碼說明 | string | -- |--|
|extra_queue_num|採礦佇列|array|目前最多7組|--|
|next_open_remaining_time|剩餘時間|int|--|--|





### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|140|the character does not exist|
|407|貨幣不夠|

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

