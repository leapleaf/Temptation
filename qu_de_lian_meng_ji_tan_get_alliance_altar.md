# 取得聯盟祭壇 get_alliance_altar

API編碼:2.8.0

> 


更新日期:2016/05/20

> 

SVN版本:

> 

發布版本:2.0.0
### 1.路徑:alliance/get_alliance_altar

### 2. 說明

取得聯盟祭壇資訊

### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
|alliance_name|聯盟名稱|string|12|--|


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |版本|
| -- | -- | -- | -- | -- |--|
| err_code | 回傳參數碼 | string |  |--|
| err_desc | 回傳參數碼說明 | string | -- |--|
|total_altar_lv|目前祭壇科技等級|int|--|2.0.1|
| picture_id|圖片id|int|--|2.0.1|


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|

### 6.回傳格式範例

*

```
array (size=4)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'total_altar_lv' => int 0
  'picture_id' => string 'AL000' (length=5)
```
