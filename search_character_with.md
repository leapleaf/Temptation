# 搜尋無聯盟玩家 search_character_without_alliance




API編碼:2.0.8





更新日期:

> 

SVN版本:

> 

發布版本:2.0.0
### 1.路徑:alliance/search_character_without_alliance

### 2. 說明

搜尋無聯盟玩家,亂數排序50名
### 3. 輸入參數說明
無須輸入

### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |  |
| err_desc | 回傳參數碼說明 | string | -- |




### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|603|找不到此聯盟|
|604|你已有所屬聯盟|
### 6.回傳格式範例

```array (size=3)

  'err_code' => string '000' (length=3)
  
  'err_desc' => string 'success' (length=7)
  
  'characters' => 
  
    array (size=50)
    
      0 => 
        array (size=4)
          'nickname' => string 'A83C172A1ACE98897DFA' (length=20)
          'lv' => string '1' (length=1)
          'model' => string '-1' (length=2)
          'exp' => string '0' (length=1)
      1 => 
        array (size=4)
          'nickname' => string 'test016' (length=7)
          'lv' => string '1' (length=1)
          'model' => string '0' (length=1)
          'exp' => string '0' (length=1)```