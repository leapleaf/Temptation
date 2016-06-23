# revive_by_goldleaf_in_boss



API編碼:2.2.6

更新日期:

SVN版本:

發布版本:2.0.8
### 1.路徑:fight/revive_by_goldleaf_in_boss

### 2. 說明


### 3. 輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |版本
| -- | -- | -- | -- | -- |--|
|storeitem_id|商店道具ID|int|--|--|--|
|pet_no|部隊號碼|int|--|第幾個部隊(pet)|--|
|boss_activity_id|boss_activity_id|int|--|--|--|



### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |版本|
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |--|
| err_desc | 回傳參數碼說明 | string | -- |




### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|910|版本已過期，需更新APP資料|
|227|部隊血量不為0,無法購買|
|224|boss戰時間結束|
|123|You don't joined this activity|
|401|can not find item in store|
|403|insufficient goldleaf|
|917|unknown currency type|





### 6.回傳格式範例
```
array (size=12)
  'err_code' => string '000' (length=3)
  'err_desc' => string '' (length=0)
  'valid' => bool true 
  'goldleaf' => int 234000
  'total_goldleaf' => int 0

      ```

```


