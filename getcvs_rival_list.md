# 取得仇敵清單 get_cvs_rival_list



API編碼:2.9.5

> 


更新日期:

> 

SVN版本:


發布版本:2.0.2

### 1.路徑:card_versus/get_cvs_rival_list

### 2. 說明
取得仇敵人員清單,


### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |版本|
| -- | -- | -- | -- | -- |--|
| err_code | 回傳參數碼 | string |  |--|
| err_desc | 回傳參數碼說明 | string | -- |--|
|rival_list|結果|array|key|--|
|nickname|暱稱|string|--|--|
|alliance_name|聯盟名稱|string|--|--|
|alliance_sname|聯盟短名稱|string|--|--|
|lv|等級|int|--|--|
|power|戰力|int|--|--|
|win_count|勝場數|int|--|--|
|avert_endtime|免戰剩餘時間|int|秒數|--|
|exp|經驗值|int|--|--|
|model|模型|int|--|--|
|rank|排名|int|--|競技場排名|
|fightable|可否攻擊|boolean|--|--|


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|



### 6.回傳格式範例



```
array (size=8)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'loser_list' => 
     0 => 
    array (size=14)
      'nickname' => string 'QQ30號' (length=7)
      'lv' => int 68
      'exp' => int 431487
      'model' => int 0
      'fightable' => boolean false
      'fought' => boolean false
      'win_count' => int 1
      'duty' => int 2
      'rank' => int 2
      'power' => int 83507
      'online' => boolean false
      'avert_endtime' => int 0
      'alliance_name' => string 'GGGGG' (length=5)
      'alliance_sname' => string 'GGG' (length=3)
  1 => &
    array (size=14)
      'nickname' => string 'QAQ' (length=3)
      'lv' => int 13
      'exp' => int 6960
      'model' => int 6
      'fightable' => boolean false
      'fought' => boolean true
      'win_count' => int 1
      'duty' => int 2
      'rank' => int 0
      'power' => int 65793
      'online' => boolean false
      'avert_endtime' => int 0
      'alliance_name' => string 'QAQQ' (length=4)
      'alliance_sname' => string 'QAQ' (length=3)
```