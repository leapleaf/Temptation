# +聯盟降權 alliance_demote_position


API編碼:2.3.1

> 



更新日期:

> 

SVN版本:

> 

發布版本:2.0.0
### 1.路徑:alliance/alliance_demote_position

### 2. 說明

降低聯盟成員職位,先判斷降權者有無權限後,對被降權者降低職位.
### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
| nickname | 被降權者 | string | 11 | 暱稱 |

### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |  |
| err_desc | 回傳參數碼說明 | string | -- |


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|601|無此權限|
|605|該玩家不屬於此聯盟|
|618|此玩家已是最低位階|

### 6.回傳格式範例

```
array (size=2)



  'err_code' => string '000' (length=3)
 


  'err_desc' => string 'success' (length=7)*



```