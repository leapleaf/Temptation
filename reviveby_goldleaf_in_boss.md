# revive_by_goldleaf_in_boss



API編碼:2.2.7

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
|184|boss fight is disable|
|223|目前boss戰非此id|
|123|You don't joined this activity|
|224|boss戰時間結束|
|226|部隊血量不為0,無法復活|
|407|gold leaf is not enough|





### 6.回傳格式範例
```
array (size=12)
  'err_code' => string '000' (length=3)
  'err_desc' => string '' (length=0)

      ```

```


