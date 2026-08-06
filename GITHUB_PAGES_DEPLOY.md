# GitHub Pages 部署说明

本项目已配置好 Vite 和 GitHub Actions，推送到 GitHub 后可自动部署到 GitHub Pages。

## 已完成的配置

- `vite.config.js` 已设置 `base: './'`，适配 GitHub Pages 子路径部署。
- `.github/workflows/deploy.yml` 已配置自动构建和发布。
- `npm run build` 已验证通过。
- `npm run preview` 可本地预览生产包。

## 首次发布步骤

1. 在 GitHub 创建一个新仓库，例如 `wedding-invitation-demo`。
2. 在本地项目目录执行：

```bash
git init
git add .
git commit -m "init wedding invitation"
git branch -M main
git remote add origin https://github.com/你的用户名/wedding-invitation-demo.git
git push -u origin main
```

3. 打开 GitHub 仓库页面，进入：

```text
Settings → Pages
```

4. 在 `Build and deployment` 中选择：

```text
Source: GitHub Actions
```

5. 等待 `Actions` 页面中的 `Deploy to GitHub Pages` 工作流完成。

## 访问地址

部署完成后，地址通常是：

```text
https://你的用户名.github.io/wedding-invitation-demo/
```

如果仓库名不同，请把上面的 `wedding-invitation-demo` 替换成你的仓库名。

## 本地命令

```bash
npm install
npm run dev
npm run build
npm run preview
```
