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
|attacker_score|挑戰者分數|int||--|
|defender_score|防禦者分數|int|--|--|
|win|挑戰結果|boolean||--|


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|196|競技場尚未開啟|
|112|not found character|
|113|action point is not enough|


### 6.回傳格式範例

```
array (size=5)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'attacker' => 
    array (size=13)
      'attacker_score' => int 65
      'lv' => int 100
      'duty' => int 3
      'theology' => int 0
      'belief' => int 0
      'versus_rate' => float 0.75
      'troop_rate' => float 1.2
      'hp' => int 270
      'def' => int 385
      'atk' => int 415
      'skill_rate' => float 1.25
      'skill_power' => int 0
      'equip_plus' => 
        array (size=5)
          'hp' => int 0
          'atk' => int 0
          'def' => int 0
          'theology' => int 0
          'belief' => int 0
  'deffender' => 
    array (size=13)
      'defender_score' => int 33
      'lv' => int 24
      'duty' => int 1
      'theology' => int 20
      'belief' => int 20
      'versus_rate' => float 1.5
      'troop_rate' => float 0
      'hp' => int 310
      'def' => int 25
      'atk' => int 5
      'skill_rate' => float 0
      'skill_power' => int 0
      'equip_plus' => 
        array (size=5)
          'hp' => int 300
          'atk' => int 0
          'def' => int 20
          'theology' => int 0
          'belief' => int 0
  'win' => boolean true
```

