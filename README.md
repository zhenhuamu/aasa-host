# 🍎 Apple App Site Association Host

适用于飞牛系 App（FNFresh / Actogo / E68 / MemberShop）的 AASA 文件托管。

## ✅ 特性
- 免费托管（Cloudflare Pages / Netlify）
- 自动 HTTPS
- 正确 MIME 类型（application/json）
- 支持 appclips + 多 appID

## 🚀 使用方法
1. 上传到你的 GitHub 仓库（例如 aasa-host）
2. 打开 [Cloudflare Pages](https://pages.cloudflare.com/)
3. 选择「Create a Project」→ 连接此仓库
4. 构建设置：
   - Build command: 留空
   - Output directory: `.`
5. 部署完成后访问：
   ```
   https://<你的项目>.pages.dev/.well-known/apple-app-site-association
   ```
6. 验证：
   ```bash
   curl -I https://<你的域名>/.well-known/apple-app-site-association
   ```
   确认返回：
   ```
   content-type: application/json
   ```

---

## 🔧 如要更新
修改 `apple-app-site-association` 内容后推送，Cloudflare 会自动重新部署。
