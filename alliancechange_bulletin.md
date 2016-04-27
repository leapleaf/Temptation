#聯盟變更內部布告  alliance_change_bulletin





API編碼:2.0.22

> 


更新日期:2016/04/27

> 

SVN版本:153??.

> 

發布版本:2.0.0
### 1.路徑:alliance/alliance_change_bulletin

### 2. 說明

取得公開招募聯盟資訊,會先判斷有無聯盟,有則604,client一次取完,依序播放,播完再call這支api,

### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
|character_id|角色id|int|4|帶入token|
|bulletin|內部布告|string|--|目前未設限制，有需要再加|


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

