# 取得開放活動清單 get_activity_list 　




API編碼:2.10.0

> 


更新日期:

> 

SVN版本:


發布版本:2.0.2

### 1.路徑:system/get_activity_list

### 2. 說明
取得開放活動清單,只會取得現在有開放的活動

### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |版本|
| -- | -- | -- | -- | -- |--|
| err_code | 回傳參數碼 | string |  |--|
| err_desc | 回傳參數碼說明 | string | -- |--|
|activity|活動|array|key|--|
|activity_id|活動id|string|有可能有英文?|--|
|description|活動描述|string|--|--|
|type|類型|int|--|--|
|start_time|開始時間|string|--|--|
|end_time|結束時間|string|--|--|
|reward|獎勵|string|--|--|


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|



### 6.回傳格式範例

```
array (size=3)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'activity' => 
    array (size=1)
      0 => 
        array (size=6)
          'activity_id' => string '888' (length=3)
          'description' => string '0' (length=1)
          'type' => int 1
          'start_time' => string '2016-05-20 00:00:00' (length=19)
          'end_time' => string '2016-05-26 01:00:00' (length=19)
          'reward' => string '' (length=0)
```



