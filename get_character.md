# 取得角色資訊 get_character



API編碼:2.6.0





更新日期:

> 

SVN版本:

> 

發布版本:2.0.0
### 1.路徑:character/get_character

### 2. 說明
新增戰力與聯盟
### 3. 新增輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |
| -- | -- | -- | -- | -- |





### 4. 新增回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| power | 戰力 | int |--|
| alliance_name | 聯盟名稱 | string | -- |
| alliance_short_name | 聯盟名稱 | string | -- |
|position|職位|int|--|




### 5. 新增錯誤代碼說明
|錯誤代碼|意義|
|--|--|


### 6.回傳格式範例

```
array (size=53)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  'nickname' => string 'wade' (length=4)
  'model' => int 1
  'duty' => int 1
  'exp' => int 30622
  'lv' => int 24
  'power' => int 67462
  'alliance_name' => string '123' (length=3)
  'alliance_short_name' => string 'A' (length=1)...
  ```

