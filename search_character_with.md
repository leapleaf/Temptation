# 搜尋無聯盟玩家 search_character_without_alliance




API編碼:2.0.8





更新日期:2016/04/25

> 

SVN版本:15357..

>  

發布版本:2.0.0
### 1.路徑:alliance/search_character_without_alliance

### 2. 說明

搜尋無聯盟玩家,keyword可以不輸入,預設亂數排序50名,limit給0為預設
### 3. 輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |
| -- | -- | -- | -- |--| -- |
|keyword|搜尋字串|string|12|模糊搜尋暱稱|
|limit|筆數|int|--|給client的筆數|


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |  |
| err_desc | 回傳參數碼說明 | string | -- |
|characters|角色|array|純key|
|nickname|暱稱|string|--|
|lv|等級|string|--|
|model|角色模組|string|--|
|duty|職能|string|--|
|power|戰力|string|--|
|lang|語系|string|--|




### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|

### 6.回傳格式範例

```
array (size=3)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'characters' => 
    array (size=1)
      0 => 
        array (size=6)
          'nickname' => string 'QQ18號' (length=7)
          'lv' => string '1' (length=1)
          'model' => string '0' (length=1)
          'duty' => string '3' (length=1)
          'power' => string '0' (length=1)
          'lang' => string 'tw' (length=2)
```