# Songtao Mao — 个人网站管理

- 主页：https://songtaomao.github.io/
- 仓库：https://github.com/SongtaoMao/songtaomao.github.io
- 发布配置：[GitHub Pages](https://github.com/SongtaoMao/songtaomao.github.io/settings/pages)，`main` 分支的根目录 `/`。
- 部署记录：[GitHub Actions](https://github.com/SongtaoMao/songtaomao.github.io/actions)。
- 技术：静态 HTML / CSS / JavaScript，无需安装依赖或本地构建。
- 操作前阅读 [AGENTS.md](AGENTS.md)；每轮结果写入 [RESULT.md](RESULT.md)。

## 编辑位置

| 文件 | 用途 |
| --- | --- |
| `index.html` | 简介、访问经历、论文、教学、联系方式；也含首页专用样式和 SEO 标签 |
| `assets/css/main.css` | 通用布局与响应式样式 |
| `assets/js/` | 导航与页面交互 |
| `images/Songtao.jpeg` | 个人照片 |
| `files/` | 网站链接的公开 PDF |
| `robots.txt` / `sitemap.xml` | 搜索引擎抓取与站点地图 |

## 日常编辑与发布

1. 在本仓库内检查 Git 根目录、远端、工作区和分支，再拉取最新远端状态；不要把其他项目的更改一起提交。
2. 默认先在 `codex/<任务名>` 分支修改并预览。每轮更新 `RESULT.md`，提交并推送该分支；推送预览分支不会更新生产主页。用户要求“仅本地”时遵从当轮指令。
3. 页面改动至少检查 HTML、资源路径、受影响的桌面/手机布局；检查 `git diff --check`。按改动范围验证，不为纯文档更新运行网站构建。
4. 用户明确要求发布时，将已确认版本同步到 `main`。若当轮已授权发布，无需再次询问。
5. 等待对应提交的 Pages 部署成功，再检查公开网址及关键内容。区分“代码已同步”和“线上已生效”。

`main` 是生产分支，推送通常会触发 Pages 部署。网站应保持上线时，仅管理文档的变更可以直接同步到 `main`，但同一提交不能夹带尚未确认的网页内容。停用期间，管理文档也推送到非生产分支，避免意外重新上线。

## 已确认的首页基线

以 2026-10-13 发布的 `21002e1` 为本次接手基线，后续按用户要求更新：

- 简介包含 UIUC 2025、Bocconi 2026 和 Fall 2026 Simons 访问经历及链接。
- 求职表述为寻找 starting in 2027 的 postdoctoral 或 other research positions。
- 12 篇论文；Abelian Cayley 列首，planted clique 标 SODA 2027，Batch LPN 标 TCC 2026。
- PASCAL 标注按贡献排序；保留其他作者排序说明及 Low-degree 贡献说明与 Hopkins 原始论文链接。
- 桌面照片高度 440px、向下偏移 36px；图标 42px；Email/图标块向上调整 24px；简介字号为原来的 90%。
- 保留 canonical、description、Search Console 验证标签、robots 和 sitemap。涉及内容更新时同步相关日期，勿把历史收录诊断当作当前结果。

这些是已确认状态，不是永久冻结内容；明确的新要求优先。

## 临时停用与恢复

“停用”沿用用户原意：公开网址不可访问 / 返回 404，不显示维护说明。只有用户要求停用时才执行。

停用前先保存当时最新内容，提交并推送，并创建带日期的恢复标签；记录完整提交 SHA、仓库名称和 Pages 配置。优先使用 GitHub Pages 的 **Unpublish site**，检查公开网址实际状态。该操作保留仓库内容与配置；后续新的部署会重新上线，因此停用期间不要触发生产部署。

恢复时使用停用前记录的最新版本，按记录恢复发布来源并创建新部署，再核对线上内容。不得默认恢复旧标签 `website-before-pause-20260825`：它只保存 2026 年 8 月版本，会遗漏之后的更新。

历史上曾通过临时改名仓库再关闭 Pages 完成停用；这是历史操作记录，不是日常默认步骤。

参考：[GitHub 官方停用与重新启用说明](https://docs.github.com/en/pages/getting-started-with-github-pages/unpublishing-a-github-pages-site)。

## 同步与运行范围

本仓库独立于周围目录所属的其他 Git 仓库。所有 Git 操作明确指定本仓库路径。当前管理副本在工作区的 `personal-website/` 中；旧位置只作历史副本，不并行编辑。

本地只做轻量编辑、状态检查、小型检查和必要预览。昂贵任务先推送脚本/config，再在 GitHub Codespaces 或 GitHub runner 执行；长时间本地 Python 任务需要用户明确允许。

本网站没有配置 Overleaf 远端。若未来从 CV / 论文项目更新 PDF，先确认源项目、导出文件与网站引用，再分别记录实际完成的同步；不得宣称未配置的 Overleaf 同步已完成。
