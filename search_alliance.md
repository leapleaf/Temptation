# 搜尋聯盟 search_alliance




API編碼:2.0.9





更新日期:

> 

SVN版本:

> 

發布版本:2.0.0
### 1.路徑:alliance/search_alliance

### 2. 說明

搜尋聯盟,可精確與模糊搜尋,先判斷有無輸入聯盟名稱,若無則取token
### 3. 輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |
| -- | -- | -- | -- | -- |
|alliance_name|聯盟名稱|string|18|若不輸入則取token|
|character_id |角色ID|int|4|由token取得|




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
|錯誤代碼|意義|說明|
|--|--|--|
|602|不屬於任何聯盟|發生在取token時|
|603|找不到此聯盟|--|
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