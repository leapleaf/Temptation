# 驅逐聯盟成員 dismiss_member





API編碼:2.0.10





更新日期:2016/4/25

> 

SVN版本:15358.



發布版本:2.0.0


關聯資料庫:

C:create;R:read;U:update;D:delete;

|Table Name|行為|備註|
|--|--|--|
|alliance|R|--|
|character|R|--|
|alliance_member|R,D|--|
|alliance_donate_history|D|--|


### 1.路徑:alliance/dismiss_member

### 2. 說明

驅逐聯盟成員，只有rank2以上的成員可以驅逐成員,同時不得驅逐同職位者.
### 3. 輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |
| -- | -- | -- | -- | -- |
|character_id |角色ID|int|4|可由token取得(clinet可不用輸入|
|outcast|被驅逐者|string|--|暱稱|



### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |--|
| err_desc | 回傳參數碼說明 | string | -- |




### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|601|權限不足|
|602|不屬於任何聯盟|
|605|該玩家不屬於此聯盟|

### 6.回傳格式範例

```array (size=2)

  'err_code' => string '000' (length=3)
  
  'err_desc' => string 'success' (length=7)```