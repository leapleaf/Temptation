# get_chat



API編碼:2.10.0

> 


更新日期:

> 

SVN版本:


發布版本:2.0.2

### 1.路徑:character_chat/get_chat

### 2. 說明
增加回傳參數 chat_info
### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |


### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |版本|
| -- | -- | -- | -- | -- |--|
| err_code | 回傳參數碼 | string |  |--|
| err_desc | 回傳參數碼說明 | string | -- |--|
|chat_content|聊天內容|array|key|--|
|chat_info|聊天資訊|array|key|2.0.2|
|nickname|暱稱|string|--|2.0.2|
|model|外型|int|--|2.0.2|
|duty|職能|int|--|2.0.2|
|alliance_name|聯盟名稱|string|--|2.0.2|
|is_online|是否上線|boolean|--|2.0.2|



### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|



### 6.回傳格式範例

```
array (size=5)
  'err_code' => string '000' (length=3)
  'err_desc' => string '成功' (length=6)
  'last_character_chat_id' => int 9768
  'chat_content' => 
    array (size=36)
      0 => string 'wade#Hi everybody|04:03' (length=23)
      1 => string 'leapleaf#AE00D90BBD46297CEED3創立了聯盟goddamn54，歡迎大家加入。|10:36|2016/05/13' (length=94)
      2 => string 'wade#Hi everybody|10:13' (length=23)
      3 => string 'leapleaf#A7788創立了聯盟刺刺der，歡迎大家加入。|08:20|2016/05/16' 
  'chat_info' => 
    array (size=5)
      0 => 
        array (size=5)
          'nickname' => string 'wade' (length=4)
          'model' => string '1' (length=1)
          'duty' => string '1' (length=1)
          'alliance_name' => string '' (length=0)
          'is_online' => boolean true
      23 => 
        array (size=5)
          'nickname' => string '吃飯了' (length=9)
          'model' => int 0
          'duty' => int 0
          'alliance_name' => string 'ere' (length=3)
          'is_online' => boolean false
      27 => 
        array (size=5)
          'nickname' => string 'yee' (length=3)
          'model' => int 0
          'duty' => int 0
          'alliance_name' => string 'QAQQ' (length=4)
          'is_online' => boolean false
      28 => 
        array (size=5)
          'nickname' => string 'd01' (length=3)
          'model' => int 0
          'duty' => int 0
          'alliance_name' => string 'ere' (length=3)
          'is_online' => boolean false
      30 => 
        array (size=5)
          'nickname' => string 'hithere' (length=7)
          'model' => int 0
          'duty' => int 0
          'alliance_name' => string '' (length=0)
          'is_online' => boolean false
```



