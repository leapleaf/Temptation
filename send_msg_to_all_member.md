# 聯盟廣播 send_msg_to_all_member




### AllianceInfoModify靜態表對應之後要改成寄聯盟信專屬



API編碼:2.0.11





更新日期:

> 

SVN版本:

> 

發布版本:2.0.0
### 1.路徑:alliance/send_msg_to_all_member

### 2. 說明
寄出邀請信，目前只有新人不能寄出
### 3. 輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |
| -- | -- | -- | -- | -- |
|character_id |角色ID|int|4|可由token取得(clinet可不用輸入|
|msg|廣播文字|text|--|角色暱稱|



### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |--|
| err_desc | 回傳參數碼說明 | string | -- |




### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|601|權限不足|
|604|你已有所屬聯盟|
|606|不能寄邀請信給自己|

### 6.回傳格式範例

```array (size=2)

  'err_code' => string '000' (length=3)
  
  'err_desc' => string 'success' (length=7)```
