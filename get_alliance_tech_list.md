# 取得聯盟資訊 get_alliance_tech_list



API編碼:2.1.1

> 


更新日期:2016/04/29

> 

SVN版本:15445..

> 

發布版本:2.0.0
### 1.路徑:alliance_tech/get_alliance_tech_list

### 2. 說明

取得聯盟科技資訊,取得的是可研發科技清單
### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
|character_id|聯盟名稱|string|12|取token,client不須輸入|


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |版本|
| -- | -- | -- | -- | -- |--|
| err_code | 回傳參數碼 | string |  |--|
| err_desc | 回傳參數碼說明 | string | -- |--|
|alliance_tech_id|聯盟科技id|int|--|--|
|exp|現在科技研發值|int|--|--|
|threshold|此科技升級閥值|int|--|--|
|remiaining_time|升級剩餘時間|int|--|--|
|can_levleup|可升級|boolean|--|--|
|open|是否開啟|boolean|--|2.0.1|
|project|--|int|--|--|
|tectype|--|int|--|--|
|member_score|個人積分|int|--|--|
|donate_cdtime|個人捐獻cd|int|--|--|
|donate_lock|捐獻鎖定|int|1為鎖住|--|

### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|601|權限不足|
|602|不屬於任何聯盟|

### 6.回傳格式範例

```
array (size=6)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'tech_list' => 
    array (size=19)
      0 => 
        array (size=8)
          'alliance_tech_id' => int 100000
          'exp' => int 0
          'threshold' => int 1000
          'remaining_time' => int 0
          'can_levelup' => boolean false
          'open' => boolean false
          'project' => int 1
          'tectype' => int 1
      1 => 
        array (size=8)
          'alliance_tech_id' => int 100100
          'exp' => int 0
          'threshold' => int 1000
          'remaining_time' => int 0
          'can_levelup' => boolean false
          'open' => boolean false
          'project' => int 1
          'tectype' => int 2
............          
  'member_score' => int 1460
  'donate_cdtime' => int 0
  'donate_lock' => boolean false
  'top'=>1;
  ```

