# Product Teardown Skill

从市场、商业、用户、技术、模型与数据基础层六个维度系统拆解数字产品和 AI 产品。

## 文件位置

Skill 主目录：`~/Desktop/skill/product-teardown/`

核心文件：

- `SKILL.md`：触发条件和执行流程
- `references/six-layer-framework.md`：六层分析细则
- `references/report-template.md`：报告结构模板
- `agents/openai.yaml`：Codex 界面元数据

## 安装到 Codex

当前文件保存在桌面，便于查看和修改，但不会自动成为全局 Skill。需要启用时执行：

```bash
cp -R ~/Desktop/skill/product-teardown ~/.codex/skills/product-teardown
```

如果目标目录已经存在，请先确认是否需要覆盖，避免丢失旧版本。安装完成后重新开启 Codex 会话，使 Skill 被发现。

## 调用方式

显式调用最稳定：

```text
使用 $product-teardown 深度拆解 Perplexity，重点分析商业、模型和数据壁垒。
```

也可以自然语言触发：

```text
帮我从市场、商业、用户、技术、模型和数据六层拆解 Notion AI。
```

```text
对这个产品做一份标准产品拆解：https://example.com
```

```text
快速比较产品 A 和产品 B，重点看用户价值与商业模式。
```

## 分析深度

- `quick`：适合快速了解产品和会议讨论。
- `standard`：默认，输出完整六层报告。
- `deep`：适合竞品研究、产品战略或投资初研，会增加竞品、反证和待验证假设。

示例：

```text
使用 $product-teardown，以 deep 模式拆解 Cursor，市场范围限定为中国和北美，资料截至今天。
```

## 建议提供的信息

- 产品名称、网址、代码仓库或相关文档
- 分析目的，例如竞品研究、立项、投资或复盘
- 目标市场和时间范围
- 最关心的层级
- 期望深度和输出篇幅

信息不足时，Skill 会根据公开资料分析，并把无法验证的内容标记为“未知”或“推断”。

## 来源

该 Skill 参考并改造自 MIT 许可的 [daymade/claude-code-skills：product-analysis](https://github.com/daymade/claude-code-skills/tree/main/product-analysis)，新增市场、商业、模型和数据基础层，并调整为通用产品与 AI 产品拆解工作流。
