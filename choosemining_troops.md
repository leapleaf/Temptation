# 選取採礦 choose_mining_troops




API編碼:2.9.0

> 


更新日期:

> 

SVN版本:

> 

發布版本:2.2.0
### 1.路徑:mining/choose_mining_troops

### 2. 說明
選取採礦地點



以pass_stage_no +-2關卡等級

### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |版本|
| -- | -- | -- | -- | -- | -- |
|mining_sites|採礦地點|int|--|值為1,2,3|--|



### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |版本|
| -- | -- | -- | -- | -- |--|
| err_code | 回傳參數碼 | string |  |--|
| err_desc | 回傳參數碼說明 | string | -- |--|
|stages|活動關卡|array|key|--|
|no|序列數|int|--|--|
|pass_stage_no|已過關卡|int|0無過關,目前最高10|--|
|stage_no|活動關卡|int|地上5關天上15關|--|
|lv|活動關卡等級|int|--|--|
|fought|是否打過|int|打過吐1|--|
|reset_remainingtime|重製剩餘時間|int|低於0吐0|--|



### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|601|權限不足|
|602|不屬於任何聯盟|
|642|科技尚未開放|

### 6.回傳格式範例

```
array (size=4)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'pass_stage_no' => int 0
  'stages' => 
    array (size=20)
      0 => 
        array (size=4)
          'no' => int 1
          'stage_no' => int 2000002
          'fought' => boolean false
          'reset_remainingtime' => int 41
      1 => 
        array (size=4)
          'no' => int 2
          'stage_no' => int 2000002
          'fought' => boolean false
          'reset_remainingtime' => int 41
      2 => 
        array (size=4)
          'no' => int 3
          'stage_no' => int 2000002
          'fought' => boolean false
          'reset_remainingtime' => int 41
      3 => 
        array (size=4)
          'no' => int 4
          'stage_no' => int 2000002
          'fought' => boolean false
          'reset_remainingtime' => int 41
      4 => 
        array (size=4)
          'no' => int 5
          'stage_no' => int 2000001
          'fought' => boolean false
          'reset_remainingtime' => int 41
      5 => 
        array (size=4)
          'no' => int 6
          'stage_no' => int 2000002
          'fought' => boolean false
          'reset_remainingtime' => int 41
      6 => 
        array (size=4)
          'no' => int 7
          'stage_no' => int 2000002
          'fought' => boolean false
          'reset_remainingtime' => int 41
      7 => 
        array (size=4)
          'no' => int 8
          'stage_no' => int 2000001
          'fought' => boolean false
          'reset_remainingtime' => int 41
      8 => 
        array (size=4)
          'no' => int 9
          'stage_no' => int 2000002
          'fought' => boolean false
          'reset_remainingtime' => int 41
      9 => 
        array (size=4)
          'no' => int 10
          'stage_no' => int 2000002
          'fought' => boolean false
          'reset_remainingtime' => int 41
      10 => 
        array (size=4)
          'no' => int 11
          'stage_no' => int 2000001
          'fought' => boolean false
          'reset_remainingtime' => int 41
      11 => 
        array (size=4)
          'no' => int 12
          'stage_no' => int 2000001
          'fought' => boolean false
          'reset_remainingtime' => int 41
      12 => 
        array (size=4)
          'no' => int 13
          'stage_no' => int 2000001
          'fought' => boolean false
          'reset_remainingtime' => int 41
      13 => 
        array (size=4)
          'no' => int 14
          'stage_no' => int 2000002
          'fought' => boolean false
          'reset_remainingtime' => int 41
      14 => 
        array (size=4)
          'no' => int 15
          'stage_no' => int 2000001
          'fought' => boolean false
          'reset_remainingtime' => int 41
      15 => 
        array (size=4)
          'no' => int 16
          'stage_no' => int 2000002
          'fought' => boolean false
          'reset_remainingtime' => int 41
      16 => 
        array (size=4)
          'no' => int 17
          'stage_no' => int 2000002
          'fought' => boolean false
          'reset_remainingtime' => int 41
      17 => 
        array (size=4)
          'no' => int 18
          'stage_no' => int 2000001
          'fought' => boolean false
          'reset_remainingtime' => int 41
      18 => 
        array (size=4)
          'no' => int 19
          'stage_no' => int 2000002
          'fought' => boolean false
          'reset_remainingtime' => int 41
      19 => &
        array (size=4)
          'no' => int 20
          'stage_no' => int 2000002
          'fought' => boolean false
          'reset_remainingtime' => int 41
```

