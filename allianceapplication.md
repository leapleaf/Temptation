# 申請加入聯盟 alliance_application
API編碼:2.6.0

> 



更新日期:

> 

SVN版本:15435..

> 

發布版本:2.0.0


關聯資料庫:

C:create;R:read;U:update;D:delete;

|Table Name|行為|備註|
|--|--|--|
|alliance|R,U|--|
|character|R|--|
|alliance_member|R|--|
|alliance_invitation|C|--|
### 1.路徑:alliance_member/alliance_application

### 2. 說明

申請加入聯盟,將所有申請紀錄資料庫,同一聯盟不得重複申請,加入聯盟後所有申請將會刪除


### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
| alliance_name | 聯盟名稱 | string | 18 | -- |


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |  |
| err_desc | 回傳參數碼說明 | string | -- |


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|604|你已有所屬聯盟|
|603|找不到此聯盟|
|627|未達到加入此聯盟之要求|
|635|不得重複申請聯盟|

### 6.回傳格式範例

*array (size=2)
> 


  'err_code' => string '000' (length=3)
> 


  'err_desc' => string 'success' (length=7)*

