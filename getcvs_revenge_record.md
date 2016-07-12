# 仇敵挑戰紀錄get_cvs_revenge_record


API編碼:2.9.1

> 


更新日期:

> 

SVN版本:


發布版本:2.0.2

### 1.路徑:rank/get_card_versus_record

### 2. 說明
查詢競技場排名,type==0為歷史,==1為今日,==2為本周
ver2.0.5 type ==1為今日;type==2為本次活動;type==3為歷史
### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
|type|種類|int|--|--|


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |版本|
| -- | -- | -- | -- | -- |--|
| err_code | 回傳參數碼 | string |  |--|
| err_desc | 回傳參數碼說明 | string | -- |--|
|result|結果|array|key|--|
|character|腳色參數|array|key|--|
|nickname|暱稱|string|--|--|
|alliance_name|聯盟|string|--|--|
|alliance_short_name|聯盟|string|--|--|
|lv|等級|int|--|--|
|power|戰力|int|--|--|
|victory_rate|勝率|int|--|--|
|total_pk|總場次|int|不含平手|--|
|avert_endtime|免戰剩餘時間|int|秒數|--|
|rank|排名|int|--|--|
|score|個人積分|int|--|--|
|model|模型|int|--|--|
|duty|職能|int|--|--|



### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|196|競技場尚未開啟|
|112|not found character|
|113|action point is not enough|
|173|敵方免戰中|
|197|你沒有分身術,不能打自己|


### 6.回傳格式範例

```

array (size=4)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'result' => 
    array (size=18)
      0 => 
        array (size=12)
          'nickname' => string '吃飯了' (length=9)
          'alliance_name' => string 'ere' (length=3)
          'alliance_short_name' => string 'ewr' (length=3)
          'lv' => int 100
          'power' => int 12542
          'victory_rate' => float 0.39047619047619
          'total_pk' => int 210
          'avert_endtime' => int 0
          'rank' => int 1
          'score' => int 180
          'model' => int 6
          'duty' => int 3
      1 => 
        array (size=12)
          'nickname' => string 'yee' (length=3)
          'alliance_name' => string 'QAQQ' (length=4)
          'alliance_short_name' => string 'QAQ' (length=3)
          'lv' => int 51
          'power' => int 49361
          'victory_rate' => float 0.77692307692308
          'total_pk' => int 130
          'avert_endtime' => int 0
          'rank' => int 2
          'score' => int 130
          'model' => int 1
          'duty' => int 3
      2 => 
        array (size=12)
          'nickname' => string 'QQ30號' (length=7)
          'alliance_name' => string 'TEST4' (length=5)
          'alliance_short_name' => string 'TS4' (length=3)
          'lv' => int 57
          'power' => int 83309
          'victory_rate' => float 1
          'total_pk' => int 67
          'avert_endtime' => int 0
          'rank' => int 3
          'score' => int 110
          'model' => int 0
          'duty' => int 1
      3 => 
        array (size=12)
          'nickname' => string 'Iori' (length=4)
          'alliance_name' => string '' (length=0)
          'alliance_short_name' => string '' (length=0)
          'lv' => int 24
          'power' => int 1385
          'victory_rate' => float 0.75
          'total_pk' => int 8
          'avert_endtime' => int 0
          'rank' => int 4
          'score' => int 0
          'model' => int 1
          'duty' => int 1
      4 => 
        array (size=12)
          'nickname' => string 'QQ26號' (length=7)
          'alliance_name' => string '' (length=0)
          'alliance_short_name' => string '' (length=0)
          'lv' => int 22
          'power' => int 84317
          'victory_rate' => float 0
          'total_pk' => int 2
          'avert_endtime' => int 0
          'rank' => int 4
          'score' => int 0
          'model' => int 0
          'duty' => int 1
      5 => 
        array (size=12)
          'nickname' => string 'QQ37號' (length=7)
          'alliance_name' => string '' (length=0)
          'alliance_short_name' => string '' (length=0)
          'lv' => int 55
          'power' => int 82662
          'victory_rate' => float 0
          'total_pk' => int 1
          'avert_endtime' => int 0
          'rank' => int 4
          'score' => int 0
          'model' => int 0
          'duty' => int 1
      6 => 
        array (size=12)
          'nickname' => string 'd' (length=1)
          'alliance_name' => string '' (length=0)
          'alliance_short_name' => string '' (length=0)
          'lv' => int 50
          'power' => int 9421
          'victory_rate' => float 0
          'total_pk' => int 1
          'avert_endtime' => int 0
          'rank' => int 4
          'score' => int 0
          'model' => int 0
          'duty' => int 1

  'character' => 
    array (size=1)
      0 => 
        array (size=12)
          'nickname' => string 'wade' (length=4)
          'alliance_name' => string '' (length=0)
          'alliance_short_name' => string '' (length=0)
          'lv' => int 24
          'power' => int 67462
          'victory_rate' => float 0
          'total_pk' => int 99
          'avert_endtime' => int 0
          'rank' => int 4
          'score' => int 0
          'model' => int 1
          'duty' => int 1
```

