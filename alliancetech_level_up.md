#聯盟科技升級 alliance_tech_level_up


API編碼:2.1.3

> 


更新日期:2016/05/06

> 

SVN版本:15427.

> 

發布版本:2.0.0
### 1.路徑:alliance_tech/alliance_tech_level_up

### 2. 說明

根據角色所在聯盟，可對科技進行捐獻，若捐獻到達可升級時會進入升級狀態，此時無法捐獻
> 


捐獻數量依靜態表規範，一種道具只有一個數目
### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
| alliance_tech_id | 聯盟科技 | int | -- | -- |

### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |  |
| err_desc | 回傳參數碼說明 | string | -- |
| remaining_time|剩餘升級時間|int|--|
|alliance_score|聯盟積分|int|--|
|personal_score|個人積分|int|--|


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|602|不屬於任何聯盟|
|601|權限不足|
|623|無此可研發科技|
|622|此科技正在升級(加吐remaining_time)|


### 6.回傳格式範例

*

```
array (size=6)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'alliance_tech_id' => int '100100' (length=6)
  'remaining_time' => int 0
  'alliance_score' => int 690
  'personal_score' => int 690
  
升級中
array (size=3)
  'err_code' => string '622' (length=3)
  'err_desc' => string '此科技正在升級' (length=36)
  'remaining_time' => int 29
```