#修改聯盟招募 alliance_change_recruit






API編碼:2.0.25

> 


更新日期:2016/05/

> 

SVN版本:153??.

> 

發布版本:2.0.0


關聯資料庫:

C:create;R:read;U:update;D:delete;

|Table Name|行為|備註|
|--|--|--|
|alliance|R,U|--|
|character|R|--|
|alliance_member|R|--|
### 1.路徑:alliance/alliance_change_recruit

### 2. 說明
修改聯盟招募條件,0 為限制招募,需輸入戰力及等級,1為公開不須輸入戰力等級
recuit
### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
|character_id|角色id|int|4|帶入token|
|recruit|公開招募|int|1:公開,0:限制招募|
|level|等級|int|限制招募等級,|
|power|戰力|int|限制招募戰力|


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |  |
| err_desc | 回傳參數碼說明 | string | -- |




### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|601|無此權限|
|602|不屬於任何聯盟|

### 6.回傳格式範例

```
array (size=3)

  'err_code' => string '000' (length=3)
  
  'err_desc' => string 'success' (length=7)
```

