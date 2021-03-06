# 聯盟科技捐獻研發 alliance_tech_research

API編碼:2.1.0

> 


更新日期:2016/04/29

> 

SVN版本:15427.

> 

發布版本:2.0.0

關聯資料庫:

C:create;R:read;U:update;D:delete;

|Table Name|行為|備註|
|--|--|--|
|alliance|R|--|
|character|R|--|
|alliance_member|R|--|
|alliance_tech|C,R,U|--|
|alliance_donate_history|C|--|
### 1.路徑:alliance_tech/alliance_tech_research

### 2. 說明

根據角色所在聯盟，可對科技進行捐獻，若捐獻到達可升級時會進入升級狀態，此時無法捐獻，若輸入的tech_id大於現在db同一group者,則建立同一group最低等級的tech_id(可改寫成吐error_code,看client)

目前捐獻依次增加cd 10秒 最大值30秒 超過會開始倒數cd cd完才可再捐
> 


捐獻數量依靜態表規範，一種道具只有一個數目
### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
| alliance_tech_id | 聯盟科技 | int | -- | -- |
| item_id | 道具id | int | -- | -- |

### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |版本|
| -- | -- | -- | -- | -- |--|
| err_code | 回傳參數碼 | string |  |--|
| err_desc | 回傳參數碼說明 | string | -- |--|
|alliance_tech_id|捐獻科技id|int|--|--|
| remaining_time|剩餘升級時間|int|--|--|
|alliance_score|現在聯盟積分|int|--|--|
|personal_score|現在個人積分|int|--|--|
|donate_cdtime|個人捐獻|int|--|--|
|donate_cdtime|個人捐獻cd|int|--|--|
|item_id1|可捐獻道具id|int|--|2.0.1|
|item_id2|可捐獻道具id|int|--|2.0.1|
|goldleaf|可捐獻金葉|int|--|2.0.1|
|character|腳色資訊|array|key|2.0.1|
|in_stock1|腳色所持item_id1數量|int|--|2.0.1|
|in_stock2|腳色所持item_id2數量|int|--|2.0.1|
|goldleaf|腳色金葉|int|--|2.0.1|

### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|602|不屬於任何聯盟|
|601|權限不足|
|623|無此可研發科技|
|622|此科技正在升級，無法捐獻(加吐remaining_time)|
|624|無法捐獻此道具|
|625|捐獻冷卻中|
|630|已達可升級狀態,無須捐獻|
|403|物品資源不夠|

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