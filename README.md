# A6y55 的个人主页

原生 HTML / CSS 单页。没有构建步骤、JavaScript 运行时依赖、第三方字体或访问统计。页面内容直接保存在 HTML 中。

## 文件结构

```text
index.html          个人简介、研究经历、外部链接和页面元信息
assets/style.css    排版、配色、移动端与打印样式
assets/favicon.svg  站点图标
.nojekyll           禁用 GitHub Pages 的 Jekyll 处理
```

## 本地预览

直接用浏览器打开 `index.html`，或在仓库根目录运行：

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

浏览器访问 `http://127.0.0.1:8000`。预览后使用 `Ctrl+C` 停止服务。

## 日常维护

- 修改简介：编辑 `index.html` 中的 `#about` 区域。
- 正文使用第一人称，直接介绍工作和经历；来源通过链接提供，核验说明留在本文档。
- 公开身份统一使用 A6y55，页面、元信息和 Git 提交均不使用真实姓名或私人邮箱。
- 添加经历：在 `#work .experience-grid` 中复制一个 `article.experience-card`，填写项目名称、实际年份、工作内容和可核验的来源链接。
- 更新联系信息：编辑 `#contact`。公开邮箱需要本人确认后再添加。
- 修改配色和字体：编辑 `assets/style.css` 顶部的 `:root`。
- 修改名字或域名：同时更新页面标题、描述、canonical 和 Open Graph 元信息。
- 新增项目、论文、CVE、奖项时，只记录已确认的信息。未公开的漏洞细节不写入主页。

目前只有个人简介和少量经历，直接维护 HTML 即可。需要持续发布多篇文章时，再评估引入基于 Markdown 的静态站点生成器。

## 内容依据

以下来源于 2026-09-17 核对：

| 条目 | 依据与表述范围 |
| --- | --- |
| 研究致谢 | [Kamailio Credits](https://github.com/kamailio/kamailio-credits#credits) 列出 A6y55，年份 2026，Scope 为 Security，工作描述为 Vulnerability research and fuzzing。主页未据此推定 CVE 编号、漏洞数量或严重等级。 |
| SUS 战队经历 | [SUS 关于页面](https://seusus.com/about/) 的 SUS@2025 名录列出 a6y55，方向为 Reverse/PWN。2025 仅表示公开名录版本，不表示加入或离队时间。 |
| 核心成员身份 | 由本人提供；SUS 公开名录确认成员与方向，但未标注“核心成员”职务。 |
| 东南大学背景 | Kamailio Credits 和 [GitHub 公开资料](https://github.com/A6y55) 均列有 Southeast University。主页未推定学历、年级或毕业时间。 |

## GitHub Pages 部署

仓库名保持为 `A6y55.github.io`。在 GitHub 仓库的 **Settings → Pages → Build and deployment** 中设置：

- **Source**：Deploy from a branch
- **Branch**：`main`
- **Folder**：`/ (root)`

提交并推送主页文件后，GitHub Pages 从根目录发布站点。`.nojekyll` 让这些静态文件跳过 Jekyll 处理，不需要额外的 Actions 工作流。

参考：[配置发布来源](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)、[创建 GitHub Pages 站点](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)。
