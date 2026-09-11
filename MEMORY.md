Skills目录symlink→~/Jarvis/skills/(BassionP/Jarvis---Bassion-Paul);记忆备份仓库BassionP/Jarvis-s-memery(均private)。gh CLI已认证BassionP,PAT可push。
§
SLS(阿里日志)用于RTC监控(bad-room-user+kick_hack_rtc,按uid/roomId/svip分组)。方言受限:无count(distinct)over(),cross join不稳,多查询告警最稳。另有live_server_event_loghub表(uid/type/ds)JOIN全量表tod_hapi_user_info_mongo(uid键,ext为JSON含第三方绑定,json_extract(ext,'$.key')取值)。
§
WARP=2a09:bac0::/29+104.28.0.0/16+162.159.192.0/22(以RIPEstat/AS13335为准)。WARP用户47.5%黑产不能一刀切:选Bengali/India/Pakistan=真人,Other/Indo/Viet=黑产。澳门84.252.*100%黑产。2a02:6ea0*=Datacamp机房。
§
Race Online AS63969拉整ASN。印尼编号名多开(Warsa 05/Nomor 1等,110.138.53.*/103.133.24.*)=印尼羊毛党,非黑产。
§
孟加拉黑产买断ISP段:103.54.37.*、103.155.118.*(Race Online,100%)、160.187.109.*(BDCOLO,97.9%);正规ISP段多被买断污染。
§
送礼/活动数据须按周同期对齐
§
Hapi宝箱风控：SVIP充值门槛600万→sv1/1800万→sv2/6000万→sv3。svip2+豁免(成本认了)，IP段黑名单只拦svip0，工具号指纹=累充恰好到阈值(尤600万卡sv1)。金额=次数×2.3万(单次中位,相关0.998)。数据坑:次数/金额文件SVIP字段不一致，金额文件为最新权威。
§
Hapi语音审核:日均200h阿语,自建Whisper large-v3+阿里云GPU,阿语方言是ASR难点。
§
BytePlus国际控制台console.byteplus.com被Akamai拦机房/VPN(403 TCP_DENIED),需住宅IP;www.byteplus.com与console.volcengine.com不受影响。
§
钉钉文档/表格经config.yaml的4个MCP访问(勿用浏览器,有OAuth登录墙):dingtalk-docs仅adoc(脑图amind无MCP读);dingtalk-able仅AI表格able;dingtalk-sheet读写普通表格axls(get_all_sheets/get_range/set_cell_range)。用户发[DeviceInfo]设备数据填表,布尔大写TRUE/FALSE。
§
Hapi非SVIP送礼占比治理目标日均40%(健康值),8月底封黑产压43.2%但9月初回流47%(集中封不持久→持续封+防回流)。月初1号给SVIP发一大笔钱,非SVIP占比压低5-7pp,月初对比须剔除1号
§
黑产标注语义：标红=确认黑产(正样本)；未标红≠正常≠误报(不确定,有薅羊毛特征)。黑产=顶级薅羊毛(连续谱)。禁红字率当概率、禁反推「低红字率=干净」,只用lift富集度。评分=梯度:条件越多越黑产。
§
IP段拉黑输出a.b.c(不带.*)竖写可逗号隔开;IPv6不写(WARP归薅羊毛)。
§
黑产vs薅羊毛(用户权威):黑产=工具号=只送礼不收礼+批量≥10同特征+无社交+低充≤600万→封禁;薅羊毛=有收有送+≤50+有社交+低充≤600万→限制。静态字段(数字名/选国/零充)只是候选,数字名=默认名≠黑产,区分靠行为信号在事件流水表。选国/设备每日漂移。
§
风控效果评估:短期=操作后一周vs上周同期,长期=操作后vs操作前基线(累积效果,单次看短期)。复盘卡片=动作/数据表现(短期+长期)/达成度/问题/教训。钉钉'P的领域'知识库workspaceId=vr4zEOpQM29MrmDY。数据文件在~/Documents/~/Downloads。
§
Hapi SQL口径:svipLevel=null即非SVIP(未获SVIP),当天现1-11按SVIP(max聚合,非min/最终态)。asset_id:1金币/2钻石/13筹码。坑:NOT IN漏NULL、group by致JOIN膨胀。
§
手机号区号是硬信号(选国才漂移):南亚↔中东=正常(劳工),欧洲=疑点,+56智利/IP=高可疑。
§
虚拟软件建号:用户名数字+单字母(25654785l式);昵称工整英文(南亚真人不用);单IP多号跨多国。
§
中东≠南亚黑产逻辑:中东svip0(活跃91.6%/金币64.6%)=本地零充用户,金币来源钻石换币36.6%+升级活动26.1%(纯增发)+宝箱16%+房间返利8.6%+家族6%,充值≈0,去向93%送礼,有收有送非工具号,本质非充值化。