# 此處處理聯盟相關API
*表示未完成 

```
### 聯盟人數限制50開始,資料庫要有現在最大人數 修改join_alliance

V *search_character_without_allince_by_name character用nickname模糊  (問清楚再做)同下 
  併入search_character_without_allince
V search_character_without_alliance多吐duty(職能)、語系、取幾名(int) 0給50
v 聯盟名稱改為限制12(最大11)
v quit_alliance:err_code 620 聯盟解散失敗
V sendAllianceInvitation 604:刪你 606:無法寄信給自己
V create_alliance 缺flag_id[靜態表] 602..說明刪除
V get_alliance_list +吐flag
V promote、demote、transit加暱稱
V+ search_alliance_default取幾名(int) 0給50 其他同search_alliance
V get_member_list 輸入多一筆數目 多吐duty、lv 0吐全部並指兔有上線的 power

V*alliance_power_rank 輸入 筆數(int) 0給50 吐名稱 盟主 戰力
V*get_alliance_info 刪除錯誤代碼、權限取消並多吐最大成員數

*character_id client不用帶

V*++改名稱、旗幟加上花金幣



Vsend_msg_to_all_member要注意type '資料庫' type=8,subtype=2




資料庫
---
alliance 新增 flag 
alliance_member新增 join_time (UTC+0)
alliance_log 增加name type
allaiance 新增max_member int 長度4


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
            
            
            
               while (sizeof($ninalli) > $output_num) {
        array_pop($ninalli);
    }
            ```