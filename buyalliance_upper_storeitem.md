
#購買聯盟上游道具 buy_alliance_upper_storeitem


API編碼:2.2.2

> 


更新日期:2016/05/03

> 

SVN版本:15458

> 

發布版本:2.0.0
### 1.路徑:alliance_store/buy_alliance_upper_storeitem

### 2. 說明
購買聯盟上游道具,會先判斷有無聯盟,再判斷有無權限,計算積分足不足夠,成功則將道具加入聯盟商店



### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
| character_id | 腳色id | int | -- | 由token取得 |
| storeitem_id | 道具id | int | 6 | -- |
|num|購買道具數|int|

### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |  |
| err_desc | 回傳參數碼說明 | string | -- |


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|910|版本已過期，需更新APP資料|
|602|不屬於任何聯盟|
|601|權限不足|
|617|無此商品目錄|
|607|聯盟積分不足|





### 6.回傳格式範例

*

```
array (size=4)
  'err_code' => string '000' (length=3)
  'err_desc' => string 'success' (length=7)
  

```

