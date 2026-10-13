# 小雨助手下载页

这是一个纯静态下载页，不需要框架或编译步骤。网页可部署到 Cloudflare Pages（也可使用 GitHub Pages）；Android 和 Windows 安装包使用国内直连地址，iPhone 使用网页版。

## 部署到 Cloudflare Pages

1. 将 `index.html`、`guide.html` 和 `guide` 图片目录一并提交到 GitHub 仓库根目录，并在 Cloudflare 控制台打开 **Workers & Pages → Create application → Pages → Connect to Git**，选择仓库 `liang1668/xiyuzs`。
2. 构建设置选择 **None** 或 **Static HTML**；生产分支选 `main`，**Build command 留空**，**Build output directory 填 `.`**。此项目没有编译步骤。
3. 保存并部署。成功后 Cloudflare 会提供 `*.pages.dev` 网站地址。
4. 绑定自己的域名：打开 Pages 项目的 **Custom domains → Set up a domain**，按提示添加域名并配置 DNS。

如果使用 GitHub Pages：在仓库 **Settings → Pages** 中选择 **Deploy from a branch**、`main` 分支和 `/ (root)` 目录，然后保存。

## 下载地址

- Android APK：`http://139.196.4.34:8080/downloads/xyzs.apk`
- Windows EXE：`http://139.196.4.34:8080/downloads/xyzs.exe`
- iPhone/iPad 网页版：`http://139.196.4.34/lottery/index.html`

页面会自动识别 Android、iPhone/iPad 和其他设备，为“立即下载”按钮选择对应地址；平台卡片也提供直接链接。更换安装包时请同步更新 `index.html` 中的平台下载链接。请勿将访问令牌或其他密钥放进网页代码。
