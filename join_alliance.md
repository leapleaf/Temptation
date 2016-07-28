# 加入聯盟 join_alliance



API編碼:2.0.7






更新日期:2016/04/25

> 

SVN版本:15356.

> 

發布版本:2.0.0


關聯資料庫:

C:create;R:read;U:update;D:delete;

|Table Name|行為|備註|
|--|--|--|
|alliance|R|--|
|character|R,U|--|
|alliance_member|R,C|--|
|alliance_tech|C|--|
|alliance_invitation|C|--|


### 1.路徑:alliance_member/join_alliance

### 2. 說明

取得聯盟成員清單,加入聯盟,會先判斷該腳色是否有無聯盟,並依聯盟名稱加入聯盟,
新加入者職位(position)一律為6
### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
| character_id | 角色id | int | 4 |--|
|alliance_name|聯盟名稱|string|18|--|

### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |  |
| err_desc | 回傳參數碼說明 | string | -- |
|position|職位|int|==6 or 7|




### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|603|找不到此聯盟|
|604|你已有所屬聯盟|
|621|超過聯盟人數上限|
### 6.回傳格式範例

```
array (size=3)

  'err_code' => string '000' (length=3)
  
  'err_desc' => string 'success' (length=7)
  ```
