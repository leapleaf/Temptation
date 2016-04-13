# 搜尋聯盟 search_alliance




API編碼:2.0.9





更新日期:

> 

SVN版本:

> 

發布版本:2.0.0
### 1.路徑:alliance/search_alliance

### 2. 說明

搜尋聯盟,可精確與模糊搜尋,先判斷有無角色id,若無則搜尋聯盟名稱
### 3. 輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |
| -- | -- | -- | -- | -- |
|character_id |角色ID|int|4|可以不輸入|
|type|搜尋模式|int|1|0:精確1:模糊|
|alliance_name|聯盟名稱|string|18|--|



### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |--|
| err_desc | 回傳參數碼說明 | string | -- |
|alliance|聯盟|array|--|
| name | 聯盟名稱 | string |--|
| lang | 語系 | string | -- |
|shortname|聯盟短名稱|string|--|
|flag|聯盟旗幟|string|--|
|createtime|創立時間|string|--|
|member_count|成員人數|string|--|



### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|603|找不到此聯盟|
### 6.回傳格式範例

```array (size=3)
  'err_code' => string '000' (length=3)
  
  'err_desc' => string 'success' (length=7)
  
  'alliance' => 
  
    array (size=2)
      0 => 
        array (size=7)
          'name' => string 'magus_ship' (length=10)
          'lang' => string 'en' (length=2)
          'shortname' => string 'MS' (length=2)
          'introduction' => string 'introduction' (length=12)
          'flag' => string '1' (length=1)
          'createtime' => string '2016-03-21 09:21:55' (length=19)
          'members_count' => string '1' (length=1)
      1 => 
        array (size=7)
          'name' => string 'Magus_Land' (length=10)
          'lang' => string 'en' (length=2)
          'shortname' => string 'A' (length=1)
          'introduction' => string 'introduction' (length=12)
          'flag' => string '1' (length=1)
          'createtime' => string '2016-03-23 06:22:59' (length=19)
          'members_count' => string '6' (length=1)```