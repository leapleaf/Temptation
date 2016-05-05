# 聯盟戰力排名 alliance_power_rank




API編碼:2.4.0

```
    if (!$permission) {//暫時寫入mem 等規格開後刪掉
        $Leaderpermision = [10001 => 1, 10002 => 0, 10003 => 0, 10004 => 0, 10005 => 0, 10006 => 0, 10007 => 0];
        addAlliancePermisiontoMem('LeaderChange', $Leaderpermision);
    }

```



更新日期:

> 

SVN版本:

> 

發布版本:2.0.0
### 1.路徑:rank/alliance_power_rank

### 2. 說明

轉讓盟主,轉讓者會變最低職位
### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
| limit | 筆數 | string | 11 | 未帶入則為50筆 |

### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |  |
| err_desc | 回傳參數碼說明 | string | -- |
|ranks|排名|array|key|



### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|601|無此權限|
|605|該玩家不屬於此聯盟|
|power|聯盟戰力|int|--|
|alliance_name|聯盟名稱|string|--|
|alliance_short_name|聯盟短名稱|string|--|
|leader|盟主|string|--|

### 6.回傳格式範例

*```
array (size=10)
  0 => 
    array (size=4)
      'power' => int 548818
      'alliance_name' => string '123' (length=3)
      'alliance_short_name' => string 'A' (length=1)
      'leader' => string 'wade' (length=4)

```



