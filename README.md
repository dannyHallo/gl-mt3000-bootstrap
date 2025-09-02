# 重置 SSH 链接

C:/Users/<user_name>/.ssh/known_hosts

# 建立路由器和电脑的 ssh 连接

ssh root@192.168.8.1

# 使用脚本切换到 iStore 风格

https://cafe.cpolar.cn/wkdaily/gl-inet-onescript/src/branch/master

wget -O gl-inet.sh https://cafe.cpolar.cn/wkdaily/gl-inet-onescript/raw/branch/master/gl-inet.sh && chmod +x gl-inet.sh && ./gl-inet.sh

there's also a copy at ./gl-inet.sh

选择选项 1 （一键风格化）

https://didiboy0702.gitbook.io/wukongdaily/new-shou-ye/mt3000-bu-shua-ji-shi-yong-zhi-nan

# 安装 OpenClash

Luci - iStore - 手动安装

- 对应的卸载方式

```zsh
# see all installed packages (including manual installations)
opkg list-installed

# remove this one
opkg remove luci-app-openclash
```

# OpenClash 配置

配置订阅
https://45.137.181.239/api/v1/client/subscribe?token=043a2abc9bfa49508303dc70a644c9ba

加速
Plugin Settings - 模式设置 - 最下方 切换页面到 Fake-IP 模式
Plugin Settings - 模式设置 - 运行模式：Fake-IP (TUN-混合) 模式 「UDP-TUN, TCP-转发」
保存配置

Overwrite Settings - DNS 设置 - 勾选自定义上游 DNS 服务器
Overwrite Settings - DNS 设置 - 勾选追加上游 DNS
Overwrite Settings - DNS 设置 - NameServer - 取消勾选全部
Overwrite Settings - DNS 设置 - Default-NameServer - 取消勾选全部
保存配置

Overwrite Settings - 常规设置 - Github 地址修改 - 选择第一个即可 （https://fastly.jsdelivr.net/）
保存配置

Plugin Settings - 版本更新
然后内核更新至 Master 最新 （可选）

Config Subscribe - 配置 Clash 订阅信息
保存配置 - 更新配置

启动 OpenClash

