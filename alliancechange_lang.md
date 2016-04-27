#聯盟變更語系 alliance_change_lang






API編碼:2.0.23

> 


更新日期:2016/04/27

> 

SVN版本:153??.

> 

發布版本:2.0.0
### 1.路徑:alliance/alliance_change_lang

### 2. 說明

變更聯盟內部布告，目前只有Rank2以上才可變更,

### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
|character_id|角色id|int|4|帶入token|
|lang|內部布告|string|--|目前未設限制，有需要再加|


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |  |
| err_desc | 回傳參數碼說明 | string | -- |




### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|601|無此權限|
|602|不屬於任何聯盟|

### 6.回傳格式範例

```
array (size=3)

  'err_code' => string '000' (length=3)
  
  'err_desc' => string 'success' (length=7)
```

