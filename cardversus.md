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
ver2.0.3興曾比牌冷卻時間,每次比牌會增加設定表value1冷卻時間,當超過設定表Value2就無法繼續比牌,等到比牌冷卻時間低於等於0才可再比

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
|cvs_cd_time|比牌CD累計時間|int|--|ver2.0.3|
|cvs_lock|是否可比牌|int|--|ver2.0.3|


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

```

