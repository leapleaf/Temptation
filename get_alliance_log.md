# *取得聯盟日誌 get_alliance_log










API編碼:2.0.11





更新日期:


SVN版本:

> 

發布版本:2.0.0
### 1.路徑:alliance/get_alliance_log



### 2. 說明
取得聯盟日誌,筆數限制
### 3. 輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |
| -- | -- | -- | -- | -- |
|$limit |處理動作|var|--|0:拒絕並刪除郵件,1:接受|
|mail_id|郵件id|var|--|郵件id|



### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |--|
| err_desc | 回傳參數碼說明 | string | -- |




### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|604|已有所屬聯盟|
|614|此邀請已失效|

### 6.回傳格式範例

```array (size=2)

  'err_code' => string '000' (length=3)
  
  'err_desc' => string 'success' (length=7)```



