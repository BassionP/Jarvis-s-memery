User's Hermes skills directory is symlinked to ~/Jarvis/skills/ (private GitHub repo BassionP/Jarvis---Bassion-Paul). PAT remote for push + gh CLI authed as BassionP.
§
SLS(阿里日志)用于RTC监控(bad-room-user+kick_hack_rtc,按uid/roomId/svip分组)。方言受限:无count(distinct) over(),cross join不稳,多查询告警最稳。另有live_server_event_loghub事件表(uid/type/ds分区yyyymmdd)JOIN用户全量表tod_hapi_user_info_mongo(uid联表键,ext为JSON含thirdEmail/bindFacebook/bindApple/bindGoogle,json_extract(ext,'$.key')取值)。
§
WARP=2a09:bac0::/29+104.28.0.0/16+162.159.192.0/22(官网不发布池,以RIPEstat/AS13335为准)。WARP用户47.5%黑产不能一刀切:选Bengali/India/Pakistan=真人,Other/Indonesia/Vietnam=黑产。澳门84.252.*100%黑产。IP段列解析先剥.*。2a02:6ea0*=Datacamp机房。
§
Race Online AS63969拉整ASN。印尼编号名多开(Warsa 05/Nomor 1/Stella 1等,110.138.53.*/103.133.24.*)=印尼羊毛党,黑产与薅羊毛边界,非黑产。
§
孟加拉黑产买断ISP段:103.54.37.*、103.155.118.*(均Race Online,100%)、160.187.109.*(BDCOLO,97.9%)；正规ISP段多已被买断污染。
§
送礼/活动数据须按周同期对齐
§
Hapi宝箱风控：SVIP充值门槛600万→sv1/1800万→sv2/6000万→sv3。svip2+豁免(充值成本认了)，IP段黑名单只拦svip0，工具号指纹=累充恰好到阈值(尤600万卡sv1)。金额=次数×2.3万(单次中位,相关0.998,两参数冗余)，金额400万=175次(周三~2.5倍)。数据坑:次数/金额文件SVIP字段不一致，金额文件为最新权威。
§
Hapi语音审核：日均200h阿语音频、准实时，选满血large-v3(非turbo)自建Whisper+阿里云GPU；阿语方言是ASR难点。
§
BytePlus国际控制台console.byteplus.com被Akamai按IP拦机房/VPN(403 TCP_DENIED),需住宅IP;www.byteplus.com与console.volcengine.com不受影响。
§
钉钉文档/表格经config.yaml的4个MCP访问(勿用浏览器,有OAuth登录墙):dingtalk-docs仅adoc;dingtalk-able仅AI表格able;dingtalk-sheet读写普通表格axls(get_all_sheets/get_range/set_cell_range)。用户发[DeviceInfo]设备上报数据让填表/校验,布尔统一大写TRUE/FALSE。
§
Hapi非SVIP送礼占比~42%。货币:钻石=充值,筹码(类型13)=金币1:1。送礼LuckyGift最大消耗76-92万/天,资金主源=钻石换金币(收礼钻石3.3:1换币,库存非增发~30%)+升级活动(升到等级白送纯增发~20%);宝箱/roomsupport/family/magicball/event=消费返利(花→按比例反),红包=用户间转移。宝箱风控对送礼影响仅0.3-0.5%。白桢国(风控)负责宝箱/拉新/僵尸。事件分析xlsx正=流入负=流出。
§
黑产标注语义：用户标红=确认黑产(正样本)，未标红≠正常(混着正常+不确定用户)。禁止用红字率(红/总数)当黑产概率、禁止反向推测「低红字率=干净」，只用lift富集度=(黑产中占比)/(全体占比)。IP/邀请者拉黑用确认黑产计数，红字率是下界。
§
IP段拉黑输出a.b.c格式(不带.*)竖写每行一个可逗号隔开;IPv6不写(WARP归薅羊毛)。
§
Python:pandas分析须用hermes venv python(~/.hermes/hermes-agent/venv/bin/python3),系统python3=3.9.6的pandas坏。
§
黑产vs薅羊毛(用户权威):黑产=工具号=只送礼不收礼+批量≥10同特征+无社交+低充≤600万→封禁;薅羊毛=有收有送+≤50+有社交+低充≤600万→限制。静态字段(数字名/区号/选国/零充)只是候选,区分靠行为信号(送礼收礼/批量/社交)在事件流水表。数字名30x最稳,区号/选国/设备每日漂移。