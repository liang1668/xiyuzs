# 小雨助手下载页

这是一个可直接部署到 GitHub Pages 的静态下载页。网页由 GitHub Pages 托管，APK、EXE 安装包和 iPhone 网页版由下载服务器提供。

## 上传并发布网页

1. 在 GitHub 创建或打开 `liang1668/xiyuzs` 仓库。若要让所有用户都能访问下载页和安装包，请将仓库设为 **Public（公开）**。
2. 将 `index.html` 和本说明文件上传到仓库根目录并提交。
3. 打开仓库 **Settings → Pages**，在 **Build and deployment** 中选择 **Deploy from a branch**。
4. 选择 `main` 分支和 `/ (root)` 目录并保存。部署完成后，Pages 页面会显示网站地址。

## 上传安装包到下载服务器

将安装包上传到服务器 `139.196.4.34:8080` 对应的 `/downloads/` 目录，并使用以下文件名：

- Android：`xiaoyu.apk`
- Windows：`xyzs.exe`

网页按钮分别链接到 `http://139.196.4.34:8080/downloads/xiaoyu.apk` 和 `http://139.196.4.34:8080/downloads/xyzs.exe`，iPhone 网页版链接保持为 `http://139.196.4.34:8080/`。如果服务器地址或文件名变化，需要同步修改 `index.html` 中对应链接。

服务器需允许浏览器直接访问这些文件。建议为下载服务器启用 HTTPS；若安装包应直接下载而不是在浏览器中打开，请让服务器为文件响应设置 `Content-Disposition: attachment`。

GitHub Pages 只托管网页，不托管这些安装包。请勿将访问令牌或其他密钥放进网页代码。
