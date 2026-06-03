# Gene Skill

一个用于生成人格基因组 `GENOME.md` 的方法论仓库。

它把一个人物或概念视为可被“测序”的系统，围绕六条染色体、双链提取协议和表观遗传层，生成一份既可阅读、也可被 AI 直接加载使用的人格文件。

## 这是什么

这个项目不是传统意义上的应用程序，而是一套面向 AI Agent 的人格建模 skill。

核心产物是 `GENOME.md`：

- 它是结构化的人格基因组文档
- 它定义了认知、情绪、关系、叙事、时间、阴影六条染色体
- 它包含“表层链 + 深层链”的双链提取结果
- 它可以作为角色扮演、思维顾问、分析视角切换的运行载体

仓库当前主要包含：

- `SKILL.md`：主 skill 定义与完整工作流
- `references/`：提取协议、创建算法、模板、伦理边界
- `examples/`：示例基因组与研究材料

## 能做什么

项目支持三类核心操作：

1. `Clone`
从真实人物出发，基于公开资料或用户提供素材，生成其人格基因组。

2. `Evolve`
在已有 `GENOME.md` 的基础上，结合新信息做增量更新。

3. `Create`
从多个基因组、概念描述或两者混合中，创造一个新的人格实体。

适合的使用场景包括：

- 构建“某人会如何思考”的 AI 顾问
- 把人物研究沉淀为统一结构
- 合并多种思维风格生成复合人格
- 为角色扮演、对话系统、写作陪练提供人格底座

## 核心设计

### 1. 六条染色体

- `Chr-1 认知`：心智模型、决策启发式、信念强度
- `Chr-2 情绪`：基线情绪、触发器、调节策略、应激模式
- `Chr-3 关系`：角色映射、权力偏好、信任与边界
- `Chr-4 叙事`：核心神话、语言指纹、自我叙事
- `Chr-5 时间`：跃迁事件、进化轨迹、当前向量、预测方向
- `Chr-6 阴影`：盲区、防御机制、未表达潜能

### 2. 双链提取

项目不只记录“他说了什么”，还同步提取“他为什么这样说”。

- `表层链`：公开言论、行为、立场、表达
- `深层链`：驱动力、恐惧、防御、未说出的假设

这套协议定义在 [references/extraction-protocol.md](references/extraction-protocol.md)。

### 3. 多源研究

`Clone` 路径默认会将研究拆成 8 个并行维度，包括：

- 著作
- 对话
- 表达 DNA
- 他者视角
- 决策记录
- 时间线
- 情绪模式
- 关系模式

每一路最终沉淀到 `references/research/0X-*.md`，再进入综合提取阶段。

### 4. 可运行人格文件

最终生成的 `GENOME.md` 不只是档案，还包含：

- 角色扮演规则
- 回答工作流
- 情境激活逻辑
- 面向 AI 的使用说明

模板位于 [references/genome-template.md](references/genome-template.md)。

## 仓库结构

```text
gene-skill/
├── README.md
├── SKILL.md
├── references/
│   ├── creation-algorithm.md
│   ├── ethics-boundary.md
│   ├── extraction-protocol.md
│   └── genome-template.md
└── examples/
    └── qin-shi-huang-genome/
        ├── GENOME.md
        └── references/
            └── research/
```

## 如何阅读这个项目

建议按这个顺序：

1. 先看 [SKILL.md](SKILL.md)
理解完整工作流、三种操作路由和产出标准。

2. 再看 [references/extraction-protocol.md](references/extraction-protocol.md)
理解“双链提取”为什么是这个项目的核心差异。

3. 接着看 [references/creation-algorithm.md](references/creation-algorithm.md)
如果你关心多人格融合、加权合并、概念造人，这里是关键。

4. 最后看示例 [examples/qin-shi-huang-genome/GENOME.md](examples/qin-shi-huang-genome/GENOME.md)
这是目前最直观的完整输出样例。

## 一个典型产出流程

以 `Clone` 为例，流程大致是：

1. 确认对象、用途、是否已有基因组、是否有本地语料
2. 创建目标目录与 8 份研究文件
3. 多源并行调研，保留来源、可信度和矛盾
4. 按双链协议提取六条染色体
5. 依据模板组装 `GENOME.md`
6. 对阴影染色体进行伦理边界检查

相关规则分别定义在：

- [SKILL.md](SKILL.md)
- [references/extraction-protocol.md](references/extraction-protocol.md)
- [references/ethics-boundary.md](references/ethics-boundary.md)

## 示例

当前仓库附带了一个完整样例：

- [examples/qin-shi-huang-genome/GENOME.md](examples/qin-shi-huang-genome/GENOME.md)

这个示例展示了：

- 历史人物如何被编码为人格基因组
- 六条染色体如何落地成结构化内容
- 角色扮演规则如何嵌入最终文档
- 元信息、研究逻辑、表达风格如何整合为一个可运行人格

## 边界与注意事项

这个项目尤其强调 `Chr-6 阴影染色体` 的使用边界。

- 阴影信息属于推断，不是事实
- 对活人必须控制置信度与措辞
- 不应用于攻击、操纵或未经请求的暴露
- 对用户本人测序时，需要额外的知情确认

详见 [references/ethics-boundary.md](references/ethics-boundary.md)。

## 适合谁

这个仓库更适合以下人群：

- 想把人物研究产品化为 AI 可运行结构的人
- 在做角色系统、顾问系统、人格化 Agent 的人
- 希望用统一模板沉淀“某人是如何思考的”的研究者
- 想探索“人物建模 + prompt/skill 设计”结合方式的开发者

如果你期待的是一个现成可启动的 Web 服务或 CLI 程序，这个仓库当前不是那种形态；它更像一套可复用的方法、协议和产物模板。
