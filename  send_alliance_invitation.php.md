# 接受聯盟邀請 accept_alliance_invitation





API編碼:2.0.12






更新日期:

> 

SVN版本:

> 

發布版本:2.0.0
### 1.路徑:alliance/accept_alliance_invitation

### 2. 說明
寄出邀請信，目前只有新人不能寄出
### 3. 輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |
| -- | -- | -- | -- | -- |
|character_id |角色ID|int|4|可由token取得(clinet可不用輸入|
|accept|處理郵件|var|1|(0:reject & delete, 1:accept)|
|mail_id|郵件id|var|--|--|



### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |--|
| err_desc | 回傳參數碼說明 | string | -- |




### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|111|not found character mail|
|601|權限不足|
|604|你已有所屬聯盟|
|614|此邀請已失效|

### 6.回傳格式範例

```array (size=2)

  'err_code' => string '000' (length=3)
  
  'err_desc' => string 'success' (length=7)```