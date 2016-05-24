# 競技場排名 get_card_versus_record


API編碼:2.9.1

> 


更新日期:

> 

SVN版本:


發布版本:2.0.2

### 1.路徑:rank/get_card_versus_record

### 2. 說明
查詢競技場排名
### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
|nickname|暱稱|int|--|被挑戰者|


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |版本|
| -- | -- | -- | -- | -- |--|
| err_code | 回傳參數碼 | string |  |--|
| err_desc | 回傳參數碼說明 | string | -- |--|
|attacker|挑戰者|array|key|--|
|deffender|防禦者|array|key|--|
|score|分數|int|--|--|
|lv|等級|int|--|--|
|duty|職能|int|--|--|
|theology|虔誠|int|--|--|
|belief|信仰|int|--|--|
|versus_rate|職能加成|float|--|--|
|troop_rate|部隊加成|float|--|--|
|hp|血量|int|--|--|
|def|防禦|int|--|--|
|atk|攻擊力|int|--|--|
|skill_rate|技能加成|float|--|--|
|skill_power|技能強度|int|--|--|
|equip_plus|裝備加成|array|key|--|
|hp|血量|int|--|--|
|def|防禦|int|--|--|
|atk|攻擊力|int|--|--|
|theology|虔誠|int|--|--|
|belief|信仰|int|--|--|
|win|挑戰結果|int|1:win,0:lose,-1:draw|--|


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|196|競技場尚未開啟|
|112|not found character|
|113|action point is not enough|
|173|敵方免戰中|


### 6.回傳格式範例

```
array (size=3)
  0 => 
    array (size=7)
      'nickname' => string 'Iori' (length=4)
      'alliance_name' => string '' (length=0)
      'lv' => int 24
      'power' => int 79374
      'victory_rate' => float 1
      'total_pk' => int 3
      'avert_endtime' => int 0
  1 => 
    array (size=7)
      'nickname' => string '吃飯了' (length=9)
      'alliance_name' => string 'ere' (length=3)
      'lv' => int 100
      'power' => int 12542
      'victory_rate' => float 0.88888888888889
      'total_pk' => int 27
      'avert_endtime' => int 0
  2 => 
    array (size=7)
      'nickname' => string 'wade' (length=4)
      'alliance_name' => string '' (length=0)
      'lv' => int 24
      'power' => int 67462
      'victory_rate' => float 0
      'total_pk' => int 27
      'avert_endtime' => int 2301075
```

