# 作者及联系方式
作者：冰河  
QQ：2711098650  
微信公众号： 冰河技术

# 工具简述
本项目均为冰河亲自编写并整理的Python渗透脚本集合，可直接拿来用于渗透实战

# 脚本说明
### com.binghe.hacker.tools.script.attack.crypt 包下的脚本：
```
1.crypt_attack.py: 利用字典破解Unix/Linux口令 
``` 
  
### com.binghe.hacker.tools.script.attack.ssh 包下的脚本
```
1. pxssh_connection.py: 使用pexpect中的pxssh模块连接ssh， 需要在Linux下执行  
2. ssh_attack.py: 暴力破解SSH  
3. ssh_botnet.py: 构建SSH僵尸网络,批量向多个SSH终端发送执行命令，达到批量控制目标主机的目的  
4. ssh_connection.py: 连接ssh，需要在Linux下执行  
5. ssh_dsa_attack.py: 利用ssh密钥暴力破解SSH 
``` 
  
### com.binghe.hacker.tools.script.attack.zip 包下的脚本
```
1. attack_zip.py: 暴力破解zip文件  
2. attack_zip_input_args.py: 暴力破解zip文件  
```
### com.binghe.hacker.tools.script.attack.ftp 包下的脚本
```
1. ftp_anonymous.py: 确定一个FTP服务器是否允许匿名登录，允许则返回True,不允许返回False
2. ftp_brute.py: 根据用户名:密码字典暴力爆破FTP服务器
3. ftp_web_page.py: 在FTP服务器上搜索网页
4. ftp_inject.py: 感染FTP上的网页
5. ftp_attack_web_page.py: 完整的感染FTP服务器上的网页脚本
```
### com.binghe.hacker.tools.script.attack.metasploit 包下的脚本
```
1. conficker.rc: Metasploit脚本，在Kali命令行中运行msfconsole -r conficker.rc 即可运行该脚本
2. metasploit_attack.py: 利用Metasploit实施攻击的脚本，主要针对Windows系统
```
### com.binghe.hacker.tools.script.attack.0day 包下的脚本
```
1.zeroday_ftp_attack.py: 0day漏洞利用脚本，针对FreeFloat FTP
2.zeroday_ftp_attack2.py: 0day漏洞利用脚本，针对FreeFloat FTP
```
### com.binghe.hacker.tools.script.net 包下的脚本
```
1. windows_reg_net.py: 列举Windows注册表中存储的网络名和默认网关的Mac
2. windows_reg_net_location.py: 列举Windows注册表中存储的网络名和默认网关的Mac,并通过https://wigle.net查询物理位置
3. windows_net_location.py: 测试Mac地址的地理位置
```
### com.binghe.hacker.tools.script.recycle 包下的脚本
```
1. windows_recycle_recovery.py: 查找系统中所有用户对应的回收站中的文件，并打印出来
```
### com.binghe.hacker.tools.script.meta 包下的脚本
```
1. meta_pdf.py: 分析PDF文件中的元数据信息
2. meta_image.py: 下载链接中的所有图片，并检查每张图片中的GPS元数据，若存在GPS元数据，在打印此文件存在GPS元数据
3. meta_skype_sqlite3.py: 检查Skype数据库，把账户信息、联系人地址、通话记录以及存放在数据库中的消息打印出来
4. meta_firefox_sqlite3.py: 查询火狐浏览器存储的上网记录
5. meta_sms_ios.py: 提取IOS备份中的所有短信记录
```
### com.binghe.hacker.tools.script.network.pcap 包下的脚本
```
1. GeoLiteCity.dat: IP的地理位置数据库
2. search_ip_geolitecity.py: 使用GeoLiteCity.dat数据库查询指定IP的位置信息
3. data.pcap: 数据包文件,供测试分析数据包用
4. analysis_pcap_dpkt.py: 使用dpkt分析pcap数据包
5. analysis_pcap.py: 分析pcap数据包，可以直接看到数据包的源和目标的物理位置，此脚本是其他三个脚本的最终整合版
6. analysis_pcap_kml.py: 分析pcap文件，并将分析结果生成KML文件在Google地球上标注

```
### com.binghe.hacker.tools.script.network.loic 包下的脚本
```
1. analysis_dpkt_loic.py: 使用Dpkt发现下载LOIC的行为
2. analysis_pcap_irc.py: 解析HIVE服务器上的IRC命令
3. analysis_loic_online.py: 实时检测DDos攻击
4. analysis_loic.py: 分析loic, 实时检测DDos攻击，此脚本为analysis_dpkt_loic.py、analysis_loic_online.py、analysis_pcap_irc.py 三个脚本的整合
```
### com.binghe.hacker.tools.script.network.scapy 包下的脚本
```
1. scapy_ip_ttl.py: 检测数据包中的TTL值是否为假，如果是假的则打印出来，此脚本可检测nmap是否启用了伪装源IP扫描
2. scapy_dns_fast_flux.py 用Scapy找出flux流量
3. scapy_dns_domain_flux.py: 用Scapy找出Domain Flux流量
```
### com.binghe.hacker.tools.script.network.syn 包下的脚本
```
1. scapy_syn_flood.py: 使用Scapy制造SYN泛洪攻击
2. scapy_syn_tcp.py: 读取TCP序列号
3. scapy_syn_forge.py: 伪造TCP连接
4. scapy_syn.py: 使用Scapy制造SYN泛洪攻击、读取TCP序列号并伪造TCP连接; 此脚本是scapy_syn_flood.py、scapy_syn_forge.py和scapy_syn_tcp.py的整合版
```
### com.binghe.hacker.tools.script.network.warn 包下的脚本
```
1. scapy_warn_data.py:产生大量警报的工具包，分析人员也可以使用这个工具来验证IDS是否能够正确识别出恶意流量
2. scapy_warn.py: 生成触发拒绝服务攻击、漏洞利用(exploits)和踩点扫描警报的数据包
```
### com.binghe.hacker.tools.script.network.wireless 包下的脚本
```
此包下的如下脚本均需要将网卡设置为监听模式：
1. wireless_scapy_sniffer.py: 侦听无线网卡数据流量
2. wireless_regex.py: 正则表达式验证American Express信用卡
3. wireless_express.py: 嗅探无线数据包中的信用卡信息
4. wireless_customer_info.py: 截获宾馆中无线数据流量中的用户信息
5. wireless_google.py: 抓取Google搜索数据并实施显示的无线网络数据包嗅探器
6. wireless_ftp.py: 嗅探FTP登录口令
7. wireless_probe.py: 发现802.11请求
8. wireless_hidden.py: 找出隐藏的802.11网络的网络名
9. wireless_dup.py: 复制RadioTap、802.11、SNAP、LLC、IP和UDP层中的信息
10. wireless_airplain.py: 截获无人机
11. wireless_cookie_wordpress_print.py: 解析Wordpress HTTP会话
12. wireless_cookie_wordpress_find_attack.py: 检测企图盗用Wordpress会话的人，并将结果显示在屏幕上
```
### com.binghe.hacker.tools.script.network.bluetooth 包下的脚本
```
1. bluetooth_discorver.py: 发现周围的蓝牙设备，并把蓝牙设备的名字和Mac地址输出到屏幕
2. bluetooth_discover_circle.py: 持续监听新的蓝牙设备
3. bluetooth_rfcomm_channel.py: 检测RFCOMM通道是否开放并处于监听状态
4. bluetooth_rfcomm_protocol.py: 使用蓝牙服务发现协议打印蓝牙设备的服务名称、协议和端口号
5. bluetooth_obexftp.py 用Python ObexFTP控制打印机
6. bluetooth_phone.py: 窃取手机电话簿信息
```
### com.binghe.hacker.tools.script.network.spy 包下的脚本
```
1. mechanize_website_source.py: 用mechanize解析网站源代码
2. mechainze_proxy.py: mechainze代理
3. mechainze_website_cookie.py: 打印网站的cookie
4. mechainze_user_agent.py: 修改访问网站的user-agent
5. mechainze_browser.py: 自定义浏览器(匿名)
6. mechainze_browser_test.py: 测试自定义浏览器，可打印多个不同的cookie
7. mechainze_browser_links.py: 分析并打印网页上的链接
8. mechainze_browser_imgs.py: 从网站上下载图片，并直接写入硬盘
9. mechainze_google.py: 与Google API交互
10. mechainze_twitter.py: 从Twitter上获取数据
11. mechainze_twitter_locate.py: 从推文中获取地理位置信息
12. mechainze_twitter_hobby.py: 用正则表达式解析Twitter用户的兴趣爱好
```
### com.binghe.hacker.tools.script.network.email 包下的脚本
```
1. smtplib_send_email.py: 使用smtplib发送电子邮件
2. smtp_twitter_send_mail.py: 利用目标对象留在Twitter中可以公开的访问的信息对他发送邮件进行钓鱼攻击
3. mechainze_browser.py: 自定义浏览器类
4. mechainze_twitter_hobby.py: 用正则表达式解析Twitter用户的兴趣爱好
```
### com.binghe.hacker.tools.script.network.ak 免杀包下的脚本
```
1. bindshell.py: 生成绑定1337端口的Shell
2. check_virus.py: 将生成的bindshell.exe提交到vscan.novirusthanks.org检测
```
### com.binghe.hacker.tools.script.scanner 包下的脚本
```
1. scan_host_ports.py: 端口扫描器  
2. scan_nmap.py: 使用nmap进行扫描
```

# 出现率高的密码
```
aaa
academia
anything
coffee
computer
cookie
oracle
password
secret
super
unknown
```
# 免责声明
以上脚本只限于对自己做的项目进行安全测试，不可用于其他，如果在使用过程中出现任何违法违规事件，均与作者本人无关。

# 扫一扫关注微信公众号

**你在刷抖音，玩游戏的时候，别人都在这里学习，成长，提升，人与人最大的差距其实就是思维。你可能不信，优秀的人，总是在一起。** 
  
扫一扫关注冰河技术微信公众号  
![微信公众号](https://github.com/sunshinelyz/binghe_resources/blob/master/images/subscribe/qrcode_for_gh_0d4482676600_344.jpg)  
