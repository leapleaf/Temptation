# 此處處理聯盟相關API
*表示未完成

```
聯盟人數限制從50開始

V search_character_without_alliance多吐duty(職能)、語系、取幾名(int) 0給50
search_character_alliance character用nickname模糊 取消type
聯盟名稱改為限制12
search_alliance_default取幾名(int) 0給50 其他同search_alliance
quit_alliance:err_code 60X 聯盟解散失敗
604:刪你
606:無法寄信給自己
promote、demote、transit加暱稱
alliance_power_rank 輸入 筆數(int) 0給50 吐名稱 盟主 戰力
get_alliance_list +吐flag
get_member_list 輸入多一筆數目 多吐duty、lv 0吐全部並指兔有上線的
get_alliance_info 刪除錯誤代碼、權限取消並多吐最大成員數


*character_id client不用帶
create_alliance 缺flag_id[靜態表]
++改名稱、旗幟加上花金幣
602..說明刪除


send_msg_to_all_member要注意type '資料庫'


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