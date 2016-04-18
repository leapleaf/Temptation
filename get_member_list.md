# 取得聯盟成員資訊 get_member_list


API編碼:2.0.5

> 



更新日期:2016/04/18

> 

SVN版本:Committed revision 15054.


> 

發布版本:2.0.0
### 1.路徑:alliance/get_member_list

### 2. 說明

取得聯盟成員清單,會依據token或character_id取得所有聯盟成員的
暱稱、位階、角色模組、經驗值、是否在線、戰力,
輸入限制:0為取預設50,顯示所有成員,其他則依限制筆數顯示(依職位排序)

err_code 602為自己未加入聯盟中,故看不到自己的聯盟
### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
|alliance_name|聯盟名稱|string|12|未輸入則取token|
|limit|限制筆數|

### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |  |
| err_desc | 回傳參數碼說明 | string | -- |
|members|聯盟成員|array|--|
|alliance_name|聯盟名稱|string|--|
|nickname|成員暱稱|string|--|
|position|職位|string|--|
|model|角色模組|string|--|
|duty|職能|stiring|--|
|lv|等級|string|--|
|is_online|是否在線|bool|--|
|power|成員戰力|string|--|


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|602|不屬於任何聯盟|
|603|找不到此聯盟|

### 6.回傳格式範例

```array (size=3)

  'err_code' => string '000' (length=3)
  
  'err_desc' => string 'success' (length=7)
  
  'members' => 
  
    array (size=2)
      0 => 
        array (size=6)
          'nickname' => string 'wade' (length=4)
          'position' => string '1' (length=1)
          'model' => string '1' (length=1)
          'exp' => string '30622' (length=5)
          'is_online' => boolean true
          'power' => string '67192' (length=5)
      1 => 
        array (size=6)
          'nickname' => string 'Rocky' (length=5)
          'position' => string '6' (length=1)
          'model' => string '1' (length=1)
          'exp' => string '-1' (length=2)
          'is_online' => boolean false
          'power' => string '10660' (length=5)```