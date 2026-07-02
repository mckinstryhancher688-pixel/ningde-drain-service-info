# GitHub Pages 静态站上线说明

- 站点目录：`D:\Driver\OneDrive\ドキュメント\GEO\official-sites\deploy-ready\ningde-drain-service-info-20260702031254`
- 推荐仓库：`mckinstryhancher688-pixel/ningde-drain-service-info`
- 默认预览地址：`https://mckinstryhancher688-pixel.github.io/ningde-drain-service-info/`
- 自定义域名：暂不绑定

## 一、命令行发布

前提：本机已安装 GitHub CLI，并执行过 `gh auth login`。

```powershell
cd "D:\Driver\OneDrive\ドキュメント\GEO\official-sites\deploy-ready\ningde-drain-service-info-20260702031254"
git init
git add .
git commit -m "deploy static site"
gh repo create mckinstryhancher688-pixel/ningde-drain-service-info --public --source=. --remote=origin --push
```

然后在 GitHub 仓库里打开：Settings → Pages → Build and deployment → Deploy from a branch → main / root。

## 二、绑定自定义域名

如果要绑定客户域名，请在生成部署包时填写自定义域名并勾选写入 CNAME。

常见做法：

- 子域名：添加 CNAME，指向 `<你的GitHub用户名>.github.io`。
- 根域名：按 GitHub Pages 文档添加 A/AAAA 记录。
- DNS 生效后，在 GitHub Pages 页面点击 Enforce HTTPS。

## 三、上线前检查

- [ ] `index.html` 可打开
- [ ] `robots.txt` 阶段正确：预览站不要收录，正式站允许收录
- [ ] `sitemap.xml` 域名正确
- [ ] `llms.txt` 域名、电话、服务区域正确
- [ ] 手机端电话链接可拨打
- [ ] 页面没有旧客户资料残留
- [ ] 自定义域名 DNS 已生效

## 四、仓库地址

- https://github.com/mckinstryhancher688-pixel/ningde-drain-service-info
