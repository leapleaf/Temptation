# 聯盟地圖 get_alliance_list



API編碼:2.0.4

> 

更新日期:2016/4/13,2016/4/26

> 

SVN版本:15004,15350.

> 

發布版本:2.0.0
### 1.路徑:alliance/get_alliance_list

### 2. 說明
取得所有已建立的聯盟,關聯資料庫:world_map,alliance
### 3. 輸入參數說明
| 參數 | 意義 | 型別|長度限制 | 說明 |
| -- | -- | -- | -- | -- |--|
|limit|限制筆數|int|--|帶0為50|


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |--|
| err_desc | 回傳參數碼說明 | string | -- |
|alliance_list|聯盟清單|array|--|
|world_map_id|世界地圖id|string|--|
|leader|盟主|string|--|
|alliance_name|聯盟名稱|string|--|
|flag|聯盟旗幟|string|--|
|total_power|戰力|string|--|


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|


### 6.回傳格式範例
```
array (size=3)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'alliance_list' => 
    array (size=15)
      0 => 
        array (size=4)
          'leader' => string '123' (length=3)
          'alliance_name' => string 'goddamn' (length=7)
          'flag' => string '1111111' (length=7)
          'total_power' => string '0' (length=1)
      1 => 
        array (size=4)
          'leader' => string 'E566A8604B794AF49735' (length=20)
          'alliance_name' => string 'goddamn8888' (length=11)
          'flag' => string '1111111' (length=7)
          'total_power' => string '0' (length=1)
      2 => 
        array (size=4)
          'leader' => string 'Fff' (length=3)
          'alliance_name' => string '333' (length=3)
          'flag' => string '1' (length=1)
          'total_power' => string '0' (length=1)

```