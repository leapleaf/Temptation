# +盟主轉讓 alliance_leader_transit



API編碼:2.3.2

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
### 1.路徑:alliance/alliance_leader_transit

### 2. 說明

轉讓盟主,轉讓者會變最低職位
### 3. 輸入參數說明


| 參數 | 意義 | 型別 | 長度限制 | 說明 |
| -- | -- | -- | -- | -- | -- |
| nickname | 繼位者 | string | 11 | 暱稱 |

### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |  |
| err_desc | 回傳參數碼說明 | string | -- |


### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|601|無此權限|
|605|該玩家不屬於此聯盟|

### 6.回傳格式範例

*array (size=2)
> 


  'err_code' => string '000' (length=3)
> 


  'err_desc' => string 'success' (length=7)*



