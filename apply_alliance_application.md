

# 核可聯盟新人 apply_alliance_application
API編碼:2.4.2

> 



更新日期:2016/05/12

> 

SVN版本:15741..

> 

發布版本:2.0.0

關聯資料庫:

C:create;R:read;U:update;D:delete;

|Table Name|行為|備註|
|--|--|--|
|alliance|R,U|--|
|character|R|--|
|alliance_member|R,C|--|
|character_mail|U,D|--|
|alliance_invitation|R,D|--|

### 1.路徑:alliance_member/apply_alliance_application

### 2. 說明

核可聯盟新人,先判斷有無'Allow'權限,若核可則刪除該玩家所有其他聯盟申請,具結則刪除該筆玩家申請

### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
| nickname | 暱稱 | string | 12 | 申請玩家 |
|apply|核可|int|1|1:核可 0:拒絕|


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
|638|無此邀請信件|

### 6.回傳格式範例

*array (size=2)
> 


  'err_code' => string '000' (length=3)
> 


  'err_desc' => string 'success' (length=7)*



