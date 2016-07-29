

# 取得申請聯盟清單 get_alliance_application
API編碼:2.6.1

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
|alliance|R|--|
|character|R|--|
|alliance_member|R,C|--|
|character_mail|U,D|--|
|alliance_invitation|R,D|--|
### 1.路徑:alliance_member/get_alliance_application

### 2. 說明

取得申請聯盟清單,先判斷有無'Allow'權限,再取得相對應玩家的資料

### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |  |
| err_desc | 回傳參數碼說明 | string | -- |
|applications|申請清單|array|key|
|nickname|暱稱|string|--|
|power|戰力|int|--|
|model|模組|int|--|
|lv|等級|int|--|
|duty|責任|int|--|


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|601|無此權限|
|603|找不到此聯盟(client本人沒有聯盟|

### 6.回傳格式範例

*array (size=2)
> 


  'err_code' => string '000' (length=3)
> 


  'err_desc' => string 'success' (length=7)*



