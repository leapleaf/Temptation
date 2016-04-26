# 取得聯盟科技 get_alliance_tech




API編碼:2.0.?

> 


更新日期:

> 

SVN版本:

> 

發布版本:2.0.0
### 1.路徑:alliance_tech/get_alliance_tech

### 2. 說明

取得聯盟科技資訊,取得的是可研發科技清單
### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
|character_id|聯盟名稱|int|12|取token,client不須輸入|
|alliance_tech_id|聯盟科技id|int|請代入資料庫有的id|


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |  |
| err_desc | 回傳參數碼說明 | string | -- |
|exp|科技研究值|int|目前|
|threshold|科技升級所需|int|--|
|benefit|現在科技效果|int|Value1|
|next_benefit|下一科技效果|int|若無則吐0|
|remiaining_time|升級剩餘時間|int|低於0吐0|


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|601|權限不足|
|602|不屬於任何聯盟|

### 6.回傳格式範例

```
array (size=7)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'exp' => int 0
  'threshold' => int 0
  'benefit' => int 0
  'next_benefit' => int 0
  'remaining_time' => int 0
```

