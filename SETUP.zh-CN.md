# 修改与部署

## 1. 核对个人信息

已填写 Ruihong Mai、BITZH、Data Science and Big Data Technology、RuihongMai 和 mairuihong666@gmail.com。就读日期尚待补充。

修改 `_config.yml` 的 `first_name`、`last_name` 和 `url`。英文名没有固定拆分要求，可将完整名字填入 `first_name`，并将 `last_name` 留空。网站标题使用 `title: blank` 时自动显示姓名。

个人站点配置：

```yaml
url: https://RuihongMai.github.io
baseurl: ''
```

在 `_data/profile.yml` 填入学校、专业、日期、GitHub 用户名和邮箱。项目链接写在对应 `_projects/*.md` 的 `repository_url` 中。没有真实链接时保留空字符串。

如需头像，在 `assets/img/` 放入自己的照片，并将 `_pages/about.md` 的 `profile: false` 改为：

```yaml
profile:
  align: right
  image: profile.jpg
  image_circular: false
```

PDF 可放在 `assets/pdf/`，然后在 `_data/profile.yml` 填入 `resume_pdf: /assets/pdf/resume.pdf` 或 `thesis_pdf: /assets/pdf/thesis.pdf`。当前未附虚构简历或论文 PDF，CV 页面本身可直接阅读。

## 2. 建立自己的 GitHub 仓库

创建空仓库 `RuihongMai.github.io`。不要初始化 README。将本文件所在的整个 academic-homepage 文件夹作为仓库根目录，不要把它再套进一层目录。

在此目录打开终端运行：

```sh
git init -b main
git add .
git commit -m "Create academic homepage"
git remote add origin https://github.com/RuihongMai/RuihongMai.github.io.git
git push -u origin main
```

推荐终端推送，以确保 `.github/workflows/deploy.yml` 等隐藏目录被包含。

## 3. 开启 Pages

仓库 Settings → Pages → Build and deployment → Source 选择 **GitHub Actions**。
在 Actions 中运行 `Build and deploy academic homepage`，或再次推送 main。
工作流成功后访问 `https://RuihongMai.github.io`。

这份定制仓库使用官方 Pages 部署动作，因此选择 GitHub Actions，不使用上游旧教程里的 gh-pages 分支模式。

如果使用普通项目仓库，例如 `portfolio`，保留上面的 url，并设置 `baseurl: /portfolio`；地址为 `https://RuihongMai.github.io/portfolio/`。

## 4. 后续维护

个人介绍修改 `_pages/about.md`；论文摘要修改 `_pages/research.md`；项目细节修改 `_projects/`。页面链接使用 relative_url，兼容根域名和项目子目录。

发布前核对 CONTENT_CHECKLIST.md。当前环境未安装 Ruby / Docker，尚未实际执行 Jekyll 构建或浏览器视觉验收；以首次 Actions 构建结果为准。如失败，在 Actions 打开 Build site 查看错误日志。
