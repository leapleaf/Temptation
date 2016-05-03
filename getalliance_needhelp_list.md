#取得聯盟幫助清單 get_alliance_needhelp_list


API編碼:2.3.0

> 


更新日期:2016/05/03

> 

SVN版本:

> 

發布版本:2.0.0
### 1.路徑:alliance_help/get_alliance_needhelp_list

### 2. 說明

取得現在聯盟成員需要幫助的清單


### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
| character_id | 腳色id | int | -- | 由token取得 |

### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |  |
| err_desc | 回傳參數碼說明 | string | -- |
|compose_queued_list|裝備陣列|array|key|
| collect_gem_queue|寶石陣列|array|key|
|nickname|玩家暱稱|string|--|
|queue_id|製作序列|string|依語系調整|


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|910|版本已過期，需更新APP資料|
|602|不屬於任何聯盟|


### 6.回傳格式範例

*

```
array (size=5)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'items' => 
    array (size=1)
      0 => &
        array (size=7)
          'item_id' => int 100001
          'name' => string 'Jasper' (length=6)
          'description' => string 'Troops Summoning Item.' (length=22)
          'type' => int 1
          'price' => int 100
          'num' => int 2
          'icon_id' => int 501001
  'member_point' => int 4930
  'alliance_point' => int 280

```
