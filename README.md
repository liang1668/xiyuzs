# 小雨助手下载页

这是一个纯静态下载页，不需要框架或编译步骤。网页可部署到 Cloudflare Pages（也可使用 GitHub Pages）；APK、EXE 安装包由 GitHub Releases 提供，iPhone 使用网页版。

## 部署到 Cloudflare Pages

1. 将 `index.html` 提交到 GitHub 仓库根目录，并在 Cloudflare 控制台打开 **Workers & Pages → Create application → Pages → Connect to Git**，选择仓库 `liang1668/xiyuzs`。
2. 构建设置选择 **None** 或 **Static HTML**；生产分支选 `main`，**Build command 留空**，**Build output directory 填 `.`**。此项目没有编译步骤。
3. 保存并部署。成功后 Cloudflare 会提供 `*.pages.dev` 网站地址。
4. 绑定自己的域名：打开 Pages 项目的 **Custom domains → Set up a domain**，按提示添加域名并配置 DNS。

如果使用 GitHub Pages：在仓库 **Settings → Pages** 中选择 **Deploy from a branch**、`main` 分支和 `/ (root)` 目录，然后保存。

## 发布安装包到 GitHub

1. 打开仓库 **Releases → Draft a new release**。
2. 填写版本标签（例如 `v1.0.0`），将 `.apk`、`.exe` 或 `.zip` 安装包拖入附件区域。
3. 发布 Release。下载页会自动显示最新已发布 Release 的安装包，不需要重新上传网页。

APK 资产会显示在 Android 区域；EXE 和 ZIP 会显示在 Windows 区域。醒目的“立即下载”按钮会根据访问设备选择 APK、EXE，或在 iPhone/iPad 上打开网页版。若最新 Release 暂时没有 Windows 安装包，页面会显示提示并提供 Releases 入口。

请将仓库设为 **Public（公开）**，这样访客无需登录即可下载 Release 资产。iPhone 网页版链接仍为 `http://139.196.4.34:8080/`。请勿将访问令牌或其他密钥放进网页代码。
