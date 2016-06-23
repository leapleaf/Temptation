# 取得當前boss資訊  get_boss_activity2


API編碼:2.2.1

更新日期:

SVN版本:

發布版本:2.0.6,2.0.8
### 1.路徑:fight/get_boss_activity2

### 2. 說明
取得當前boss資訊,可取得當前報名玩家資訊
### 3. 輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |
| -- | -- | -- | -- | -- |
|lang|語系|string|2|--|
|activity_id|目前boss活動id|int|2|與boss_id相同|


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |版本
| -- | -- | -- | -- | -- |--|
| err_code | 回傳參數碼 | string |--|
| err_desc | 回傳參數碼說明 | string | -- |
|stage|當前boss資訊|array|key|
|name|boss名稱|string|--|
|description|boss描述|string|--|
|alreadySignup|玩家本人是否報名|bool|--|
|alreadyFight|玩家本人是否已戰鬥過|bool|--|
|bg_image_path|背景圖路徑|string|--|
|boss_image_path|boss圖路徑|string|--|
|boss_name_id|boss名稱id|int|--|
|boss_hp|boss hp|int|--|
|boss_atk|boss atk|int|--|
|boss_def|boss def|int|--|
|boss_skillBuildID|boss技能組id|int|--|
|start_remaining_time|距離開戰剩餘時間|int|秒數|
|signup_remaining_time|距離報名開始剩餘時間|int|秒數|
|end_remaining_time|Boss戰結束時間|int|秒數|2.0.8
|can_singup|可否報名|bool|--|
|can_start|可否開戰|bool|--|
|otherPlayers|其他玩家資訊|array|key|
|nickname|玩家暱稱|string|--|
|lv|等級|int|--|
|model|模組|int|--|
|duty|職能|int|--|
|pet_id|主牌|int|--|
|power|戰力|int|--|
|alliance_short_name|聯盟短名稱|string|--|




### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|


### 6.回傳格式範例

```
array (size=3)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'stage' => 
    array (size=16)
      'name' => string '推特西里' (length=12)
      'description' => string '豹頭，獅身，熊腳，怒吼，龐大的怒氣在身上燃燒，攻擊方式是怒吼與熊腳。' (length=102)
      'alreadySignup' => boolean false
      'alreadyFight' => boolean false
      'bg_image_path' => string '302004' (length=6)
      'boss_image_path' => string '302004' (length=6)
      'boss_name_id' => int 761074
      'otherPlayers' => 
  array (size=3)
    0 => 
      array (size=4)
        'nickname' => string 'QQ30號' (length=7)
        'lv' => string '65' (length=2)
        'power' => int 82280
        'alliance_short_name' => string 'TS4' (length=3)
    1 => 
      array (size=4)
        'nickname' => string 'yee' (length=3)
        'lv' => string '51' (length=2)
        'power' => int 53525
        'alliance_short_name' => string 'QAQ' (length=3)
  2 => 
      array (size=4)
        'nickname' => string '吃飯了' (length=9)
        'lv' => string '100' (length=3)
      'power' => int 88580
        'alliance_short_name' => string 'qqq' (length=3)
      'boss_hp' => int 18500
      'boss_atk' => int 9050
      'boss_def' => int 3950
      'boss_skillBuildID' => int 100405
      'start_remaining_time' => int 0
      'end_remaining_time' => int 20223
      'signup_remaining_time' => int 0
      'can_singup' => boolean false
      'can_start' => boolean true
      ```
