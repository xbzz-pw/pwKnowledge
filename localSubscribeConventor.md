
# 说明
使用转换工具为 [subconverter](https://github.com/tindy2013/subconverter)  

# 步骤
## 1. 首先，在你本地跑起上文的 *本地转换工具*  
## 2. 使用 *[订阅转换工具](https://acl4ssr-sub.github.io/)* 转换
*后端地址* 选用本地的 **subconverter**  
## 3. 做DNS防泄漏
在转换完的订阅链接中 添加/替换 `config=https://cf.buliang0.cf/clash-rules/nodnsleak.ini` 参数  
该 `ini` 原文如下：  
```
[custom]
;解决DNS泄露，无分流群组
ruleset=🚀 节点选择,[]DOMAIN-SUFFIX,xn--ngstr-lra8j.com
ruleset=🚀 节点选择,[]DOMAIN-SUFFIX,services.googleapis.cn
ruleset=🚀 节点选择,https://raw.githubusercontent.com/ACL4SSR/ACL4SSR/master/Clash/Ruleset/GoogleCNProxyIP.list
ruleset=DIRECT,https://raw.githubusercontent.com/ACL4SSR/ACL4SSR/master/Clash/LocalAreaNetwork.list
ruleset=DIRECT,https://raw.githubusercontent.com/ACL4SSR/ACL4SSR/master/Clash/UnBan.list
ruleset=DIRECT,https://raw.githubusercontent.com/ACL4SSR/ACL4SSR/master/Clash/ChinaDomain.list
ruleset=DIRECT,https://raw.githubusercontent.com/ACL4SSR/ACL4SSR/master/Clash/ChinaMedia.list
ruleset=REJECT,https://raw.githubusercontent.com/ACL4SSR/ACL4SSR/master/Clash/BanAD.list
ruleset=REJECT,https://raw.githubusercontent.com/ACL4SSR/ACL4SSR/master/Clash/BanProgramAD.list
ruleset=DIRECT,https://raw.githubusercontent.com/ACL4SSR/ACL4SSR/master/Clash/ChinaCompanyIp.list
ruleset=DIRECT,https://raw.githubusercontent.com/ACL4SSR/ACL4SSR/master/Clash/ChinaIp.list
ruleset=DIRECT,[]GEOIP,CN,no-resolve
ruleset=🚀 节点选择,[]FINAL

custom_proxy_group=🚀 节点选择`select`[]♻️ 自动选择`[]DIRECT`.*
custom_proxy_group=♻️ 自动选择`url-test`.*`http://www.gstatic.com/generate_204`300,,50

enable_rule_generator=true
overwrite_original_rules=true
```
