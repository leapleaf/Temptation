# 取得聯盟資訊 get_alliance_tech_list



API編碼:2.1.1

> 


更新日期:

> 

SVN版本:

> 

發布版本:2.0.0
### 1.路徑:alliance_tech/get_alliance_tech_list

### 2. 說明

取得聯盟科技資訊,取得的是可研發科技清單
### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
|character_id|聯盟名稱|string|12|取token,client不須輸入|


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |  |
| err_desc | 回傳參數碼說明 | string | -- |
|alliance_tech_id|聯盟科技id|int|--|
|exp|現在科技研發值|int|--|
|threshold|此科技升級閥值|int|--|
|remiaining_time|升級剩餘時間|int|--|
|project|--|int|--|
|tectype|--|int|--|


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|601|權限不足|
|602|不屬於任何聯盟|

### 6.回傳格式範例

```
array (size=12)
  0 => 
    array (size=6)
      'alliance_tech_id' => int 100000
      'exp' => int 0
      'threshold' => int 1000
      'remiaining_time' => int 0
      'project' => int 1
      'tectype' => int 1
```

