# 取得競技人員清單 get_card_versus_list


API編碼:2.9.2

> 


更新日期:

> 

SVN版本:


發布版本:2.0.2

### 1.路徑:rank/get_card_versus_list

### 2. 說明
取得競技人員清單,range為取得範圍 會以exp查詢所在範圍內的所有人的資訊


### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
|range|取得範圍|int|--|--|


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |版本|
| -- | -- | -- | -- | -- |--|
| err_code | 回傳參數碼 | string |  |--|
| err_desc | 回傳參數碼說明 | string | -- |--|
|nickname|暱稱|string|--|--|
|alliance_name|聯盟|string|--|--|
|lv|等級|int|--|--|
|power|戰力|int|--|--|
|victory_rate|勝率|int|--|--|
|total_pk|總場次|int|不含平手|--|
|win_count|勝場數|int|--|--|
|lose_count|敗場數|int|--|--|
|exclude_pk_count_down|免戰剩餘時間|int|秒數|--|
|exp|經驗值|int|--|--|
|model|模型|int|--|--|
|rank|經驗值排名|int|--|--|

### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|



### 6.回傳格式範例



```
array (size=10)
  0 => 
    array (size=12)
      'nickname' => string 'QQ39號' (length=7)
      'alliance_name' => string '' (length=0)
      'lv' => int 50
      'power' => int 46792
      'victory_rate' => float 1
      'total_pk' => int 1
      'win_count' => int 1
      'lose_count' => int 0
      'online' => boolean false
      'exclude_pk_count_down' => int 0
      'exp' => int 218500
      'rank' => int 10
  1 => 
    array (size=12)
      'nickname' => string 'Iori' (length=4)
      'alliance_name' => string '' (length=0)
      'lv' => int 24
      'power' => int 79374
      'victory_rate' => float 1
      'total_pk' => int 3
      'win_count' => int 3
      'lose_count' => int 0
      'online' => boolean false
      'exclude_pk_count_down' => int 0
      'exp' => int 29798
      'rank' => int 11
  2 => 
    array (size=12)
      'nickname' => string '吃飯了' (length=9)
      'alliance_name' => string 'ere' (length=3)
      'lv' => int 100
      'power' => int 12542
      'victory_rate' => float 0.88888888888889
      'total_pk' => int 27
      'win_count' => int 24
      'lose_count' => int 3
      'online' => boolean false
      'exclude_pk_count_down' => int 0
      'exp' => int 223644
      'rank' => int 12
  3 => 
    array (size=12)
      'nickname' => string '更新' (length=6)
      'alliance_name' => string '' (length=0)
      'lv' => int 50
      'power' => int 82133
      'victory_rate' => float 0
      'total_pk' => int 0
      'win_count' => int 0
      'lose_count' => int 0
      'online' => boolean false
      'exclude_pk_count_down' => int 0
      'exp' => int 110376
      'rank' => int 13
  4 => 
    array (size=12)
      'nickname' => string 'd' (length=1)
      'alliance_name' => string '' (length=0)
      'lv' => int 50
      'power' => int 9421
      'victory_rate' => float 0
      'total_pk' => int 0
      'win_count' => int 0
      'lose_count' => int 0
      'online' => boolean false
      'exclude_pk_count_down' => int 0
      'exp' => int 214148
      'rank' => int 14
  5 => 
    array (size=12)
      'nickname' => string 'QQ26號' (length=7)
      'alliance_name' => string '' (length=0)
      'lv' => int 22
      'power' => int 84317
      'victory_rate' => float 0
      'total_pk' => int 0
      'win_count' => int 0
      'lose_count' => int 0
      'online' => boolean false
      'exclude_pk_count_down' => int 0
      'exp' => int 22885
      'rank' => int 16

```