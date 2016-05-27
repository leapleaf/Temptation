#更新競技場名單 fight/refresh_fightable_list





API編碼:2.9.3

> 


更新日期:

> 

SVN版本:

> 

發布版本:2.0.2
### 1.路徑:fight/refresh_fightable_list

### 2. 說明
更新競技場名單,會花費金葉,call這支api後去call list才會真的更新
### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |版本|
| -- | -- | -- | -- | -- |--|
| err_code | 回傳參數碼 | string |  |--|
| err_desc | 回傳參數碼說明 | string | -- |--|



### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|222|競技場清單無須更新|
|407|貨幣不夠|



### 6.回傳格式範例

```
array (size=10)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
 
```



