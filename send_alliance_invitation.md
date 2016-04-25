# 寄聯盟邀請信 send_alliance_invitation





### sendMailAlliance($ValueControl, $Localization, $character_id, $findid->id, $reward, 640024, 630014, 8, 0)[下午 06:21:59] Magus: //640024 630014 為好友邀請 聯盟要換

type = 8 subtype = 2


API編碼:2.0.13





更新日期:2016/4/25

> 

SVN版本:15359.

> 

發布版本:2.0.0
### 1.路徑:alliance/send_alliance_invitation

### 2. 說明
寄出邀請信，目前只有新人不能寄出
### 3. 輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |
| -- | -- | -- | -- | -- |
|character_id |角色ID|int|4|可由token取得(clinet可不用輸入|
|nickname|受邀者|string|--|角色暱稱|



### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |--|
| err_desc | 回傳參數碼說明 | string | -- |




### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|601|權限不足|
|604|已有所屬聯盟|
|606|無法寄信給自己|

### 6.回傳格式範例

```array (size=2)

  'err_code' => string '000' (length=3)
  
  'err_desc' => string 'success' (length=7)```