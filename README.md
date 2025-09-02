# GL MT3000 Bootstrap guide

## References

<https://didiboy0702.gitbook.io/wukongdaily/new-shou-ye/mt3000-bu-shua-ji-shi-yong-zhi-nan>
<https://cafe.cpolar.cn/wkdaily/gl-inet-onescript/src/branch/master>

## Connect with SSH

- If connected previously, remove the host first from `C:/Users/<user_name>/.ssh/known_hosts`

```zsh
ssh root@192.168.8.1
```

## Switch to iStore theme

- make sure the time zone is correct

```zsh
wget -O gl-inet.sh https://cafe.cpolar.top/wkdaily/gl-inet-onescript/raw/branch/master/gl-inet.sh && chmod +x gl-inet.sh && ./gl-inet.sh
```

- Selete option 1 （一键风格化）

- Do not close the shell before it completed with successful notification like below.

```zsh
恭喜您!现在你的路由器已经变成iStoreOS风格啦!
现在您可以访问8080端口 查看是否生效 http://192.168.8.1:8080
更多up主项目和动态 请务必收藏我的导航站 https://tvhelper.cpolar.top
赞助本项目作者 https://wkdaily.cpolar.top/01
```

## Install OpenClash

Luci - iStore - 手动安装

## Uninstall Openclash
You can use this command to uninstall, but keep in mind that the configs will not be cleaned up completely, it's recommended to reset the router directly.

```zsh
# see all installed packages (including manual installations)
opkg list-installed

# remove this one
opkg remove luci-app-openclash
```

## OpenClash 配置

Config subscribe - config - 保存配置 - 更新配置

Follow KISS principle, you are done now.

Here's a way to optimize, but it doesn't work in my case now.

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



