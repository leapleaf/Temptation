#比牌 fight/card_versus





API編碼:2.9.0

> 


更新日期:

> 

SVN版本:

> 

發布版本:2.0.2
### 1.路徑:fight/card_versus

### 2. 說明

取得聯盟科技資訊,取得的是可研發科技清單,會執行達到升級時的tech_id升級
### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
|nickname|暱稱|int|--|被挑戰者|


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |版本|
| -- | -- | -- | -- | -- |--|
| err_code | 回傳參數碼 | string |  |--|
| err_desc | 回傳參數碼說明 | string | -- |--|
|attacker_score|挑戰者分數|int||--|
|defender_score|防禦者分數|int|--|--|
|win|挑戰結果|boolean||--|


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|196|競技場尚未開啟|
|113|action point is not enough|


### 6.回傳格式範例

```
array("err_code" => '000',
            "err_desc" => 'success',
            "attacker_score" => $Me->attacker_score,
            "defender_score" => $Enemy->attacker_score,
            "win" => (boolean)$win
        )
```

