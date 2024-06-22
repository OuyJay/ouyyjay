

EDtunnel-Dāi méng kǒnglóng 🦖

![edgetunnel](https://camo.githubusercontent.com/545035e7d0bc8da5e91bb38721e309d723eb2d4c1a94ef7605c3ff3a5945a5d9/68747470733a2f2f74632d313330333831373430332e636f732e61702d6368656e6764752e6d7971636c6f75642e636f6d2f323032342f30362f32332f363637373032366437356630352e706e67)

🦕 [GitHub 存储库](https://github.com/DaiMengKongLong/EDtunnel/tree/main)

🦊[UUID 生成](https://www.uuidgenerator.net/)

 [⚡️电报群](https://t.me/dmkljlq)


## pages.dev 中部署


1. 观看YouTube视频：
    
    [https://youtu.be/Mi6O3dJXeDI](https://youtu.be/Mi6O3dJXeDI)
    
2. 克隆此存储库并在 cloudflare 页面中部署。
    

## worker.dev 中部署


1. 复制 `_worker.js` 代码来自 [文件](https://github.com/DaiMengKongLong/EDtunnel/blob/main/_worker.js).
    
2. 或者，您可以单击下面的按钮直接部署。
    
    [![Deploy to Cloudflare Workers](https://camo.githubusercontent.com/706bbe2a2cf53a4824ae5e2b599311927e28540dc8a9a57a16f8f5b195572aeb/68747470733a2f2f6465706c6f792e776f726b6572732e636c6f7564666c6172652e636f6d2f627574746f6e)](https://deploy.workers.cloudflare.com/?url=https://github.com/DaiMengKongLong/EDtunnel)


## 多端口支持（可选）

默认端口为80和443，如果要添加更多端口，可以使用以下端口：

```
80, 8080, 8880, 2052, 2086, 2095, 443, 8443, 2053, 2096, 2087, 2083
http port: 80, 8080, 8880, 2052, 2086, 2095
https port: 443, 8443, 2053, 2096, 2087, 2083
```

如果您在 cloudflare 页面中部署，则不支持 https 端口。只需直接使用订阅链接添加多个端口节 点，订阅内容将返回所有 Cloudflare 支持的端口。

## 代理 IP (可选)

1.  在cloudflare页面部署时，可以在wrangler.toml文件中设置proxyIP，变量名是PROXYIP。
    
2.  在worker.dev中部署时，可以在_worker.js文件中设置proxyIP，变量名为proxyIP。
    
    注意：proxyIP是您要设置的 IP 或域。这意味着 proxyIP 用于通过代理路由流量，而不是直接路由到使用 Cloudflare (CDN) 的网站。如果您不设置此变量，与 Cloudflare IP 的连接将被取消（或阻止）...

原因：到 Cloudflare IP 范围的出站 TCP 套接字暂时被阻止，请参阅 [tcp-sockets 文档](https://developers.cloudflare.com/workers/runtime-apis/tcp-sockets/#considerations)

## 用法

首先，在浏览器中打开你的pages.dev域名
