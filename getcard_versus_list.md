# 取得競技人員清單 get_card_versus_list


API編碼:2.9.2

> 


更新日期:

> 

SVN版本:


發布版本:2.0.2

### 1.路徑:rank/get_card_versus_list

### 2. 說明
取得競技人員清單,range為取得範圍 會以exp查詢所在範圍內的所有人的資訊


### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
|range|取得範圍|int|--|--|


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |版本|
| -- | -- | -- | -- | -- |--|
| err_code | 回傳參數碼 | string |  |--|
| err_desc | 回傳參數碼說明 | string | -- |--|
|character_exp_rank|腳色經驗值排名|int|本人|--|
|event|card_versus活動資訊|array|key|--|
|activity_id|活動id|string|--|--|
|type|活動類型|int|--|--|
|description|活動描述|string|--|--|
|reward|活動獎勵|string|--|--|
|remaining_time|活動剩餘時間|--|--|
|result|結果|array|key|--|
|nickname|暱稱|string|--|--|
|alliance_name|聯盟名稱|string|--|--|
|alliance_short_name|聯盟短名稱|string|--|--|
|lv|等級|int|--|--|
|power|戰力|int|--|--|
|victory_rate|勝率|int|--|--|
|total_pk|總場次|int|不含平手|--|
|win_count|勝場數|int|--|--|
|lose_count|敗場數|int|--|--|
|exclude_pk_count_down|免戰剩餘時間|int|秒數|--|
|exp|經驗值|int|--|--|
|model|模型|int|--|--|
|rank|排名|int|--|--|
|fightable|可否攻擊|boolean|--|--|

### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|



### 6.回傳格式範例



```
array (size=5)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'character_rank' => int 4
  'card_vs_event' => 
    array (size=1)
      0 => 
        array (size=5)
          'activity_id' => string '888' (length=3)
          'type' => int 1
          'description' => string '0' (length=1)
          'reward' => string '' (length=0)
          'remaining_time' => int 23368
  'result' => 
    array (size=10)
      0 => 
        array (size=17)
          'nickname' => string 'yee' (length=3)
          'alliance_name' => string 'QAQQ' (length=4)
          'alliance_short_name' => string 'QAQ' (length=3)
          'lv' => int 51
          'power' => int 49361
          'victory_rate' => float 0.91549295774648
          'total_pk' => int 71
          'win_count' => int 65
          'lose_count' => int 6
          'online' => boolean false
          'exclude_pk_count_down' => int 0
          'exp' => int 149993
          'model' => int 1
          'duty' => int 3
          'rank' => int 2
          'fightable' => boolean true
          'fought' => boolean false
      1 => 
        array (size=17)
          'nickname' => string 'A4455' (length=5)
          'alliance_name' => string '' (length=0)
          'alliance_short_name' => string '' (length=0)
          'lv' => int 1
          'power' => int 2647
          'victory_rate' => float 0
          'total_pk' => int 0
          'win_count' => int 0
          'lose_count' => int 0
          'online' => boolean false
          'exclude_pk_count_down' => int 0
          'exp' => int 84
          'model' => int 3
          'duty' => int 1
          'rank' => int 0
          'fightable' => boolean true
          'fought' => boolean false
      
```