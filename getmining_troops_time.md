# 取得採礦部隊時間get_mining_troops_time



API編碼:2.9.1

> 


更新日期:

> 

SVN版本:

> 

發布版本:2.2.0
### 1.路徑:mining/get_mining_troops_time

### 2. 說明
取得現在採礦部隊時間


以pass_stage_no +-2關卡等級

### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |版本|
| -- | -- | -- | -- | -- | -- |
|mining_sites|採礦地點|int|--|值為1,2,3|--|



### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |版本|
| -- | -- | -- | -- | -- |--|
| err_code | 回傳參數碼 | string |  |--|
| err_desc | 回傳參數碼說明 | string | -- |--|
|remaining_time|最後一支部隊的採集時間|int|--|--|




### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|905|輸入資料格式錯誤|
|140|the character does not exist|
|642|科技尚未開放|

### 6.回傳格式範例

```
array (size=4)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'remaining_time' => int 0
 
```

