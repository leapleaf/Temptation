# 公開聯盟輪播 alliance_carousel_recruit




API編碼:2.0.21

> 


更新日期:2016/04/27

> 

SVN版本:15373.

> 

發布版本:2.0.0
### 1.路徑:alliance/alliance_carousel_recruit

### 2. 說明

取得公開聯盟資訊,會先判斷有無聯盟,有則604,client一次取完,依序播放,播完再call這支api,

### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
|character_id|角色id|int|4|帶入token|


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |  |
| err_desc | 回傳參數碼說明 | string | -- |
|alliances|聯盟|array|key|
|alliance_name|聯盟名稱|string|--|
|shortname|聯盟短名稱|string|--|



### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|604|已有所屬聯盟|

### 6.回傳格式範例

```
array (size=3)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'alliances' => 
    array (size=14)
      0 => 
        array (size=2)
          'name' => string 'ABC' (length=3)
          'shortname' => string 'A' (length=1)
      1 => 
        array (size=2)
          'name' => string 'goddamn333' (length=10)
          'shortname' => string 'A' (length=1)
```

