# 選取採礦 choose_mining_troops




API編碼:3.0.0

> 


更新日期:

> 

SVN版本:

> 

發布版本:2.2.0
### 1.路徑:mining/choose_mining_troops

### 2. 說明
選取採礦地點,分三種,3為最高級礦區,會依上線時間開放最大採礦部隊數,初始一律為2,5分鐘變3,10分鐘變4,最大為8,斷線5分鐘後會重算

### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |版本|
| -- | -- | -- | -- | -- | -- |
|mining_sites|採礦地點|int|--|值為1,2,3|--|



### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |版本|
| -- | -- | -- | -- | -- |--|
| err_code | 回傳參數碼 | string |  |--|
| err_desc | 回傳參數碼說明 | string | -- |--|
|remaining_time|最後一支部隊的採集時間|int|--|--|




### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|905|輸入資料格式錯誤|
|140|the character does not exist|
|271|mining troop num is over|
|272|同一礦區不得超過4隊|

### 6.回傳格式範例

```
array (size=4)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'remaining_time' => int 0
 
```

