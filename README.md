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
│   └── README.md                       # 技能模块文档
├── docs/                # 文档目录
└── README.md            # 项目根文档
```

## 技能模块

项目包含以下技能模块：

1. **frontend-ui-test** - 前端界面操作测试
   - 启动前端服务器、访问页面、截图、点击按钮等操作测试
   - 需要使用能添加图片的多模态模型

2. **full-review-repair** - 全维度代码审查与修复
   - 执行完整的项目代码审查、修复和测试流程
   - 包括后端、数据库、前端和UI的全面评估

3. **auto-task-experience-summarizer** - 自动任务经验总结器
   - 自动读取与总结任务执行经验
   - 记录关键步骤、问题及解决方案、优化建议等

4. **brainstorm** - 头脑风暴技能
   - 处理问题、BUG时进行头脑风暴
   - 收集各Agent的专业意见，整合多个可行方案

5. **bug-hunter-fractal** - 分形式问题排查技能
   - 采用分形递归思想，从现象到根源层层定位问题
   - 每个决策点都询问用户，每一步都保存到文档

6. **fractal-designer** - 分形式设计器
   - 从用户初步想法开始，逐步细化为可落地的设计方案
   - 每个技术分叉点都询问用户，确保设计符合预期

7. **full-review-repair-fractal** - 分形式全维度代码审查与修复
   - 从宏观到微观逐步深入执行代码审查、修复和测试
   - 每个审查层级都遵循自相似模式，确保全面性和深度

8. **graph-theory-fractal** - 分形式图论分析技能
   - 结合分形递归思想和图论思想分析系统/模块
   - 识别节点、定义边、分析图结构、提出优化建议

9. **knowledge-fractal** - 分形式知识体系构建技能
   - 从知识主题开始，逐步细化构建知识体系
   - 可用于写帮助文档或总结 achievement

10. **refactor-fractal** - 分形式代码重构技能
    - 从重构目标开始，逐步细化制定重构计划并执行
    - 每个决策点都询问用户，确保重构方向正确

11. **requirements-fractal** - 分形式需求分析技能
    - 从用户初步想法开始，逐步细化为可落地的需求文档
    - 每个决策点都询问用户，确保需求准确完整

12. **task-scheduler-fractal** - 分形式项目任务规划器
    - 制定详细、可执行的项目任务计划文档
    - 采用分批次读取策略，解决文档过多的问题

详细的技能说明请查看 [skills/README.md](./skills/README.md)。

## 最近更新

- 添加测试工作流管理规则文档
- 明确主Agent与子Agent在测试流程中的职责分工和操作规范
- 注意：禁用了playwright编写测试脚本

## 环境说明

- 我使用的是国服，国际服需要按需调整
- 技能模块的详细文档在 `skills/README.md`
