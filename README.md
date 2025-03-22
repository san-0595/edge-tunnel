# Edge Tunnel

这是一个基于 Cloudflare Workers 平台的代理脚本

**欢迎各位大佬指正代码中存在的问题！** 

[![Stargazers over time](https://starchart.cc/ImLTHQ/edge-tunnel.svg?variant=adaptive)](https://starchart.cc/ImLTHQ/edge-tunnel)

如果觉得本项目对您有帮助, 请点个 Star 支持一下！

## 使用方法

请确保您已注册 GitHub 和 Cloudflare (简称 CF) 账号

[![Deploy to CF Workers](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/ImLTHQ/edge-tunnel)

**注意:** 部署 Workers 请务必绑定自定义域名

1. **Fork 本项目** 
2. **创建 Workers/Pages**
5. **添加环境变量**
6. **保存并部署**
8. **生效后导入订阅**

<details>
<summary><code><strong>「 建议做的 」</strong></code></summary>

**设置 GitHub Action 同步上游仓库**
1. 来到您 Fork 的仓库
2. 在 `Actions` 选项卡中, 点击 `Enable workflow`, 选择 `上游同步`
3. 启用此 Workflow 可以使您的仓库与作者的更新保持同步
</details>

## 变量说明

| 变量名 | 示例 | 备注 |
| - | - | - |
| `SUB_PATH` | `订阅路径` | https://域名/订阅路径 |
| `SUB_UUID` | `550e8400-e29b-41d4-a716-446655440000` | 用于验证订阅请求的 UUID |
| `TXT_URL` | `https://raw.githubusercontent.com/ImLTHQ/edge-tunnel/main/SpeedTest/HKG.txt` | 优选 IP 的 TXT 地址, 支持多个地址, 地址之间用换行分隔格式`地址:端口#节点名称`端口不填默认 443, 节点名称不填则使用默认节点名称 |
| `SUB_NAME` | `节点` | 默认节点名称 |
| `PROXY_IP` | `ts.hpc.tw:443` | 反代服务器 IP 地址和端口 |
| `SOCKS5_GLOBAL` | `true`,`false` | 是否启用 SOCKS5 全局反代 |
| `SOCKS5` | `账号:密码@地址:端口` | SOCKS5 代理服务器的连接信息, 格式为 `账号:密码@地址:端口` |
| `FAKE_WEB` | `baidu.com` | 根路径的伪装网站, 访问根目录时会跳转到该网站 |

<details>
<summary><code><strong>「 第三方 ProxyIP 」</strong></code></summary>

有能力请自建

- `ts.hpc.tw`
- `ProxyIP.US.CMLiussss.net`
- `ProxyIP.SG.CMLiussss.net`
- `ProxyIP.JP.CMLiussss.net`
- `ProxyIP.HK.CMLiussss.net`
- `ProxyIP.KR.CMLiussss.net`
- `ProxyIP.DE.tp2024.CMLiussss.net`
- `ProxyIP.Aliyun.CMLiussss.net`
- `ProxyIP.Oracle.CMLiussss.net`
- `ProxyIP.DigitalOcean.CMLiussss.net`
- `ProxyIP.Vultr.CMLiussss.net`
- `ProxyIP.Multacom.CMLiussss.net`
</details>

<details>
<summary><code><strong>「 本项目提供的优选 TXT 地址 」</strong></code></summary>

- `https://raw.githubusercontent.com/ImLTHQ/edge-tunnel/main/SpeedTest/HKG.txt` 香港
- `https://raw.githubusercontent.com/ImLTHQ/edge-tunnel/main/SpeedTest/KHH.txt` 台湾
- `https://raw.githubusercontent.com/ImLTHQ/edge-tunnel/main/SpeedTest/SIN.txt` 新加坡
- `https://raw.githubusercontent.com/ImLTHQ/edge-tunnel/main/SpeedTest/NRT.txt` 东京
- `https://raw.githubusercontent.com/ImLTHQ/edge-tunnel/main/SpeedTest/SEA.txt` 西雅图
- `https://raw.githubusercontent.com/ImLTHQ/edge-tunnel/main/SpeedTest/LHR.txt` 伦敦
</details>

## 已适配客户端

- v2ray
- clash

## 免责声明

本免责声明适用于 GitHub 上的 "edge-tunnel" 项目 (以下简称"本项目"), 项目链接为`https://github.com/ImLTHQ/edge-tunnel`

**用途**

- 本项目仅供教育、研究和安全测试目的而设计和开发
- 旨在为安全研究人员、学术界人士及技术爱好者提供一个探索和实践网络通信技术的工具
- 用途仅仅是作为代理用于隐藏真实IP, 并非作为绕过防火墙的工具

**合法性**

- 在下载和使用本项目代码时, 必须遵守使用者所适用的法律和规定使用者有责任确保其行为符合所在地区的法律框架、规章制度及其他相关规定

**免责**

- 作为本项目的 **二次开发作者** (以下简称“作者”), 我 **ImLTHQ** 强调本项目仅应用于合法、道德和教育目的
- 作者不认可、不支持亦不鼓励任何形式的非法使用如果发现本项目被用于任何非法或不道德的活动, 作者将对此强烈谴责
- 作者对任何人或组织利用本项目代码从事的任何非法活动不承担责任使用本项目代码所产生的任何后果, 均由使用者自行承担
- 作者不对使用本项目代码可能引起的任何直接或间接损害负责
- 为避免任何意外后果或法律风险, 使用者应在使用本项目代码后的 24 小时内删除代码

通过使用本项目代码, 使用者即表示理解并同意本免责声明的所有条款如使用者不同意这些条款, 应立即停止使用本项目

作者保留随时更新本免责声明的权利, 且不另行通知最新版本的免责声明将发布在本项目的 GitHub 页面上

## 感谢

- [shulng(代码建议)](https://github.com/shulng)
- [XIU2(CF测速)](https://github.com/XIU2)
- [zizifn(原作者)](https://github.com/zizifn)
- [cmliu(二次开发与ProxyIP提供者)](https://github.com/cmliu)