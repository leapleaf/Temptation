# boss戰設置 boss_fight_setup


API編碼:2.2.3

更新日期:

SVN版本:

發布版本:2.0.6,2.0.8
### 1.路徑:fight/boss_fight_setup

### 2. 說明
設置boss戰,開戰前5分鐘才可設置,最後1分鐘關閉設置,只能設一個部隊,
call 這隻api前請先用set_skills設置 type=1(boss),若是未設置會自動抓type=2

ver2.0.8:移除輸入道具
### 3. 輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |版本|
| -- | -- | -- | -- | -- |--|
|pet1|部隊|int|--|若玩家未設置,boss戰開始時|--|
|items|道具|jsoncode|最大數量10 |ex:[{\"item_id\":1,\"num\":3},{\"item_id\":2,\"num\":3},{\"item_id\":3,\"num\":3}]|2.0.8移除|
|


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |--|
| err_desc | 回傳參數碼說明 | string | -- |


### 5. 錯誤代碼說明
|錯誤代碼|意義|版本|
|--|--|
|910|版本已過期，需更新APP資料|
|123|You don't joined this activity|
|195|不在BOSS戰可配置時間|
|182|You can't use special pet in this fight mode|
|181|配置物品數量超過10個|2.0.8移除|
|131|The Pet1 is not exist|




### 6.回傳格式範例

```
array (size=4)
  'err_code' => string '000' (length=3)
  'err_desc' => string '' (length=0)
  'petInfo1' => 
    array (size=21)
      'pet_id' => int 100101
      'lv' => int 10
      'series' => int 101
      'max_hp' => int 16700
      'hp' => int 16700
      'attack' => int 551
      'defense' => int 431
      'act_skill_id1' => int 10000101
      'act_skill_id2' => int 10000301
      'act_skill_id3' => int 0
      'pas_skill_id1' => int 10001101
      'pas_skill_id2' => int 10000601
      'pas_skill_id3' => int 10001401
      'pas_skill_prb1' => int 15
      'pas_skill_prb2' => int 20
      'pas_skill_prb3' => int 20
      'buffList' => 
        array (size=0)
          empty
      'pas_skill_trigger' => int 0
      'recover_hp' => int 0
      'damage_hp' => int 0
      'property' => string '3' (length=1)
  'skills' => 
    array (size=5)
      0 => int 10000110
      1 => int 10000207
      2 => int 10000410
      3 => int 10000803
      4 => int 10001401
      ```





