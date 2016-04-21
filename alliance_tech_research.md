# 聯盟科技捐獻研發 alliance_tech_research

API編碼:2.1.0

> 


更新日期:

> 

SVN版本:

> 

發布版本:2.0.0
### 1.路徑:alliance_tech/alliance_tech_research

### 2. 說明

根據角色所在聯盟，可對科技進行捐獻，若捐獻到達可升級時會進入升級狀態，此時無法捐獻，若輸入的tech_id大於現在db同一group者,則建立同一group最低等級的tech_id(可改寫成吐error_code,看client)
> 


捐獻數量依靜態表規範，一種道具只有一個數目
### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
| alliance_tech_id | 聯盟科技 | string | -- | -- |
| item_id | 道具id | string | 15 | -- |

### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |  |
| err_desc | 回傳參數碼說明 | string | -- |
| remaining_time|剩餘升級時間|int|--|
|alliance_score|現在聯盟積分|int|--|
|personal_score|現在個人積分|int|--|

### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|602|不屬於任何聯盟|
|601|權限不足|
|623|無此可研發科技|
|622|此科技正在升級，無法捐獻(加吐remaining_time)|
|403|物品資源不夠|

### 6.回傳格式範例

*

```
array (size=4)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'remaining_time' => int 0
  'score' => int 4400
```