# 仇敵挑戰紀錄 get_cvs_revenge_record


API編碼:2.9.1

> 


更新日期:

> 

SVN版本:


發布版本:2.0.2

### 1.路徑:card_versus/get_cvs_revenge_record

### 2. 說明
查詢仇敵挑戰紀錄

### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
|type|種類|int|--|--|


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |版本|
| -- | -- | -- | -- | -- |--|
| err_code | 回傳參數碼 | string |  |--|
| err_desc | 回傳參數碼說明 | string | -- |--|
|record|紀錄|array|key|--|
|character|腳色參數|array|key|--|
|nickname|暱稱|string|--|--|
|alliance_name|聯盟|string|--|--|
|alliance_sname|聯盟|string|--|--|
|lv|等級|int|--|--|
|power|戰力|int|--|--|
|victory_rate|勝率|int|--|--|
|total_pk|總場次|int|不含平手|--|
|avert_endtime|免戰剩餘時間|int|秒數|--|
|rank|排名|int|--|--|
|score|個人積分|int|--|--|
|model|模型|int|--|--|
|exp|經驗值|int|--|--|
|fought|今天是否打過|bool|--|--|
|win|勝負|int|--|--|
|rank|競技場排行|int|--|--|
|power|戰力|int|--|--|
|online|在線|bool|--|--|
|avert_endtime|免戰剩餘時間|int|--|--|
|create_time|建立時間|string|--|--|


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|



### 6.回傳格式範例

```

array (size=4)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'record' => 
    array (size=18)
array (size=10)
  0 => 
    array (size=14)
      'nickname' => string 'A1133' (length=5)
      'lv' => int 64
      'exp' => int 382679
      'model' => int 4
      'fought' => boolean false
      'duty' => int 1
      'win' => int 0
      'rank' => int 5
      'power' => int 85757
      'online' => boolean false
      'avert_endtime' => int 0
      'alliance_name' => string 'XXXX' (length=4)
      'create_time' => string '2016-07-05 16:56:43' (length=19)
      'alliance_sname' => string 'XXX' (length=3)
  1 => 
    array (size=14)
      'nickname' => string 'A1133' (length=5)
      'lv' => int 64
      'exp' => int 382679
      'model' => int 4
      'fought' => boolean false
      'duty' => int 1
      'win' => int 0
      'rank' => int 5
      'power' => int 85757
      'online' => boolean false
      'avert_endtime' => int 0
      'alliance_name' => string 'XXXX' (length=4)
      'create_time' => string '2016-07-05 16:56:00' (length=19)
      'alliance_sname' => string 'XXX' (length=3)

```

