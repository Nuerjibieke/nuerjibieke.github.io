# Nuerjibieke 的学术主页

本项目使用 [Minimal Light](https://github.com/yaoyao-liu/minimal-light) 官方提供的 HTML 版本，保留模板布局、配色和响应式样式，无需安装 Ruby 或前端依赖。

- 模板版本：`1ea07f39518ac44644406380c83da6f89037c4fc`。
- 原模板许可证保留在 `LICENSE`。
- 姓名、学校、研究方向、论文和经历均明确标为待填写；GitHub 账号由本人提供。
- 当前页面已移除模板作者的论文、经历、默认 Google Analytics 和演示站 canonical 链接。

## 本地预览

在项目目录运行：

```sh
python3 -m http.server 4173 --bind 127.0.0.1 --directory html_source_file
```

打开 `http://127.0.0.1:4173` 查看英文版，`/zh/` 查看中文版，`/kk/` 查看哈萨克语版（西里尔字母，按用户选择）。左侧 EN / 中文 / Қазақша 可切换。按 Ctrl+C 停止预览。

## 修改内容

- 英文版内容：`html_source_file/index.html`
- 中文版内容：`html_source_file/zh/index.html`
- 哈萨克语版内容：`html_source_file/kk/index.html`
- 头像与论文配图：`html_source_file/assets/img/`
- 本次样式补充：`html_source_file/assets/css/custom.css`
- 原始模板样式：`html_source_file/assets/css/style.css`、`publications.css`

仓库根目录的 `_config.yml`、`index.md` 等是上游保留的 Jekyll 版本，**本次 HTML 部署不使用这些文件**，无需同时维护两套内容。

暂无真实链接的论文按钮已禁用。提供链接后，改为带真实 href 的 a 标签即可。三版为独立静态页面，内容修改时需同步翻译。正式内容确认后，删除三版中的预览提示和 `noindex, nofollow` 标签以允许搜索引擎收录。

## 发布到 GitHub Pages

推荐仓库名：`Nuerjibieke/nuerjibieke.github.io`。

1. 在自己的 GitHub 账号下创建公开仓库 `nuerjibieke.github.io`，上传当前项目文件，包含 `.github/workflows/pages.yml`。
2. 打开仓库 **Settings → Pages → Build and deployment → Source**，选择 **GitHub Actions**。
3. 在 **Actions** 中运行 `Deploy academic homepage`，或向 `main` 分支提交一次修改。
4. 部署成功后，访问 `https://nuerjibieke.github.io/`。

部署文件已准备好，会直接发布 `html_source_file`。以后提交到 `main` 即会自动更新。

当前本地克隆的 origin 指向模板作者的仓库，仅记录来源。创建自己的仓库后，先改为自己的地址再推送：

```sh
git remote set-url origin https://github.com/Nuerjibieke/nuerjibieke.github.io.git
git add .
git commit -m "Set up academic homepage from Minimal Light"
git push -u origin main
```

浏览器登录 GitHub 与终端 Git 的推送凭据是两套状态；浏览器已登录，不代表终端已有推送权限。网页上传时也要包含隐藏目录 `.github`。
