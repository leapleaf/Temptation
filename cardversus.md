#比牌 fight/card_versus





API編碼:2.9.0

> 


更新日期:

> 

SVN版本:

> 

發布版本:2.0.2
### 1.路徑:fight/card_versus

### 2. 說明
依據開放時間開放競技場,啟動後挑戰者扣減行動值,挑戰者勝利可獲的道具獎勵

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
|170|對手 vs 挑戰者 PK冷卻中|


### 6.回傳格式範例

```
array (size=10)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'attacker' => 
    array (size=16)
      'alliance_name' => string 'ere' (length=3)
      'alliance_short_name' => string 'ewr' (length=3)
      'nickname' => string '吃飯了' (length=9)
      'model' => int 6
      'pet_id' => int 100101
      'score' => int 86904
      'lv' => int 100
      'duty' => int 3
      'theology' => int 0
      'belief' => int 0
      'versus_rate' => float 0.75
      'troop_rate' => float 1.2
      'hp' => int 270
      'def' => int 385
      'atk' => int 415
      'equip_plus' => 
        array (size=5)
          'hp' => int 0
          'atk' => int 0
          'def' => int 0
          'theology' => int 0
          'belief' => int 0
  'deffender' => 
    array (size=16)
      'alliance_name' => string '""' (length=2)
      'alliance_short_name' => string '""' (length=2)
      'nickname' => string 'wade' (length=4)
      'model' => int 1
      'pet_id' => int 0
      'score' => int 33
      'lv' => int 24
      'duty' => int 1
      'theology' => int 20
      'belief' => int 20
      'versus_rate' => float 1.5
      'troop_rate' => float 0
      'hp' => int 310
      'def' => int 25
      'atk' => int 5
      'equip_plus' => 
        array (size=5)
          'hp' => int 300
          'atk' => int 0
          'def' => int 20
          'theology' => int 0
          'belief' => int 0
  'win' => int 1
  'win_count' => int 1
  'win_gold' => int 0
  'surplus' => int 18
  'total_win' => int 81
  'total_lose' => int 128
```

