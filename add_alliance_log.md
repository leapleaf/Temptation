# *加入聯盟日誌 add_alliance_log

API編碼:2.0.17

目前信件 type = 8, subtype = 2



更新日期:2016/4/25 2016/5/5

> 

SVN版本:15358.15506

> 

發布版本:2.0.0
### 1.路徑:alliance/add_alliance_log

### 2. 說明
記錄聯盟日誌
### 3. 輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |
| -- | -- | -- | -- | -- |
|nickname|暱稱|string|--|--|
|type|型別|int|8|client定義|
|value|值|text|--|client定義|



### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |--|
| err_desc | 回傳參數碼說明 | string | -- |




### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|601|權限不足|
|602|不屬於任何聯盟|

### 6.回傳格式範例

```
array (size=2)

  'err_code' => string '000' (length=3)
  
  'err_desc' => string 'success' (length=7)
  ```
