

# 核可聯盟新人 apply_alliance_application
API編碼:2.4.2

> 



更新日期:

> 

SVN版本:15435..

> 

發布版本:2.0.0
### 1.路徑:alliance_member/apply_alliance_application

### 2. 說明

核可聯盟新人,先判斷有無'Allow'權限,

### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
| nickname | 暱稱 | string | 12 | 申請玩家 |
|accept|接受|int|1|1:接受 0:拒絕|


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |  |
| err_desc | 回傳參數碼說明 | string | -- |


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|601|無此權限|
|603|找不到此聯盟(client本人沒有聯盟|
|604|已有所屬聯盟|

### 6.回傳格式範例

*array (size=2)
> 


  'err_code' => string '000' (length=3)
> 


  'err_desc' => string 'success' (length=7)*



