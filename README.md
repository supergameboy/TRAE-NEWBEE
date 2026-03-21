# TRAE-NEWBEE 项目

这个项目是一个日常经验集合，包含了常用的技能、智能体和其他工具，用于扩展 AI 助手的功能。

## 项目结构

```
TRAE-NEWBEE/
├── skills/              # 技能模块目录
│   ├── frontend-ui-test/               # 前端界面操作测试
│   ├── full-review-repair/             # 全维度代码审查与修复
│   ├── auto-task-experience-summarizer/ # 自动任务经验总结器
│   └── README.md       # 技能模块文档
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

详细的技能说明请查看 [skills/README.md](./skills/README.md)。

## 最近更新

- 添加测试工作流管理规则文档
- 明确主Agent与子Agent在测试流程中的职责分工和操作规范
- 注意：禁用了playwright编写测试脚本

## 环境说明

- 我使用的是国服，国际服需要按需调整
- 技能模块的详细文档在 `skills/README.md`
