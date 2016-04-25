# 聯盟廣播 send_msg_to_all_member




### AllianceInfoModify靜態表對應之後要改成寄聯盟信專屬



API編碼:2.0.14

目前信件 type = 8, subtype = 2



更新日期:

> 

SVN版本:

> 

發布版本:2.0.0
### 1.路徑:alliance/send_msg_to_all_member

### 2. 說明
寄出邀請信，目前只有Rank2以上可以寄
### 3. 輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |
| -- | -- | -- | -- | -- |
|msg|廣播文字|text|--|--|



### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |--|
| err_desc | 回傳參數碼說明 | string | -- |




### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|601|權限不足|
|602|不屬於任何聯盟|

### 6.回傳格式範例

```
array (size=2)

  'err_code' => string '000' (length=3)
  
  'err_desc' => string 'success' (length=7)
  ```
