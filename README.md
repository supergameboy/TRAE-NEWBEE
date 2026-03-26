# TRAE-NEWBEE 项目

这个项目是一个日常经验集合，包含了常用的技能、智能体和其他工具，用于扩展 AI 助手的功能。

## 项目结构

```
TRAE-NEWBEE/
├── skills/              # 技能模块目录
│   ├── frontend-ui-test/               # 前端界面操作测试
│   ├── full-review-repair/             # 全维度代码审查与修复
│   ├── auto-task-experience-summarizer/ # 自动任务经验总结器
│   ├── brainstorm/                     # 头脑风暴技能
│   ├── bug-hunter-fractal/             # 分形式问题排查技能
│   ├── fractal-designer/               # 分形式设计器
│   ├── full-review-repair-fractal/     # 分形式全维度代码审查与修复
│   ├── graph-theory-fractal/           # 分形式图论分析技能
│   ├── knowledge-fractal/              # 分形式知识体系构建技能
│   ├── refactor-fractal/               # 分形式代码重构技能
│   ├── requirements-fractal/           # 分形式需求分析技能
│   ├── task-scheduler-fractal/         # 分形式项目任务规划器
│   ├── test-design-fractal/            # 分形式测试用例设计技能
│   └── README.md                       # 技能模块文档
├── docs/                # 文档目录
└── README.md            # 项目根文档
```

## 技能模块

项目包含以下技能模块：

### 测试类

1. **frontend-ui-test** - 前端界面操作测试
   - 启动前端服务器、访问页面、截图、点击按钮等操作测试
   - 需要使用能添加图片的多模态模型

2. **test-design-fractal** - 分形式测试用例设计
   - 从测试目标开始，逐步细化设计测试用例
   - 每个决策点都询问用户，确保测试覆盖全面

### 审查类

3. **full-review-repair** - 全维度代码审查与修复
   - 执行完整的项目代码审查、修复和测试流程
   - 包括后端、数据库、前端和UI的全面评估

4. **full-review-repair-fractal** - 分形式全维度代码审查与修复
   - 从宏观到微观逐步深入执行代码审查、修复和测试
   - 每个审查层级都遵循自相似模式，确保全面性和深度

### 问题排查类

5. **bug-hunter-fractal** - 分形式问题排查
   - 采用分形递归思想，从现象到根源层层定位问题
   - 每个决策点都询问用户，每一步都保存到文档

### 设计类

6. **fractal-designer** - 分形式设计器
   - 从用户初步想法开始，逐步细化为可落地的设计方案
   - 生成完善的标准设计文档集

### 需求类

7. **requirements-fractal** - 分形式需求分析
   - 从用户初步想法开始，逐步细化为可落地的需求文档
   - 每个决策点都询问用户，确保需求准确完整

### 规划类

8. **task-scheduler-fractal** - 分形式项目任务规划器
   - 制定详细、可执行的项目任务计划文档
   - 支持A/B组并行开发模式

### 重构类

9. **refactor-fractal** - 分形式代码重构
   - 从重构目标开始，逐步细化制定重构计划并执行
   - 每个决策点都询问用户，确保重构方向正确

### 分析类

10. **graph-theory-fractal** - 分形式图论分析
    - 结合分形递归思想和图论思想分析系统/模块
    - 识别节点、定义边、分析图结构、提出优化建议

### 知识类

11. **knowledge-fractal** - 分形式知识体系构建
    - 从知识主题开始，逐步细化构建知识体系
    - 可用于写帮助文档或总结 achievement

### 经验类

12. **auto-task-experience-summarizer** - 自动任务经验总结器
    - 自动读取与总结任务执行经验
    - 记录关键步骤、问题及解决方案、优化建议等

### 决策类

13. **brainstorm** - 头脑风暴
    - 处理问题、BUG时进行头脑风暴
    - 收集各Agent的专业意见，整合多个可行方案

### 工具类

14. **skill-creator** - 技能创建器
    - 用于创建新的技能模块

详细的技能说明请查看 [skills/README.md](./skills/README.md)。

## 核心设计思想

### 分形递归思想

本项目中多个技能采用**分形递归思想**作为核心设计理念：

- **纵向细分**：从宏观到微观，逐层深入（L0→L1→L2→L3→L4）
- **横向拆分**：同一层级内拆分为多个并行任务，提高效率
- **自相似模式**：每个层级都遵循相同的工作模式，降低认知负担
- **用户决策**：每个决策点都询问用户，确保方向正确

### 双维度分形模型

```
纵向细分（深度）
    ↓
L0 宏观级
   ├── [横向拆分] 方向A（并行）
   ├── [横向拆分] 方向B（并行）  ← 横向拆分（广度）
   └── [横向拆分] 方向C（并行）
   ↓
L1 中观级
   ↓
L2 微观级
   ↓
L3 原子级
   ↓
L4 可选深度
```

## 技能分类

### 按功能分类

| 分类 | 技能名称 | 说明 |
|------|---------|------|
| **测试类** | frontend-ui-test | 前端界面操作测试 |
| **测试类** | test-design-fractal | 测试用例设计 |
| **审查类** | full-review-repair | 全维度代码审查与修复 |
| **审查类** | full-review-repair-fractal | 分形式全维度代码审查与修复 |
| **问题排查类** | bug-hunter-fractal | 分形式问题排查 |
| **设计类** | fractal-designer | 分形式设计器 |
| **需求类** | requirements-fractal | 分形式需求分析 |
| **规划类** | task-scheduler-fractal | 分形式项目任务规划 |
| **重构类** | refactor-fractal | 分形式代码重构 |
| **分析类** | graph-theory-fractal | 分形式图论分析 |
| **知识类** | knowledge-fractal | 分形式知识体系构建 |
| **经验类** | auto-task-experience-summarizer | 自动任务经验总结 |
| **决策类** | brainstorm | 头脑风暴 |
| **工具类** | skill-creator | 技能创建器 |

### 按复杂度分类

| 复杂度 | 技能名称 | 说明 |
|--------|---------|------|
| **简单** | frontend-ui-test | 单一功能，流程固定 |
| **简单** | auto-task-experience-summarizer | 自动化流程 |
| **简单** | skill-creator | 工具类技能 |
| **中等** | full-review-repair | 多阶段流程 |
| **中等** | brainstorm | 多方案整合 |
| **复杂** | bug-hunter-fractal | 分形递归，多层级 |
| **复杂** | fractal-designer | 分形递归，多层级 |
| **复杂** | full-review-repair-fractal | 分形递归，多层级 |
| **复杂** | graph-theory-fractal | 分形递归，多层级 |
| **复杂** | knowledge-fractal | 分形递归，多层级 |
| **复杂** | refactor-fractal | 分形递归，多层级 |
| **复杂** | requirements-fractal | 分形递归，多层级 |
| **复杂** | task-scheduler-fractal | 分形递归，多层级 |
| **复杂** | test-design-fractal | 分形递归，多层级 |

## 最近更新

- 添加 skill-creator 技能创建器
- 完善所有分形式技能的横向拆分机制
- 统一技能文档格式和结构
- 添加技能分类说明
- 添加核心设计思想说明

## 环境说明

- 我使用的是国服，国际服需要按需调整
- 技能模块的详细文档在 `skills/README.md`
