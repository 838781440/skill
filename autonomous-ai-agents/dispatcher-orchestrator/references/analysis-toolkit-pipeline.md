# ⚠️ 此文件已迁移
#
此文档已提升为共享流水线文档，位于 utonomous-ai-agents/analysis-toolkit-pipeline.md。
# prism、pressure-test、grill-me 三个 skill 均引用共享版本。
# 本文件保留为历史参考，不再更新。

---

# 分析工具包流水线

Dispatcher 在接到需要**深度分析+验证+查漏**的任务时，按此流水线调度：

## 三件套职责

| 工具 | 干什么 | 什么时候用 |
|:----|:------|:----------|
| 🧠 **prism-***（深度分析） | 从多个角度解剖一个东西的结构化分析 | 需要理解事物的结构、维度、盲区时优先用 |
| 🔧 **pressure-test v2.0**（压力测试） | 用数据+逻辑找短板，技术方案/商业想法/人生决策都能压 | 方案/想法/决策需要验证是否靠谱时用 |
| 🔥 **grill-me**（拷问/追问） | 一个问题追一个问题，走完所有分支直到挖出所有隐藏问题 | 已经有结论，需要深层查漏/自我挑刺时用 |

## 推荐流程

```
prism 先分析清楚结构
    ↓
pressure-test 用数据验证短板
    ↓
grill-me 追问到所有隐藏假设都暴露
```

## 组合场景

| 用户请求 | 调度建议 |
|:--------|:--------|
| "分析一下 XX" | prism-discover → prism-scan → prism-full |
| "验证 XX 靠不靠谱" | pressure-test（直接压力测试） |
| "帮我看看 XX 有什么问题" | prism-scan → pressure-test |
| "深度分析 XX" | prism-full → pressure-test → grill-me |
| "审视一下这个方案" | grill-me → 发现漏洞后 → pressure-test 验证 |
| "全方位分析 XX" | prism-discover → prism-full → pressure-test → grill-me |

## 注意事项

- prism 是**分析类**（结构/角度/维度），不涉及外部数据
- pressure-test 是**验证类**（数据优先+逻辑辅助），可能调工具
- grill-me 是**拷问类**（纯逻辑追问），不调工具
- 三个可以独立使用，也可以串联使用
