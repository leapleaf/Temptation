# Boss最高傷害 guinnes_record_for_boss_damage



API編碼:3.0.0

> 


更新日期:

> 

SVN版本:


發布版本:2.2.0

### 1.路徑:rank/guinnes_record_for_boss_damage

### 2. 說明
取得Boss最高傷害


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



### 6.回傳格式範例



```
array (size=8)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'nickname' => string 'yee' (length=3)
  'no' => int 201
  'top_damage' => int 40029341
  'model' => int 1
  'duty' => int 3
  'lv' => int 40
```