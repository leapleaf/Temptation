#取得聯盟幫助清單 get_alliance_needhelp_list


API編碼:2.3.0

> 


更新日期:2016/05/05 2016/05/06

> 

SVN版本:15536,15556

> 

發布版本:2.0.0
### 1.路徑:alliance_help/get_alliance_needhelp_list

### 2. 說明

取得現在聯盟成員需要幫助的清單
會判斷有無幫助過 若以幫助過不會吐該筆資料
會吐client的自己需要幫助項目加上其他聯盟成員

不用帶任何參數 我會用token檢查你有沒有聯盟 有的畫吐現在正在製作寶石跟裝備的給你

### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
| character_id | 腳色id | int | -- | 由token取得 |

### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |  |
| err_desc | 回傳參數碼說明 | string | -- |
|alliance_need_helip_list|裝備陣列|array|key|
|nickname|玩家暱稱|string|--|
|model|腳色模型|int|--|
|limit|幫助限制|int|--|
|type|幫助種類|int|--|
|recvie_times|已幫助次數|int|--|
|item_id|道具id|int|--|
|gem_id|寶石id|int|--|


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|602|不屬於任何聯盟|


### 6.回傳格式範例

*

```
array (size=3)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'alliance_need_helip_list' => 
    array (size=7)
      0 => 
        array (size=7)
          'nickname' => string 'wade' (length=4)
          'queue_id' => int 144
          'model' => int 1
          'limit' => int 7
          'item_id' => int 200002
          'type' => int 1
          'recvie_times' => int 3
      1 => 
        array (size=7)
          'nickname' => string 'wade' (length=4)
          'queue_id' => int 145
          'model' => int 1
          'limit' => int 7
          'item_id' => int 200002
          'type' => int 1
          'recvie_times' => int 1
      2 => 
        array (size=7)
          'nickname' => string 'wade' (length=4)
          'queue_id' => int 146
          'model' => int 1
          'limit' => int 7
          'item_id' => int 200002
          'type' => int 1
          'recvie_times' => int 0
      3 => 
        array (size=7)
          'nickname' => string 'Rocky' (length=5)
          'queue_id' => int 147
          'model' => int 1
          'limit' => int 5
          'item_id' => int 200002
          'type' => int 1
          'recvie_times' => int 0
      4 => 
        array (size=7)
          'nickname' => string 'Rocky' (length=5)
          'queue_id' => int 131
          'model' => int 1
          'limit' => int 5
          'gem_id' => int 100001
          'type' => int 2
          'recvie_times' => int 0
      5 => 
        array (size=7)
          'nickname' => string 'Rocky' (length=5)
          'queue_id' => int 287
          'model' => int 1
          'limit' => int 5
          'gem_id' => int 100001
          'type' => int 2
          'recvie_times' => int 3
      6 => 
        array (size=7)
          'nickname' => string 'Rocky' (length=5)
          'queue_id' => int 288
          'model' => int 1
          'limit' => int 5
          'gem_id' => int 100001
          'type' => int 2
          'recvie_times' => int 2

```
