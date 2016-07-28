# 取得聯盟資訊 get_alliance_info



API編碼:2.0.3

> 


更新日期:2016/04/26

> 

SVN版本:15355.

> 

發布版本:2.0.0


關聯資料庫:

C:create;R:read;U:update;D:delete;

|Table Name|行為|備註|
|--|--|--|
|alliance|R|--|
|character|R|--|
|alliance_member|R|--|

### 1.路徑:alliance/get_alliance_info

### 2. 說明

取得聯盟資訊,先判斷有無輸入聯盟名稱,若無則搜尋自身聯盟.未輸入alliance_member多吐position
### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
|alliance_name|聯盟名稱|string|12|若未輸入帶入token(名稱一致)|


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |  |
| err_desc | 回傳參數碼說明 | string | -- |
|alliance_name|聯盟名稱|string|--|
|shortname|聯盟短名稱|string|--|
|lang|語系|string|--|
|introduction|聯盟簡介|string|--|
|flag|聯盟旗幟|int|--|
|createtime|創立時間|string|--|
|member_count|成員人數|int|--|
|max_member|成員最大數|int|--|
|leader_name|盟主|string|--|
|total_power|聯盟戰力|int|--|
|stint_level|限制等級|int|--|
|stint_power|限制戰力|int|--|
|recuit|公開招募|int|1為公開|
|position|職位|int|未輸入alliance_member吐|


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|602|不屬於任何聯盟|
|603|找不到此聯盟|

### 6.回傳格式範例

```
array (size=11)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'alliance_name' => string '123' (length=3)
  'shortname' => string 'en' (length=2)
  'lang' => string 'A' (length=1)
  'introduction' => string 'introduction' (length=12)
  'flag' => int 1
  'createtime' => string '2016-04-13 09:47:07' (length=19)
  'member_count' => int 35
  'leader_name' => string 'wade' (length=4)
  'total_power' => string '548818' (length=6)
```

