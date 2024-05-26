# CF-Workers-DoH

这是一个使用Cloudflare Workers构建的DNS-over-HTTPS（DoH）服务的示例项目。此项目允许您通过HTTPS协议进行DNS查询，以提高DNS查询的隐私和安全性。

## 功能

- 支持通过GET和POST方法进行DNS查询。
- 支持`application/dns-message`和`application/dns-json`两种Content-Type。
- 根据请求的类型自动选择相应的处理方式，以优化性能和减少计费时间。

## 文件结构

- `_worker.js`: Cloudflare Worker的主文件，包含了处理DNS查询的核心逻辑。

## 依赖

- Cloudflare Worker：此项目依赖于Cloudflare提供的无服务器计算平台，用于部署和运行代码。

## 安装和使用

1. **创建Cloudflare Worker**：
   - 登录到Cloudflare控制面板。
   - 导航到“Workers”部分。
   - 创建一个新的Worker，并将`_worker.js`的代码粘贴到新Worker的脚本编辑器中。

2. **配置路由**：
   - 在“Workers”部分，配置一个路由，使您的Worker在特定域名或路径下运行。

## 致谢

特别感谢代码的原作者[tina-hello](https://github.com/tina-hello/doh-cf-workers)提供的代码示例。
