# 取得聯盟上游購買紀錄 get_alliance_purchase_upper_history

API編碼:2.2.4

> 


更新日期:2016/05/04

> 

SVN版本:

> 

發布版本:2.0.0
### 1.路徑:alliance_store/get_alliance_purchase_upper_history

### 2. 說明

取得聯盟上游購買紀錄


### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
| character_id | 腳色id | int | -- | 由token取得 |
| lang | 語系 | string | 2 | -- |

### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |  |
| err_desc | 回傳參數碼說明 | string | -- |
|purchase_history|購買紀錄|array|key|
|nicaname|腳色暱稱|string|--|
|name|道具名稱|string|依語系調整|
|num|購買數量|int|--|
|purchase_time|購買時間|datetime|--|

### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|910|版本已過期，需更新APP資料|
|602|不屬於任何聯盟|


### 6.回傳格式範例

*

```
array (size=5)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)


```

