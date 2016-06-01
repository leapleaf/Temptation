#比牌 fight/card_versus


###注意equip_value帶入pet_id要0


API編碼:2.9.0

> 


更新日期:

> 

SVN版本:

> 

發布版本:2.0.3
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
|alliance_name|聯盟名稱|string|--|--|
|alliance_short_name|聯盟短名稱|string|--|--|
|nickname|暱稱|string|--|--|
|model|模組|int|--|--|
|pet_id|寵物id|--|--|
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
|equip_plus|裝備加成|array|key|--|
|hp|血量|int|--|--|
|def|防禦|int|--|--|
|atk|攻擊力|int|--|--|
|theology|虔誠|int|--|--|
|belief|信仰|int|--|--|
|win|挑戰結果|int|1:win,0:lose,-1:draw|--|
|win_count|連勝次數|int|--|--|
|win_gold|贏得金幣|int|--|--|
|surplus|剩餘場次|int|--|--|
|total_win|總勝場|int|--|--|
|total_lose|總敗場|int|--|--|
|personal_get_point|個人取得積分|int|--|--|
|alliance_get_point|聯盟獲得積分|int|--|--|


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|196|競技場尚未開啟|
|112|not found character|
|197|你沒有分身術,不能打自己|
|199|不得重複打對手|
|198|你已達今日戰鬥上限|
|113|action point is not enough|
|173|敵方免戰中|
|170|對手 vs 挑戰者 PK冷卻中|


### 6.回傳格式範例

```
array (size=8)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'character_rank' => int 1
  'surplus' => int 11
  'card_vs_event' => 
    array (size=1)
      0 => 
        array (size=5)
          'activity_id' => string '888' (length=3)
          'type' => int 1
          'description' => string '0' (length=1)
          'reward' => string '' (length=0)
          'remaining_time' => int 39159
  'result' => 
    array (size=20)
      0 => 
        array (size=17)
          'nickname' => string 'QQ30號' (length=7)
          'alliance_name' => string 'TEST4' (length=5)
          'alliance_short_name' => string 'TS4' (length=3)
          'lv' => int 57
          'power' => int 79831
          'victory_rate' => float 1
          'total_pk' => int 1
          'win_count' => int 1
          'lose_count' => int 0
          'online' => boolean false
          'exclude_pk_count_down' => int 0
          'exp' => int 265625
          'model' => int 0
          'duty' => int 3
          'rank' => int 3
          'fightable' => boolean true
          'fought' => boolean true
      1 => 
        array (size=17)
          'nickname' => string '吃飯了' (length=9)
          'alliance_name' => string 'qqqq' (length=4)
          'alliance_short_name' => string 'qqq' (length=3)
          'lv' => int 100
          'power' => int 13406
          'victory_rate' => float 1
          'total_pk' => int 1
          'win_count' => int 1
          'lose_count' => int 0
          'online' => boolean false
          'exclude_pk_count_down' => int 0
          'exp' => int 224210
          'model' => int 6
          'duty' => int 1
          'rank' => int 2
          'fightable' => boolean true
          'fought' => boolean true
      2 => 
        array (size=17)
          'nickname' => string 'A2233' (length=5)
          'alliance_name' => string '' (length=0)
          'alliance_short_name' => string '' (length=0)
          'lv' => int 2
          'power' => int 5253
          'victory_rate' => float 0
          'total_pk' => int 0
          'win_count' => int 0
          'lose_count' => int 0
          'online' => boolean false
          'exclude_pk_count_down' => int 0
          'exp' => int 280
          'model' => int 2
          'duty' => int 1
          'rank' => int 0
          'fightable' => boolean true
          'fought' => boolean false

  'cvs_cd_time' => int 2988
  'cvs_lock' => boolean true
```

