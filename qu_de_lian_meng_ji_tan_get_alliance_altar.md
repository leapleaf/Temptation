# 取得聯盟祭壇 get_alliance_altar

API編碼:2.1.0

> 


更新日期:2016/04/29

> 

SVN版本:15427.

> 

發布版本:2.0.0
### 1.路徑:alliance/get_alliance_altar

### 2. 說明

取得聯盟祭壇資訊

### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
|alliance_name|聯盟名稱|string|12|--|


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |版本|
| -- | -- | -- | -- | -- |--|
| err_code | 回傳參數碼 | string |  |--|
| err_desc | 回傳參數碼說明 | string | -- |--|
|total_altar_lv|目前祭壇科技等級|int|--|2.0.1|
| picture_id|圖片id|int|--|2.0.1|


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|602|不屬於任何聯盟|

### 6.回傳格式範例

*

```
array (size=9)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'alliance_tech_id' => int 102700
  'remaining_time' => int 0
  'alliance_score' => int 1560
  'personal_score' => int 1560
  'donate_cdtime' => int 0
  'can_donate_item' => 
    array (size=7)
      'item_id1' => int 100014
      'item_id1_can_donate' => boolean true
      'quantity1' => int 10
      'item_id2' => int 100014
      'quantity2' => int 15
      'item_id2_can_donate' => boolean false
      'goldleaf' => int 0
  'character' => 
    array (size=3)
      'in_stock1' => int 979
      'in_stock2' => int 979
      'goldleaf' => int 28
  
升級中
array (size=3)
  'err_code' => string '622' (length=3)
  'err_desc' => string '此科技正在升級，無法捐獻' (length=36)
  'remaining_time' => int 29
```
