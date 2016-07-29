# 捐獻排名 get_alliance_donate_rank





API編碼:2.4.1





更新日期:2016/05/04

> 

SVN版本:15501.

> 

發布版本:2.0.0

關聯資料庫:

C:create;R:read;U:update;D:delete;

|Table Name|行為|備註|
|--|--|--|
|alliance|R|--|
|character|R|--|
|alliance_member|R|--|
|alliance_donate_history|R|--|
### 1.路徑:rank/get_alliance_donate_rank

### 2. 說明

取得捐獻排行
### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
| character_id | 繼位者 | int | 11 | 由token取得 |
|type|類型|int|3|1:當日,2:當周,3全部|

### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |--|
| err_desc | 回傳參數碼說明 | string | -- |
|result|結果|array|key|
|nick_name|暱稱|string|--|
|donate_point|捐獻點數|int|--|
|member_point|目前點數|int|--|


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|601|權限不足|
|602|不屬於任何聯盟|

### 6.回傳格式範例

```
array (size=3)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'result' => 
    array (size=1)
      0 => 
        array (size=3)
          'nick_name' => string 'test0123' (length=8)
          'donate_point' => int 50
          'member_point' => string '3020' (length=4)

```




