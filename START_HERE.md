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

本地 `origin` 已指向自己的仓库 `Nuerjibieke/nuerjibieke.github.io`；`upstream` 指向模板作者，只用于保留来源。日常更新后提交并推送即可：

```sh
git add .
git commit -m "Update academic homepage"
git push origin main
```

浏览器登录 GitHub 与终端 Git 的推送凭据是两套状态；浏览器已登录，不代表终端已有推送权限。网页上传时也要包含隐藏目录 `.github`。

## 公开访客统计

2026-10-23 接入 Flag Counter 免费计数器，标识 `dFxI`，服务器为 `s05.flagcounter.com`。三语页面共用同一计数器，不分别创建。公开详情：`https://info.flagcounter.com/dFxI`。

- 以世界地图标记访客来源国家／地区，点击地图可查看各地区访客数。默认 24 小时内对重复访客去重；同一个人隔天仍可再次计入，因此不代表累计不同自然人数。
- Pageviews 是计数器图片加载次数，区别于去重访客数。图片缓存、拦截器和网络错误可能造成漏计；图片显示通常延迟约五分钟。
- IP 估算的是大致网络所在地区，VPN 或代理可能改变结果。没有接入 GPS 定位。
- 自启用时开始累计，无法补回之前未采集的访问；创建和验收过程产生的访问也会计入。
- 计数器图片为主动加载，保证未滚动至页底的访问也有机会被计入；通过 `referrerpolicy="no-referrer"` 避免发送页面地址。图片请求仍会向服务商发送访客 IP、浏览器等网络信息。隐私说明：`https://www.flagcounter.com/privacy.html`。
- 使用无邮箱注册模式，不提交邮箱或创建管理账户。公开详情页底部的 `Ignore this browser` 可排除当前浏览器自身访问。
- 使用官方 `map` 模式和 `size_xl`，按页面宽度自适应；保留原计数器标识 `dFxI`，继续累计既有数据。地图按国家／地区标记，不能当作访客的精确城市或地址。
- 按用户要求，公开页面只显示地图及计数器本身的统计，不展示统计时间、去重口径或 IP 估算的说明段落。这些维护信息仅保留在本文件中。

维护时保留三版中的相同标识。服务故障时原主页内容仍能正常显示。移除三版 `.visitor-stats` 区域即可停止向该服务发送新的图片请求。
