EDtunnel-呆萌恐龙🦖
<p align="center"> 
<img src="https://tc-1303817403.cos.ap-chengdu.myqcloud.com/2024/06/23/667700fe51ffa.png" alt="edgetunnel" style="margin-bottom: -50px;">
</p>

GitHub 存储库 [https://github.com/zizifn/edgetunnel](https://github.com/zizifn/edgetunnel)

询问问题和 cloudflare ips: [https://t.me/dmkljlq](https://t.me/dmkljlq)

[![Repository](https://img.shields.io/badge/View%20on-GitHub-blue.svg)](https://github.com/zizifn/edgetunnel)

## 可用分支并解释

| 分支名称 | 说明 |
| ------------- | ---------------------------- |
| remote-socks5 | 用于远程 SOCKS5 代理池实现的分支 |
| socks5 | 用于 SOCKS5 proxyIP 实现的分支 |
| vless | 用于出站 VLESS 协议实现的分支 |
| vless2 | 用于替代出站 VLESS 协议实现的分支 |
| code1 | 用于 code1 功能开发的分支 |
| code2 | 用于 code2 替代功能开发的分支 |
| dns | 用于 DNS 替代相关开发的分支 |
| main | 项目的主分支 |
| pages | 用于在 Cloudflare Pages 上部署的新版本 |

## 在 pages.dev 中部署

1. 观看YouTube视频：

   [https://youtu.be/Mi6O3dJXeDI](https://youtu.be/Mi6O3dJXeDI)

2. 克隆此存储库并在 cloudflare 页面中部署。

## 在 worker.dev 中部署

1. 复制 `_worker.js` 代码来自 [here](https://github.com/OuyJay/EDtunnel/blob/main/_worker.js).

2. 或者，您可以单击下面的按钮直接部署。

   [![Deploy to Cloudflare Workers](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/OuyJay/EDtunnel)

## 懒得部署

`aHR0cHM6Ly9vc3MudjJyYXlzZS5jb20vcHJveGllcy9kYXRhLzIwMjMtMDctMzAvRnJFS1lvQS50eHQ=` （免费 clash.meta 订阅配置）

## UUID 设置（可选）

1. 在cloudflare 页面部署时，可以在wrangler.toml文件中设置 uuid，变量名为UUID.filewrangler.toml也是支持的。（推荐）如果在网页部署，则不能在wrangler.toml文件中设置 uuid。

2. 在worker.dev中部署时，可以在_worker.js文件中设置uuid，变量名为userID.filewrangler.toml也是支持的。(推荐)如果在网页中部署，则不能在wrangler.toml文件中设置uuid，这种情况下，也可以在UUID环境变量中设置uuid。

注意：UUID是您想要设置的 uuid。pages.dev 和 worker.dev 所有方法都支持，但取决于您的部署方法。


### UUID 设置示例

1. 单个 uuid 环境变量

   ```.environment
   UUID = "uuid here your want to set"
   ```

2. 多个 uuid 环境变量

   ```.environment
   UUID = "uuid1,uuid2,uuid3"
   ```

   注意：uuid1，uuid2，uuid3 之间以逗号分隔,。当你设置多个 uuid 时，你可以使用它https://edtunnel.pages.dev/uuid1来获取冲突配置和 vless:// 链接。

## 订阅 vless:// 链接 (可选)

1. 访问https://edtunnel.pages.dev/uuid your set以获取订阅链接。

2. 访问https://edtunnel.pages.dev/sub/uuid your set以获取带有路径的订阅内容uuid your set。

注意：是您在 UUID 环境或文件uuid your set中设置的 uuid 。当您设置多个 uuid 时，您可以使用路径获取订阅内容。（仅支持多个 uuid 集中的第一个 uuid）wrangler.toml_worker.jshttps://edtunnel.pages.dev/sub/uuid1uuid1

3. 访问以获取带有路径和格式的https://edtunnel.pages.dev/sub/uuid your set/?format=clash订阅内容。内容将以 base64 编码返回。uuid your setclash

注意：是您在 UUID 环境或文件uuid your set中设置的 uuid 。当您设置多个 uuid 时，您将使用它来获取带有路径和格式的订阅内容。（仅支持多个 uuid 集中的第一个 uuid）wrangler.toml_worker.jshttps://edtunnel.pages.dev/sub/uuid1/?format=clashuuid1clash

## 订阅 Cloudflare bestip(纯 ip) 链接

1. 访问https://edtunnel.pages.dev/bestip/uuid your set以获取订阅信息。

2. 将 url 链接订阅https://edtunnel.pages.dev/bestip/uuid your set到您想要使用的任何客户端（clash/v2rayN/v2rayNG）。

3. 完成。如果有任何问题请加入 [@edtunnel](https://t.me/dmkljlq)

## 多端口支持（可选）

   <!-- let portArray_http = [80, 8080, 8880, 2052, 2086, 2095];
	let portArray_https = [443, 8443, 2053, 2096, 2087, 2083]; -->

有关 Cloudflare 支持的端口列表，请参阅 [官方文档](https://developers.cloudflare.com/cloudflare-one/connections/connect-apps/ports).

默认端口为80和443，如果要添加更多端口，可以使用以下端口：

```text
80, 8080, 8880, 2052, 2086, 2095, 443, 8443, 2053, 2096, 2087, 2083
http port: 80, 8080, 8880, 2052, 2086, 2095
https port: 443, 8443, 2053, 2096, 2087, 2083
```

如果您在 cloudflare 页面中部署，则不支持 https 端口。只需直接使用订阅链接添加多个端口节点，订阅内容将返回所有 Cloudflare 支持的端口。

## 代理 IP (可选)

1.在cloudflare页面部署时，可以在wrangler.toml文件中设置proxyIP，变量名是PROXYIP。

2. 在worker.dev中部署时，可以在_worker.js文件中设置proxyIP，变量名为proxyIP。

注意：proxyIP是您要设置的 IP 或域。这意味着 proxyIP 用于通过代理路由流量，而不是直接路由到使用 Cloudflare (CDN) 的网站。如果您不设置此变量，与 Cloudflare IP 的连接将被取消（或阻止）...

原因：到 Cloudflare IP 范围的出站 TCP 套接字暂时被阻止，请参阅 [tcp-sockets 文档](https://developers.cloudflare.com/workers/runtime-apis/tcp-sockets/#considerations)

## 用法

首先，在浏览器中打开你的pages.dev域名https://edtunnel.pages.dev/，然后你可以看到以下页面：/uuid your seetting获取冲突配置的路径和vless://链接。
