# 搜尋聯盟 search_alliance
可用get_alliance_info取代




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
|leader|盟主|string|--|
| lang | 語系 | string | -- |
|name|聯盟名稱|string|--|
|shortname|聯盟短名稱|string|--|
|total_power|聯盟戰力|int|--|
|flag|聯盟旗幟|int|--|
|introduction|聯盟宣言|string|--|
|createtime|創立時間|string|--|
|member_count|成員人數|int|--|
|max_member|成員最大數|int|--|
|recruit|公開招募|int|--|



### 5. 錯誤代碼說明
|錯誤代碼|意義|說明|
|--|--|--|
|602|不屬於任何聯盟|發生在取token時|
|603|找不到此聯盟|--|
### 6.回傳格式範例

```
array (size=3)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'alliance' => 
    array (size=2)
      0 => 
        array (size=10)
          'alliance_name' => string '123' (length=3)
          'alliance_short_name' => string 'A' (length=1)
          'leader' => string 'wade' (length=4)
          'power' => int 548818
          'lang' => string 'en' (length=2)
          'introduction' => string 'introduction' (length=12)
          'flag' => int 1
          'createtime' => string '2016-04-13 09:47:07' (length=19)
          'max_member' => int 50
          'members_count' => int 37
      1 => 
        array (size=10)
          'alliance_name' => string 'godda112' (length=8)
          'alliance_short_name' => string 'A' (length=1)
          'leader' => string '吃飯了' (length=9)
          'power' => int 82872
          'lang' => string 'en' (length=2)
          'introduction' => string 'introduction' (length=12)
          'flag' => int 1
          'createtime' => string '2016-04-29 07:17:58' (length=19)
          'max_member' => int 50
          'members_count' => int 5
          
          ```