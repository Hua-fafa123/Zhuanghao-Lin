# 个人主页维护

首页沿用此仓库的 Jekyll / GitHub Pages 部署方式，无需另外的托管服务。

- `_pages/about.md`：首页全部内容。页面明确设置 `layout: null`，避免套入旧版主题；`permalink: /` 保持首页地址。
- `assets/css/academic-home.css`：双栏布局、配色和手机端样式。
- `assets/js/academic-home.js`：中英文切换。
- `_config.yml`：全站姓名及社交账号。

修改双语文字时，同步更新对应元素的 `data-zh`、`data-en` 以及元素内的默认中文。未提供的学校、照片、研究方向、论文等均明确标为待补充，没有引用他人的学术成果。参考设计：https://mommqq.github.io/guojunxu/ 。

照片准备好后，可将首页的 `.portrait` 占位内容替换为图片，并使用 Jekyll 的 `relative_url` 过滤器生成图片路径。

仓库中旧模板的示例文章和其他页面仍保留，首页没有链接到这些示例；发布个人成果前应自行替换相应示例。

现有 `.github/workflows/jekyll.yml` 在推送到 `master` 后构建部署。仓库 Settings → Pages 应选择 GitHub Actions 作为来源。
