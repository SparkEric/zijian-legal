# 字间 - GitHub Pages 部署指南

本目录包含字间应用的法律声明页面，可直接部署到 GitHub Pages。

## 文件说明

- `index.html` - 首页（导航页）
- `terms.html` - 用户服务协议
- `privacy.html` - 隐私政策

## 部署步骤

### 方法一：手动创建仓库（推荐，最简单）

1. 打开 https://github.com/new 创建新仓库
   - Repository name: `zijian-legal` （或你喜欢的名字）
   - 选择 Public
   - 勾选 "Add a README file"
   - 点击 Create repository

2. 上传文件
   - 点击 "Add file" → "Upload files"
   - 将 `index.html`、`terms.html`、`privacy.html` 三个文件拖进去
   - 点击 "Commit changes"

3. 启用 GitHub Pages
   - 进入仓库的 Settings → Pages
   - Source 选择 "Deploy from a branch"
   - Branch 选择 `main` ，文件夹选 `/ (root)`
   - 点击 Save
   - 等待 1-2 分钟

4. 获取访问链接
   - 页面会显示类似 `https://你的用户名.github.io/zijian-legal/` 的链接
   - 用户协议链接：`https://你的用户名.github.io/zijian-legal/terms.html`
   - 隐私政策链接：`https://你的用户名.github.io/zijian-legal/privacy.html`

### 方法二：使用 Git 命令行

```bash
# 进入 agreement 目录
cd d:\Backup\converter\agreement

# 初始化 git 仓库
git init
git add .
git commit -m "initial commit"

# 添加远程仓库（替换为你的仓库地址）
git remote add origin https://github.com/你的用户名/zijian-legal.git

# 推送到 GitHub
git branch -M main
git push -u origin main
```

然后在仓库设置中启用 Pages 即可。

## 在 AppGallery Connect 中填写

在应用发布页面的"隐私声明"部分填写：

- **用户协议链接**：`https://你的用户名.github.io/zijian-legal/terms.html`
- **隐私政策链接**：`https://你的用户名.github.io/zijian-legal/privacy.html`

## 注意事项

- GitHub Pages 站点是公开的，任何人都可以访问
- 首次部署可能需要 1-2 分钟才能生效
- 如果有自定义域名，也可以配置自定义域名
