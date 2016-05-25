# 競技場排名 get_card_versus_record


API編碼:2.9.1

> 


更新日期:

> 

SVN版本:


發布版本:2.0.2

### 1.路徑:rank/get_card_versus_record

### 2. 說明
查詢競技場排名,type==0為歷史,==1為今日,==2為本周
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
    array (size=7)
      0 => 
        array (size=11)
          'nickname' => string 'QAQ' (length=3)
          'alliance_name' => string 'QAQQ' (length=4)
          'alliance_short_name' => string 'QAQ' (length=3)
          'lv' => int 6
          'power' => int 59594
          'victory_rate' => float 1
          'total_pk' => int 32
          'avert_endtime' => int 0
          'rank' => int 1
          'model' => int 6
          'duty' => int 1
      5 => 
        array (size=11)
          'nickname' => string '吃飯了' (length=9)
          'alliance_name' => string 'ere' (length=3)
          'alliance_short_name' => string 'ewr' (length=3)
          'lv' => int 100
          'power' => int 12542
          'victory_rate' => float 0.26086956521739
          'total_pk' => int 92
          'avert_endtime' => int 0
          'rank' => int 6
          'model' => int 6
          'duty' => int 3
      6 => 
        array (size=11)
          'nickname' => string 'wade' (length=4)
          'alliance_name' => string '' (length=0)
          'alliance_short_name' => string '' (length=0)
          'lv' => int 24
          'power' => int 67462
          'victory_rate' => float 0
          'total_pk' => int 40
          'avert_endtime' => int 2202665
          'rank' => int 7
          'model' => int 1
          'duty' => int 1
  'character' => 
    array (size=1)
      0 => 
        array (size=11)
          'nickname' => string 'wade' (length=4)
          'alliance_name' => string '' (length=0)
          'alliance_short_name' => string '' (length=0)
          'lv' => int 24
          'power' => int 67462
          'victory_rate' => float 0
          'total_pk' => int 40
          'avert_endtime' => int 2202665
          'rank' => int 7
          'model' => int 1
          'duty' => int 1
```

