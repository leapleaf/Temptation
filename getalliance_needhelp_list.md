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
array (size=4)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'collect_gem_queue' => 
    array (size=1)
      0 => 
        array (size=2)
          'nickname' => string 'Rocky' (length=5)
          'queue_id' => int 124
  'compose_queued_list' => 
    array (size=0)
      empty

```
