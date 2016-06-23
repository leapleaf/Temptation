# boss_fight_supply


API編碼:2.2.5

更新日期:

SVN版本:

發布版本:2.0.8
### 1.路徑:fight/boss_fight_supply

### 2. 說明



新增輸入參數use_items,回傳參數:attack_rate

### 3. 輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |版本
| -- | -- | -- | -- | -- |--|
|boss_activity_id|目前boss戰boss_id|int|--|--|--|



### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |版本|
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |--|
| err_desc | 回傳參數碼說明 | string | -- |
|boss_hp|boss戰是否結束|bool|--|
|boss_max_hp|原始pet hp|int|call api前|
|pet_key|目前pet hp|int|call api後|
|pet_id|pet被傷害|int|被boss打|
|petMaxHp|pet 最大hp|int|--|
|pet_hp|pet現在hp|int|--|
|pet_attack|ATK|int|--|--|
|pet_defense|DEF|int|--|--|
|act_skill_id3|大絕|int|--|--|
|revive_remaingtime|復活CD|int|--|2.0.8|



### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|000|pet1 or ''|
|910|版本已過期，需更新APP資料|
|121|Fight information don't initialize yet.|
|123|You don't joined this activity|
|121|Boss information don't initialize yet,This boss fight dosen't start yet.|





### 6.回傳格式範例
#####部隊活著
```
array (size=12)
  'err_code' => string '000' (length=3)
  'err_desc' => string '' (length=0)
  'boss_hp' => int 234000
  'boss_max_hp' => int 234000
  'pet_key' => string '' (length=0)
  'pet_id' => int 0
  'petMaxHp' => int 0
  'pet_hp' => int 0
  'pet_attack' => int 0
  'pet_defense' => int 0
  'act_skill_id3' => int 0
  'revive_remaingtime' => int 0
      ```

```


