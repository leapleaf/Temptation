# +聯盟提權 alliance_promote_position

API編碼:2.3.0

> 



更新日期:2016/05/03

> 

SVN版本:15458.

> 

發布版本:2.0.0

關聯資料庫:

C:create;R:read;U:update;D:delete;

|Table Name|行為|備註|
|--|--|--|
|alliance|R|--|
|character|R|--|
|alliance_member|R,U|--|
|character_mail|C|--|

### 1.路徑:alliance/alliance_promote_position

### 2. 說明

提升聯盟成員職位,先判斷提權者有無權限後,對被提權者提升職位,只能提權到比自己低一個職位.
### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
| nickname | 被提權者 | string | 11 | 暱稱 |

### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |  |
| err_desc | 回傳參數碼說明 | string | -- |
|position|職位|int|被更動者|


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|601|無此權限|
|605|該玩家不屬於此聯盟|
|641|階級人數已滿|

### 6.回傳格式範例
```
*array (size=2)
> 


  'err_code' => string '000' (length=3)
> 


  'err_desc' => string 'success' (length=7)*



```