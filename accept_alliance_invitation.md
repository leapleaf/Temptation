# 接受聯盟邀請 accept_alliance_invitation









API編碼:2.0.15





更新日期:2016/4/25

> 

SVN版本:15359.

> 

發布版本:2.0.0
### 1.路徑:alliance/accept_alliance_invitation

### 2. 說明
接受聯盟邀請信,
### 3. 輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |
| -- | -- | -- | -- | -- |
|accept |處理動作|var|--|0:拒絕並刪除郵件,1:接受|
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

