# +搜尋聯盟預設 search_alliance_default





API編碼:2.0.9





更新日期:

> 

SVN版本:

> 

發布版本:2.0.0


關聯資料庫:

C:create;R:read;U:update;D:delete;

|Table Name|行為|備註|
|--|--|--|
|alliance|R|--|
|character|R|--|
|alliance_member|R|--|
|alliance|R|--|

### 1.路徑:alliance/search_alliance_default

### 2. 說明

抓出所有聯盟,依limit判斷筆數,limit=0則為預設50
### 3. 輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |
| -- | -- | -- | -- | -- |
|limit|筆數|string|--|
|type|筆數|int|1為搜尋自己聯盟以外,0則是全部|
|



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
|錯誤代碼|意義|
|--|--|
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