# novelist

玄幻小说写作工具集 —— 从世界观构建、剧情规划到正文写作的深度协作 workflow。

## 包含的 Skill

| Skill | 用途 | 触发方式 |
|-------|------|----------|
| **xuanhuan-planning** | 世界观构建、修炼体系设计、势力分布、人物设定、三层剧情规划（长期/中期/短期） | "写玄幻小说"、"开新书"、"设定世界观"、"修炼体系"、"剧情规划" |
| **xuanhuan-writing** | 写前确认 → 逐批写 2-3 章 → 人工审阅 → 修正影响分析 → 循环 | "写正文"、"写第 X 章"、"继续写"、"推进剧情" |

## 安装方式

### 方式一：通过插件市场安装

1. 打开 Claude Code，按 `Ctrl+S` 打开 `settings.json`

2. 在 `extraKnownMarketplaces` 中加入：

```json
"novelist": {
  "source": {
    "source": "github",
    "repo": "niki-longevity/novelist"
  }
}
```

完整示例：

```json
{
  "extraKnownMarketplaces": {
    "novelist": {
      "source": {
        "source": "github",
        "repo": "niki-longevity/novelist"
      }
    }
  }
}
```

3. 重启 Claude Code

4. 执行 `/plugin`，在列表中找到 **novelist** 市场，安装 `novelist` 插件

5. 执行 `/reload-plugins`，即可使用

### 方式二：通过 CLI 直接安装

```bash
claude plugin install novelist@novelist
```

> 注意：依旧需要先在 `settings.json` 中配置 `extraKnownMarketplaces`。

## 使用方式

安装后，直接对 Claude Code 说：

```
我要写一本玄幻小说
```

AI 会自动触发 `xuanhuan-planning` skill，引导你一步步完成世界观构建。

当规划完成，说"开始写第一章"，AI 会自动切换到 `xuanhuan-writing` skill 开始写正文。

## 协作理念

- **深度协作，不可独断**：AI 不替你拍板，每一个关键决策都由你确认
- **小步快跑，频繁确认**：每次只写 2-3 章，写完由你审阅
- **规划可修正**：设定和剧情规划不是一开始定死的，可在过程中随时调整
