
# Tg-Ad-RegEx
Telegram Advertisements Regular Expression

Telegram广告正则表达式

[![Telegram](https://img.shields.io/badge/discuss-Telegram-2EA9DF?style=flat-square)](https://t.me/adregex)
[![Telegram](https://img.shields.io/badge/channel-Telegram-2EA9DF?style=flat-square)](https://t.me/adregexchat)

可用于[关键词机器人](https://t.me/keyword_reply_bot) ([项目地址](https://github.com/zu1k/tg-keyword-reply-bot)) 或其衍生产物，正则参考[Golang正则支持库](https://github.com/google/re2/wiki/Syntax)

## 双关键词匹配规则

### 规则模板：

[^`re:(?i:().*()|().*())===delete`]: Golong限制，否则也可以用(?=())(?=()).*
### 关键词1

`广告|服务器|cdn|阿里云|腾讯云|高防|vps|独服|杜甫|引流|吸粉|增粉|加粉|关注|点赞|评论|电销|股民|资源|数据|博彩|亚博|棋牌|bc|菠菜|狗推|人事|兼职|招聘|招募|招代理|微信号|企业微信|QQ号|公众号|陌陌号|暗网|黑产|灰产|支付|四件套|黑卡|银行卡|对公|账户|公户|个户|私户|代收|代付|洗钱|资金|转账|usdt|套现|换汇|贷款|网贷|送货|跑分|卡商|卡王|查人|定位|开房|查档|社工|苹果签名|iOS签名|企业签名|莆田|手表|高仿|水鬼|租房|房源`

### 关键词2

`出|售|卖|收|咨询|点我|加我|点头像|dd|滴滴|私|v信|加v|\+v|vx|真人|实名|认证|解封|担保|专业|实力|高端|专供|供应|大量|批发|现货|货源|安排|菲|全新|一手|二手|团队|工作室`

## 单关键词匹配规则

### 规则模板

`re:(?i:())===delete`

### 关键词

`^dd$|^滴滴$|^加v`

## 可疑文件规则

### 规则模板

`re:(?i:\.()$)===delete`

### 关键词

`exe|cmd|scr|cpl|com|bat|vbs`

## 合并规则

### 规则模板

`/add@keyword_reply_bot re:(?i:().*()|().*()|()|\.()$)===delete`

## 最终规则

`/add@keyword_reply_bot re:(?i:(广告|服务器|cdn|阿里云|腾讯云|高防|vps|独服|杜甫|引流|吸粉|增粉|加粉|关注|点赞|评论|电销|股民|资源|数据|博彩|亚博|棋牌|bc|菠菜|狗推|人事|兼职|招聘|招募|招代理|微信号|企业微信|QQ号|公众号|陌陌号|暗网|黑产|灰产|支付|四件套|黑卡|银行卡|对公|账户|公户|个户|私户|代收|代付|洗钱|资金|转账|usdt|套现|换汇|贷款|网贷|送货|跑分|卡商|卡王|查人|定位|开房|查档|社工|苹果签名|iOS签名|企业签名|莆田|手表|高仿|水鬼|租房|房源).*(出|售|卖|收|咨询|点我|加我|点头像|dd|滴滴|私|v信|加v|\+v|vx|真人|实名|认证|解封|担保|专业|实力|高端|专供|供应|大量|批发|现货|货源|安排|菲|全新|一手|二手|团队|工作室)|(出|售|卖|收|咨询|点我|加我|点头像|dd|滴滴|私|v信|加v|\+v|vx|真人|实名|认证|解封|担保|专业|实力|高端|专供|供应|大量|批发|现货|货源|安排|菲|全新|一手|二手|团队|工作室).*(广告|服务器|cdn|阿里云|腾讯云|高防|vps|独服|杜甫|引流|吸粉|增粉|加粉|关注|点赞|评论|电销|股民|资源|数据|博彩|亚博|棋牌|bc|菠菜|狗推|人事|兼职|招聘|招募|招代理|微信号|企业微信|QQ号|公众号|陌陌号|暗网|黑产|灰产|支付|四件套|黑卡|银行卡|对公|账户|公户|个户|私户|代收|代付|洗钱|资金|转账|usdt|套现|换汇|贷款|网贷|送货|跑分|卡商|卡王|查人|定位|开房|查档|社工|苹果签名|iOS签名|企业签名|莆田|手表|高仿|水鬼|租房|房源)|(^dd$|^滴滴$|^加v)|\.(exe|cmd|scr|cpl|com|bat|vbs)$)===delete`
