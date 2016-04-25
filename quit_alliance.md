# 退出聯盟 quit_alliance





API編碼:2.0.11





更新日期:2016/4/25

> 

SVN版本:15359.

> 

發布版本:2.0.0
### 1.路徑:alliance/quit_alliance

### 2. 說明

退出聯盟，盟主無法退出聯盟
### 3. 輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |
| -- | -- | -- | -- | -- |
|character_id |角色ID|int|4|可由token取得(clinet可不用輸入|



### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |--|
| err_desc | 回傳參數碼說明 | string | -- |




### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|620|聯盟解散失敗|
|602|不屬於任何聯盟|

### 6.回傳格式範例

```array (size=2)

  'err_code' => string '000' (length=3)
  
  'err_desc' => string 'success' (length=7)```