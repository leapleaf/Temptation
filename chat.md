# 新增聯盟聊天 chat



```
[2016/3/16 上午 11:15:43] Magus: alliance_chat 我是要記錄在character_chat table還是新開一張?
[2016/3/16 上午 11:16:41] Magus: 記錄在character_table需要多個欄位判斷
[2016/3/16 上午 11:17:10] Magus: 原本的api有getChatLastID,也可能會衝突
[2016/3/16 上午 11:17:17] PeterPan: character_chat channel =1 公會聊天 channelNo 記alliance_id
[2016/3/16 上午 11:17:43] Magus: 好
[2016/3/16 上午 11:17:45] PeterPan: db不用開新欄位
[2016/3/16 上午 11:17:57] Magus: 那getChatLastID?
[2016/3/16 上午 11:18:07] Magus: processChatLastID
[2016/3/16 上午 11:18:44] Magus: 我是用alliance_id去撈最後的嬤?
[2016/3/16 上午 11:19:52] PeterPan: get_chat 帶channel channelNo last_character_chat_id
[2016/3/16 上午 11:19:56] PeterPan: 原本就有的
[2016/3/16 上午 11:20:25] PeterPan: getChatFromMemcache 需要定義
[2016/3/16 上午 11:20:26] PeterPan:     if($channel == 0){ 
        $key = "PublicChat".$channelNo;
    }
//unfinish    
//    else if($channel == 1)
//    {
//        $key = "ChurchChat".$receive_id;
//    }
//    else if($channel == 2)
//    {
//       $key = "PrivateChat".$receive_id;
//    }
[2016/3/16 上午 11:20:40] PeterPan: key值
[2016/3/16 上午 11:21:55] PeterPan: 你測測看... 看有沒有問題. 如果順利的話,應該不用改其他的code
[2016/3/16 上午 11:22:03] Magus: 那不需要多一隻last_alliance_chat_id嗎
[2016/3/16 上午 11:22:10] PeterPan: 不用
[2016/3/16 上午 11:22:13] Magus: 好
[2016/3/16 上午 11:22:39] PeterPan: get_chat,chat 帶入參數 就決定是哪種模式 和頻道
[2016/3/16 上午 11:23:34] Magus: 那我memchaed還是要加一個AllianceChat+allianceid
[2016/3/16 上午 11:23:51] Magus: 目前他寫法只有Public+No
[2016/3/16 上午 11:24:14] Magus: 這個我會寫在chat.php
[2016/3/16 上午 11:24:38] Magus: 上面說的是key
[2016/3/16 上午 11:25:27] PeterPan: addChatIntoMemcache 和 getChatFromMemcache 有關if($channel == 1) 你決定key值名稱
[2016/3/16 上午 11:25:43] Magus: ok
[2016/3/16 下午 02:50:12] Magus: 修改get_chat.php  多回傳 model,duty
沒有在線上model,duty都0
[2016/3/16 下午 02:50:36] Magus: model 跟duty是character rable裡的嗎?
[2016/3/16 下午 02:50:41] Magus: table
```

```
不改key替換的方式?
            if (count($chatArray) > $cacheChatNum) {
                //remove first element
                //M1 will change its key value
                //array_shift($chatArray);
                //M2 http://stackoverflow.com/questions/18577087/how-to-remove-the-first-element-of-array-without-changing-its-key-value
                reset($chatArray);
                $first_key = key($chatArray);
                //echo $first_key;
                unset($chatArray[$first_key]);
            }
```






API編碼:2.0.?





更新日期:

> 

SVN版本:

> 

發布版本:2.0.0
### 1.路徑:alliance/chat

### 2. 說明
修改聊天,新增公會頻道,帶入alliance_id為公會id即可
### 3. 輸入參數說明
| 參數 | 意義 | 型別 |長度限制| 說明 |
| -- | -- | -- | -- | -- |
|channel |聊天頻道|var|--|0=公開;1=公會|
|channelNo|聊天子頻道|var|--|公會id|
|alliance_id|公會ID|var|--|--|
|receive_name|收話者|var|--|0為公頻|
|content|聊天內容|var|--|--|




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

