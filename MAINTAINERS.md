# 维护手册

本仓库按「发现 → 初筛 → 审查 → 收录 → 记录」管线维护。投稿者请先读[贡献指南](CONTRIBUTING.md)；本文档面向维护者，描述管线细节与既有约定。

## 1. 发现

GitHub 搜索关键词库（每轮按需组合，`sort=stars` 与 `sort=updated` 各扫一遍）：

- 形象词：`大肥鱼`、`dafeiyu`、`鲸鱼娘`、`whale-girl`、`deepseek-chan`、`deepseek 娘`、`蓝鲸`
- 话题：`topic:whale-girl`、`topic:dafeiyu`
- 生态词：`dsh` + 能力/平台名——`qq`、`wechat`、`微信`、`lark`、`飞书`、`telegram`、`bilibili`、`贴吧`、`小红书`、`douyin`、`直播`、`voice`、`tts`、`唱歌`、`翻唱`、`好感度`、`日记`、`朋友圈`、`换装`、`养鱼`、`gacha`、`拟人`、`companion`、`pet`、`persona`、`live2d`
- 外围源：DeepSeek Harness 仓库 Discussions、ruanyf/weekly 自荐帖、上游清单（awesome-dsh-plugin 等）的更新动态。

## 2. 初筛（三条硬线）

1. **相关性**：与鲸鱼娘生态直接相关，或明确服务于角色项目；纯通用、无角色元素的工具有星也不收（先例：知乎搜索 CLI、通用配色主题、usewhale/Whale）。
2. **范围**：任何合法平台均可（QQ、微信、飞书、B 站、贴吧、小红书、抖音、Telegram 等），活动须合法合规。
3. **星数**：参考信号而非门槛——低星但实现扎实可收（先例：dsh-dafeiyu-life，14 星 / 609 文件 / 301 测试），高星但离题不收。

## 3. 审查（只读代码审查）

- **方式**：只读，不下载、不安装、不运行。读文件树（git trees API）、清单（package.json / `dsh.bundle` / exports）、入口与核心源码抽样（头 / 中 / 尾）。
- **代码类标准**：入口、清单、依赖声明互相吻合；核心逻辑完整——无大面积截断、无引用不存在的文件、无未定义调用、无空壳实现。
- **资产类标准**（表情包 / 模型 / 图标）：资产文件真实存在、数量与体积合理、附使用说明；授权不明标「授权待核实」（先例：deepseek-whale-girl-icon）。
- **人设/配置类标准**：提示词与配置实质完整，几行占位不收。
- **结论三分**：PASS（收录）/ BORDERLINE（收录并补标注，或入观察名单）/ FAIL（不收录）。审查可由维护者的自动化代理执行，结论写入 README 脚注。

## 4. 收录与记录

- 条目格式见[贡献指南](CONTRIBUTING.md)；不手写星数与时效信息。
- 每轮更新在 README 脚注追加一行日期记录（新增 / 移动 / 更名 / 审查结论）。
- 提交信息用 conventional 风格（`docs: ...`）。
- 仓库迁移或改名：核实后更新链接（先例：dsh-aurabot-qq → aureth-labs）。

## 5. 观察名单（养一养再收）

- 网易云听歌小簇（ncm-player、dsh-MusicPlayer 等，2–5 星）：涨起来后归入「语音与歌声」邻近分类。
- 微博方向小件（weibo-wallpaper-dsh-plugin 等，1–2 星）。
- dsh-plugin-moments：代码完整但 2026-08 后无维护；长期无更新则考虑移除。
- Dsh_douyin、ai-biaoqingbao：实现通过审查但无正式 LICENSE，关注授权补充情况。
- wytyKen/dsh-whale-life：维护者本人规划中的项目，待其示意、基本成熟后再收录。

## 6. 既有约定

- 收录范围于 2026-11-06 放宽至任意合法平台，分类「B 站生活与内容理解」相应更名为「平台生活与内容理解」。
- 本清单是策展清单，不满足 awesome-dsh-plugin 的插件收录条件（需 `dsh.bundle` 清单与 `dsh-plugin` 话题）；那条路线属于未来的插件类项目，清单自身走「榜上榜」（已收录于 awesome-deepseek-harness）。
