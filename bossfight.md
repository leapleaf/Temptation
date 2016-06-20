# boss_fight


API編碼:2.2.4

更新日期:

SVN版本:

發布版本:2.0.6
### 1.路徑:fight/boss_fight

### 2. 說明
新增復活球,攻擊間隔隨機5~10秒,爆擊判定,miss判定,回血

復活球解說:目前固定三個,key為0,1,2;enegy_percent =-1不會累積復活球能量,

當復活球enegy_percent達到100可開始使用,pet_hp在變為0時會自動使用,由最大用到最小

ex:total_dmg約1000時的狀態 pet hp>0
```
      'revive_balls' => 
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

```
ex:total_dmg約1000時的狀態 pet hp==0(自動使用)
```
      'revive_balls' => 
        array (size=3)
          0 => 
            array (size=2)
              'enegy_percent' => int 100
              'ball_used' => boolean true
          1 => 
            array (size=2)
              'enegy_percent' => int 4
              'ball_used' => boolean false
          2 => 
            array (size=2)
              'enegy_percent' => int -1
              'ball_used' => boolean false     

```
total_dmg 會每次更新復活球,已物件型態存入mem,

pet_hp == 0時,當ball_used ==false &&enegy_percent==100才會使用
### 3. 輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |
| -- | -- | -- | -- | -- |
|boss_activity_id|目前boss戰boss_id|int|--|--|
|type|類型|int|--|0:普攻,1:技能,2:道具|
|value|值|int|--|技能id或道具id|
|energy|能量值|int|--|client算好丟上來同步,目前未用到|
|boss_damage_hp|傷害boss hp|int|--|驗證非法傷害|
|use_items|使用道具|json_code|--|ex:[{\"item_id\":100067,\"num\":1},{\"item_id\":100068,\"num\":2}]|



### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |--|
| err_desc | 回傳參數碼說明 | string | -- |
|finish|boss戰是否結束|bool|--|
|originPetHp|原始pet hp|int|call api前|
|pet_hp|目前pet hp|int|call api後|
|pet_damage|pet被傷害|int|被boss打|
|pet_buff|pet buff|array|key|
|boss_buff|boss buff|array|key|
|originBossHp|原始boss hp|int|call api前|
|boss_damage|boss被傷害|int|boss被pet打|
|boss_hp|目前boss hp|int|call api後|
|is_boss_attack|boss是否攻擊|boolean|原boss_critical|
|canFightAgain|可否再次攻擊|bool|--|
|hasAlivePet|是否有活著的寵物|boolean|--|
|skill_cdtime_info|技能cd資訊|array|key
|skill_id|技能id|int|--|
|remaining_time|剩餘冷卻時間|int|--|
|energy|能量值|int|--|
|heal|boss此次是否回血|boolean|--|
|pre_critical|下次是否爆擊|boolean|--|
|pre_miss|下次是否miss|boolean|--|
|use_revive|是否使用復活球|boolean|此次 call api|
|revive_status|復活求狀態|array|key|
|revive_max|復活球最大數|int|有可能是0,看靜態表|
|total_dmg|目前累計總傷害量|int|--|
|have_init_revive_space|是否有復活球能量槽|boolean|revive_max = 0為false|
|revive_balls|復活球|array|key(固定為陣列3個)|
|enegy_percent|復活球能量槽|int|依total_dmg換算,值為0~100,-1表示不可累積此能量槽|
|ball_used|此復活球是否用過|boolean|--|



### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|000|pet1 or ''|
|910|版本已過期，需更新APP資料|
|121|Fight information don't initialize yet.|
|123|You don't joined this activity|
|121|Boss information don't initialize yet,This boss fight dosen't start yet.|
|224|boss戰時間結束|
|225|非法傷害|




### 6.回傳格式範例
#####部隊活著
```
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
      ```

#####部隊死亡
```
            "err_code" => "000",
            "err_desc" => "",
            "finish" => bool,
            "originPetHp" => 0,
            "pet_hp" => 0,
            "pet_damage" => 0,
            "pet_buff" => [],
            "boss_buff" => [],
            "originBossHp" => int,
            "boss_damage" => 0,
            "boss_hp" => int,
            "boss_critical" => false,
            "canFightAgain" => bool,
            "hasAlivePet" => bool
```

