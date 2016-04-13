# 聯盟地圖 get_alliance_list



API編碼:2.0.4

> 

更新日期:2016/4/13

> 

SVN版本:15004

> 

發布版本:2.0.0
### 1.路徑:alliance/get_alliance_list

### 2. 說明
取得所有已建立的聯盟,關聯資料庫:world_map,alliance
### 3. 輸入參數說明
無須輸入

### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |--|
| err_desc | 回傳參數碼說明 | string | -- |
|alliance_list|聯盟清單|array|--|
|leader|盟主|string|--|
|alliance_name|聯盟名稱|string|--|


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|


### 6.回傳格式範例

array (size=12
> 


  0 => 
> 


    array (size=2)
> 


      'leader' => string 'win' (length=3)
> 


      'alliance_name' => string '988' (length=3)
> 


  1 => 
> 


    array (size=2)
> 


      'leader' => string 'pimp' (length=4)
> 


      'alliance_name' => string '977' (length=3)

