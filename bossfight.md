# boss_fight

# boss戰設置 boss_fight_setup


API編碼:2.2.4

更新日期:

SVN版本:

發布版本:2.0.6
### 1.路徑:fight/boss_fight_setup

### 2. 說明
設置boss戰,開戰前5分鐘才可設置,最後1分鐘關閉設置,只能設一個部隊,
call 這隻api前請先用set_skills設置 type=1(boss),若是未設置會自動抓type=2
### 3. 輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |
| -- | -- | -- | -- | -- |
|pet1|部隊|int|--|若玩家未設置,boss戰開始時|
|items|道具|jsoncode|最大數量10 |ex:[{\"item_id\":1,\"num\":3},{\"item_id\":2,\"num\":3},{\"item_id\":3,\"num\":3}]|
|


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |--|
| err_desc | 回傳參數碼說明 | string | -- |


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|910|版本已過期，需更新APP資料|
|123|You don't joined this activity|
|195|不在BOSS戰可配置時間|
|182|You can't use special pet in this fight mode|
|181|配置物品數量超過10個|
|131|The Pet1 is not exist|




### 6.回傳格式範例

```
#### var_dump_fortest start ####
array (size=3)
  0 => 
    array (size=2)
      'enegy_percent' => int 100
      'ball_used' => boolean false
  1 => 
    array (size=2)
      'enegy_percent' => int 4
      'ball_used' => boolean false
  2 => 
    array (size=2)
      'enegy_percent' => int -1
      'ball_used' => boolean false
#### var_dump_fortest end ####

#### var_dump_fortest start ####
array (size=21)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'pet1' (length=4)
  'finish' => boolean false
  'originPetHp' => int 15700
  'pet_hp' => int 7626
  'pet_damage' => int 8074
  'pet_buff' => 
    array (size=0)
      empty
  'boss_buff' => 
    array (size=0)
      empty
  'originBossHp' => float 64350
  'boss_damage' => string '1000' (length=4)
  'boss_hp' => float 63350
  'boss_critical' => boolean true
  'canFightAgain' => int 1
  'hasAlivePet' => boolean true
  'skill_cdtime_info' => 
    array (size=1)
      0 => 
        array (size=2)
          'skill_id' => string '10000101' (length=8)
          'remaining_time' => int 1
  'energy' => int 100
  'heal' => boolean false
  'pre_critical' => boolean true
  'pre_miss' => boolean false
  'use_revive' => boolean false
  'revive_status' => 
    array (size=4)
      'revive_max' => int 2
      'total_dmg' => int 1000
      'have_init_revive_space' => boolean true
      'revive_balls' => 
        array (size=3)
          0 => 
            array (size=2)
              ...
          1 => 
            array (size=2)
              ...
          2 => 
            array (size=2)
              ...
      ```





{"err_code":"000","err_desc":"","finish":false,"originPetHp":0,"pet_hp":0,"pet_damage":0,"pet_buff":[],"boss_buff":[],"originBossHp":24350,"boss_damage":0,"boss_hp":24350,"boss_critical":false,"canFightAgain":1,"hasAlivePet":false}
