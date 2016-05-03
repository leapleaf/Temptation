# 取得聯盟商店清單 get_alliance_storeitem_list

API編碼:2.2.0

> 


更新日期:2016/05/03

> 

SVN版本:15458

> 

發布版本:2.0.0
### 1.路徑:alliance_store/get_alliance_storeitem_list

### 2. 說明

取得現在聯盟的商店清單


### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
| character_id | 腳色id | int | -- | 由token取得 |
| language | 語系 | string | 2 | -- |

### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |  |
| err_desc | 回傳參數碼說明 | string | -- |
|items|道具陣列|array|key|
| item_id|道具id|int|--|
|name|道具名稱|string|依語系調整|
|description|道具說明|string|依語系調整|
|type|型別|int|1.素材 2.道具 3.特殊 4.熱賣|
|price|兌換價格|int|--|
|num|剩餘數量|int|--|
|icon_id|--|int|--|
|member_point|成員積分|int|查詢者本人|
|alliance_point|聯盟積分|int|--|

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
