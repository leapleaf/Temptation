# 取得聯盟聊天 get_chat





API編碼:2.0.?





更新日期:

> 

SVN版本:

> 

發布版本:2.0.0
### 1.路徑:alliance/get_chat

### 2. 說明
修改聊天,新增公會頻道,帶入alliance_id為公會id即可
### 3. 輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |
| -- | -- | -- | -- | -- |
|channel |聊天頻道|var|--|0=公開;1=公會|
|channelNo|聊天子頻道|var|--|公會id|
|alliance_id|公會ID|var|--|--|
|receive_name|收話者|var|--|--|
|content|聊天內容|var|--|--|

$INP_NAME["channel"]="channel(0=公開,1=公會)";
$INP_PARA["channel"]="0";
$INP_NAME["channelNo"]="channelNo(channelNo)";
$INP_PARA["channelNo"]="1";
$INP_NAME["receive_name"]="receive_name";
$INP_PARA["receive_name"]="";
$INP_NAME["alliance_id"]="alliance_id";
$INP_PARA["alliance_id"]="";
//$INP_NAME["content"]="content(content)";
//$INP_PARA["content"]="Raynor#Hi everybody";
$INP_NAME["last_character_chat_id"]="last_character_chat_id";
$INP_PARA["last_character_chat_id"]="1";
$INP_NAME["lang"]="lang (tw,en,cn,sp)";
$INP_PARA["lang"]="tw";




### 4. 回傳參數說明
| 參數 | 意義 | 型別 | 說明 |
| -- | -- | -- | -- | -- |
| err_code | 回傳參數碼 | string |--|
| err_desc | 回傳參數碼說明 | string | -- |




### 5. 錯誤代碼說明
|錯誤代碼|意義|
|--|--|
|604|已有所屬聯盟|
|614|此邀請已失效|

### 6.回傳格式範例

```array (size=2)

  'err_code' => string '000' (length=3)
  
  'err_desc' => string 'success' (length=7)```

