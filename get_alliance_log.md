# 取得聯盟日誌 get_alliance_log










API編碼:2.0.16





更新日期:2016/4/25 2016/5/4 2016/5/5


SVN版本:15358.15503. 15509

> 

發布版本:2.0.0
### 1.路徑:alliance/get_alliance_log



### 2. 說明
取得聯盟日誌,筆數限制 未輸入則給50筆,只吐7天內
### 3. 輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |
| -- | -- | -- | -- | -- |
|limit |處理動作|var|--|0:拒絕並刪除郵件,1:接受|
|type|型態|int--|--|



### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |--|
| err_desc | 回傳參數碼說明 | string | -- |
|logs|日誌|array|key|
|nickname|暱稱|string|--|
|type|型別|int|--|
|value|值|int||client定義|
|valuestring|日誌|text||client定義|




|createtime|建立時間|string|--|



### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|602|不屬於任何聯盟|
|615|無日誌紀錄|

### 6.回傳格式範例

```
array (size=3)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'logs' => 
    array (size=2)
      0 => 
        array (size=4)
          'nickname' => string '' (length=0)
          'type' => int 0
          'value' => string 'test' (length=4)
          'createtime' => string '2016-03-04 08:13:23.591755' (length=26)
      1 => 
        array (size=4)
          'nickname' => string '' (length=0)
          'type' => int 0
          'value' => string 'test 2' (length=6)
          'createtime' => string '2016-03-04 08:13:23.330000' (length=26)
```



