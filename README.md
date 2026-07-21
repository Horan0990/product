# Snapriva

Snapriva 是一个基于 TanStack Start 构建的在线图片工具站，同时内置了一套可复用的 SaaS 业务底座。项目面向 PNG、JPG、WebP、Base64 等常见图片处理场景，优先使用浏览器本地处理能力完成转换、压缩、裁剪、旋转、水印和 PNG 信息查看等工作；需要服务端、AI 或存储能力的流程会通过工具元数据明确标记。

除了公开图片工具页面，项目还预置了用户系统、后台管理、RBAC 权限、积分、订阅、支付、API Key、邀请码、CMS、双语内容和 Cloudflare Workers 部署配置，适合作为图片工具产品、AI 图片产品或轻量 SaaS 的起点。

## 功能概览

- **在线图片工具**：支持 PNG 透明化、PNG 压缩、PNG/JPG/WebP 转换、通用图片压缩、图片缩放、裁剪、旋转、水印和 PNG 查看器等已上线工具。
- **工具注册体系**：工具能力通过 manifest 管理，区分 `live` 和 `planned` 状态，支持分类页、详情页、关联工具、SEO 元信息和按需加载的运行时 processor。
- **浏览器本地处理**：图片工具 processor 运行在客户端 Canvas / Base64 runtime 中，列表页、分类页和 SEO 页面不会提前打包具体处理器。
- **多语言与 SEO**：使用 Paraglide JS 管理英文和中文文案，内置 canonical、hreflang、sitemap、robots、JSON-LD、博客和静态法律页面。
- **认证与用户中心**：better-auth 提供邮箱登录、OAuth 扩展能力、用户资料、账单、积分、订阅、API Key 和工单页面。
- **后台管理**：包含用户、角色、权限、订单、订阅、积分、分类、文章、邀请码、工单和系统设置管理。
- **支付与积分**：内置订单、订阅、积分发放/消费、支付回调和 webhook 处理逻辑，可接入 Stripe、PayPal、Creem、支付宝、微信支付等 provider。
- **存储与上传**：支持 S3/R2 上传配置；未配置对象存储时，图片上传可按大小限制回退到内联 base64。
- **多数据库支持**：通过 Drizzle ORM 支持 SQLite、D1、Turso、PostgreSQL 和 MySQL。
- **Cloudflare 部署**：提供 Cloudflare Workers、D1 和 Hyperdrive/PostgreSQL 的构建与部署脚本。

## 地址

https://snapriva.com/