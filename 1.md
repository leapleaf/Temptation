# create_alliance
API編碼:2.0.0

> 

更新日期:

> 

SVN版本:

> 

發布版本:2.0.0
### 1.路徑:alliance/create_alliance

### 2. 說明

建立聯盟,會先判斷該腳色有無聯盟,聯盟名稱需小於18,並不得重複

### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
| name | 聯盟名稱 | string | 18 | 不得重複 |
| shortname | 聯盟短名稱 | string | 15 | 聯盟縮寫 |
| lang | 語系 | string | 15 | -- |
| introduction | 聯盟簡介 | string | -- | 顯示在聯盟資訊 |
| character_id | 盟主 | int | 4 | 可由token取得 |

### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | -- |  |
| err_desc | 回傳參數碼說明 | -- | -- |


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|110|角色暱稱或聯盟名稱長度必須小於18|
|604|你已有所屬聯盟|
|613|聯盟名稱已存在|

### 6.回傳格式範例

*array (size=2)
> 


  'err_code' => string '000' (length=3)
> 


  'err_desc' => string 'success' (length=7)*

