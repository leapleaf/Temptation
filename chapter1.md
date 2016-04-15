# 此處處理聯盟相關API
*表示未完成 

```
聯盟人數限制從50開始



!!!???search_alliance_character character用nickname模糊 取消type (問清楚再做)
V search_character_without_alliance多吐duty(職能)、語系、取幾名(int) 0給50
v 聯盟名稱改為限制12(最大11)
v quit_alliance:err_code 620 聯盟解散失敗
V sendAllianceInvitation 604:刪你 606:無法寄信給自己
V create_alliance 缺flag_id[靜態表] 602..說明刪除
V get_alliance_list +吐flag
promote、demote、transit加暱稱
search_alliance_default取幾名(int) 0給50 其他同search_alliance
get_member_list 輸入多一筆數目 多吐duty、lv 0吐全部並指兔有上線的

alliance_power_rank 輸入 筆數(int) 0給50 吐名稱 盟主 戰力
get_alliance_info 刪除錯誤代碼、權限取消並多吐最大成員數

*character_id client不用帶

++改名稱、旗幟加上花金幣



send_msg_to_all_member要注意type '資料庫'




資料庫
---
alliance 新增 flag 
alliance_member新增 join_time (UTC+0)



---
++寫一之聯盟成員清單吐status=1的卡片,用token取



```
```
       $inalli = ORM::for_table('alliance_member')->select('character_id')->find_array();
    //var_dump($inalli);
    //$test = merge2DArray($inalli);
    //var_dump($test);
    foreach ($inalli as &$arr) {
        foreach ($arr as &$v) {
            $arr = $v;
        }
    }
    //shuffle($inalli['characters']);
    //var_dump($inalli);

    $ninalli = ORM::for_table('character')->select('nickname')
                            //->right_outer_join('character', 'world_map.character_id = character.id')

            ->right_outer_join("account",'account.id = character.account_id')            
            ->select('lv')
            ->select("model")
            ->select('duty')
            ->where_not_in('character.id', $inalli)
            ->select('account.lang')
            ->find_array();
            ```