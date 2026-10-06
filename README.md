# 小雨助手下载页

这是一个可直接部署到 GitHub Pages 的静态下载页。页面从 `liang1668/xiyuzs` 的最新 GitHub Release 自动读取 APK、EXE 和 ZIP 安装包。

## 上传并发布网页

1. 在 GitHub 创建或打开 `liang1668/xiyuzs` 仓库。若要让所有用户都能访问下载页和安装包，请将仓库设为 **Public（公开）**。
2. 将 `index.html` 和本说明文件上传到仓库根目录并提交。
3. 打开仓库 **Settings → Pages**，在 **Build and deployment** 中选择 **Deploy from a branch**。
4. 选择 `main` 分支和 `/ (root)` 目录并保存。部署完成后，Pages 页面会显示网站地址。

## 发布安装包

1. 打开仓库 **Releases → Draft a new release**。
2. 填写版本标签（例如 `v1.0.0`），并上传 `.apk`、`.exe` 或 `.zip` 安装包。
3. 发布 Release。下载页会自动显示最新版本及匹配平台的安装包，不需要重新上传网页。

请勿将访问令牌或其他密钥放进网页代码。公共下载应使用公开仓库的 Release 资产。
