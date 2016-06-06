#進入競技場 enter_card_versus_arena





API編碼:2.9.5

> 


更新日期:

> 

SVN版本:

> 

發布版本:2.0.3
### 1.路徑:fight/enter_card_versus_arena

### 2. 說明
進入競技場，取得個人腳色資訊與前10名名單

### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |版本|
| -- | -- | -- | -- | -- |--|
| err_code | 回傳參數碼 | string |  |--|
| err_desc | 回傳參數碼說明 | string | -- |--|
|card_vs_event|card_versus活動資訊|array|key|--|
|activity_id|活動id|string|--|--|
|type|活動類型|int|--|--|
|description|活動描述|string|--|--|
|reward|活動獎勵|string|--|--|
|remaining_time|活動剩餘時間|--|--|
|result|結果|array|key|--|
|nickname|暱稱|string|--|--|
|lv|等級|int|--|--|
|model|模型|int|--|--|
|duty|職能|int|--|--|
|rank|排名|int|--|--||
|win_count|勝場數|int|--|--|
|lose_count|敗場數|int|--|--|
|total_pk|總場次|int|不含平手|--|
|power|戰力|int|--|--|
|score|累計積分|int|--|--|
|victory_rate|勝率|int|--|--|
|avert_endtime|免戰剩餘時間|int|秒數|--|
|alliance_name|聯盟名稱|string|--|--|
|alliance_short_name|聯盟短名稱|string|--|--|
|skill_ids|技能組|array|key|--|
|cvs_cd_time|cvs冷卻時間|int|--|2.0.5|
|cvs_lock|cvs鎖定|boolean|--|2.0.5|



### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|



### 6.回傳格式範例

```
array (size=7)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'card_vs_event' => 
    array (size=1)
      0 => 
        array (size=5)
          'activity_id' => string '888' (length=3)
          'type' => int 1
          'description' => string '0' (length=1)
          'reward' => string '' (length=0)
          'remaining_time' => int 37064
  'result' => 
    array (size=9)
      0 => 
        array (size=14)
          'nickname' => string 'yee' (length=3)
          'lv' => int 51
          'model' => int 1
          'duty' => int 3
          'rank' => int 1
          'win_count' => int 35
          'lose_count' => int 5
          'total_pk' => int 40
          'power' => int 49361
          'score' => int 840
          'victory_rate' => float 0
          'avert_endtime' => int 0
          'alliance_name' => string 'QAQQ' (length=4)
          'alliance_short_name' => string 'QAQ' (length=3)
      1 => 
        array (size=14)
          'nickname' => string 'QQ30號' (length=7)
          'lv' => int 65
          'model' => int 0
          'duty' => int 2
          'rank' => int 2
          'win_count' => int 46
          'lose_count' => int 0
          'total_pk' => int 46
          'power' => int 82280
          'score' => int 660
          'victory_rate' => float 0
          'avert_endtime' => int 0
          'alliance_name' => string 'TEST4' (length=5)
          'alliance_short_name' => string 'TS4' (length=3)

  'character' => 
    array (size=1)
      0 => 
        array (size=22)
          'nickname' => string 'qqqQ' (length=4)
          'alliance_name' => string '' (length=0)
          'alliance_short_name' => string '' (length=0)
          'lv' => int 1
          'power' => int 1363
          'victory_rate' => float 0.8
          'total_pk' => int 10
          'win_count' => int 8
          'lose_count' => int 2
          'pet_id' => int 0
          'skill_ids' => 
            array (size=0)
              ...
          'online' => boolean false
          'exclude_pk_count_down' => int 0
          'model' => int 1
          'duty' => int 3
          'rank' => int 7
          'pet_hp' => int 10
          'pet_atk' => int 5
          'pet_def' => int 5
          'pet_hp_equip' => int 0
          'pet_atk_equip' => int 0
          'pet_def_equip' => int 0
  'cvs_cd_time' => int 0
  'cvs_lock' => boolean false

```

