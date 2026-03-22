# Skills 技能目录

本目录包含项目中使用的自定义技能模块，用于扩展 AI 助手的功能。

## 技能列表

### 1. frontend-ui-test - 前端界面操作测试

**功能说明**：此技能用于进行前端界面操作测试，包括：
- 启动前端开发服务器
- 使用浏览器访问页面
- 截取页面截图
- 读取截图内容
- 点击页面元素（按钮等）
- 对比操作前后的变化

**使用场景**：当用户需要测试前端 UI 功能或执行浏览器交互操作时调用。

**详细文档**：[frontend-ui-test/SKILL.md](./frontend-ui-test/SKILL.md)

**注意**：需要使用能添加图片的多模态模型。
![alt text](img_v3_02vv_78e65a44-baa5-4a9b-9624-f275a4c5ebeg.jpg)
![alt text](img_v3_02vv_a7eb49fb-934a-4b36-ab04-e8c0db32881g.jpg)
### 2. full-review-repair - 全维度代码审查与修复

**功能说明**：本技能用于执行完整的项目代码审查、修复和测试流程，确保代码质量和功能完整性。

**工作流程**：
```
后端审查（包括数据库）→ 修复 → 前端审查（包括UI）→ 修复 → 前端测试
```

**评估范围**：
- 后端：接口规范、业务逻辑、异常处理、安全防护
- 数据库：SQL 规范、索引优化、事务处理、数据一致性
- 前端：代码规范、渲染性能、交互逻辑、UI 还原度
- UI：布局合理性、视觉效果、用户体验、响应式适配

**使用场景**：项目阶段性审查、新功能开发完成后、修复bug后、用户要求进行全面代码审查和测试时。

**详细文档**：[full-review-repair/SKILL.md](./full-review-repair/SKILL.md)

**注意**：需要添加测试专家智能体，可以自己写或者用我写的。

我用 TRAE 做了一个有意思的Agent 「测试专家」。 点击 https://s.trae.com.cn/a/8ff930?region=cn 立即复刻，一起来玩吧！

### 3. auto-task-experience-summarizer - 自动任务经验总结器

**功能说明**：本技能用于自动读取与总结任务执行经验，包括：
- 任务执行过程中的关键步骤
- 遇到的问题及解决方案
- 优化建议
- 任务流程记录
- 任务类型分类
- 经验类别标注

**触发时机**：
- 任何任务执行开始前
- 任何任务执行完成后
- 主Agent标记任务为完成时
- 需要参考任务经验时
- 需要记录任务经验以供后续参考时

**经验文件**：自动创建经验文件并更新索引，存储在 `.trae/skills/auto-task-experience-summarizer/` 目录中。

**详细文档**：[auto-task-experience-summarizer/SKILL.md](./auto-task-experience-summarizer/SKILL.md)

### 4. brainstorm - 头脑风暴技能

**功能说明**：本技能用于在处理问题、BUG时调用，在进行重大修改、更新、复杂任务时进行头脑风暴，通过系统性地探索代码库、收集各Agent的专业意见，最终整合出多个可行方案供用户选择。

**触发关键词**：问题、BUG、错误、异常、故障、应该、可以、可能、需要、修改、更新、调整、重构、改进等。

**详细文档**：[brainstorm/SKILL.md](./brainstorm/SKILL.md)

### 5. bug-hunter-fractal - 分形式问题排查技能

**功能说明**：本技能采用分形递归思想，从问题现象开始，通过多层级、逐步细化的方式定位问题根源。每个决策点、分叉点、需要确认的地方都必须询问用户，每一步排查内容都会保存到文档。

**分形层级**：
- L0：现象描述
- L1：领域判断
- L2：模块定位
- L3：文件定位
- L4：代码定位（可选）
- L5：根因分析（可选）

**详细文档**：[bug-hunter-fractal/SKILL.md](./bug-hunter-fractal/SKILL.md)

### 6. fractal-designer - 分形式设计器

**功能说明**：本技能采用分形递归思想，从用户的初步想法开始，通过多层级、逐步细化的方式将概念转化为可落地的设计方案。每个技术分叉点、冲突点、需要决策或有疑问的地方都必须询问用户。

**分形层级**：
- L0：初步想法
- L1：需求分析
- L2：方案设计
- L3：详细设计
- L4：可落地实现（可选）

**详细文档**：[fractal-designer/SKILL.md](./fractal-designer/SKILL.md)

### 7. full-review-repair-fractal - 分形式全维度代码审查与修复

**功能说明**：本技能采用分形递归思想，从宏观到微观逐步深入执行完整的项目代码审查、修复和测试流程。每个审查层级都遵循相同的自相似模式，结合全维度评估要点。

**分形层级**：
- L0：项目级
- L1：领域级
- L2：模块级
- L3：文件级
- L4：代码级（可选）

**详细文档**：[full-review-repair-fractal/SKILL.md](./full-review-repair-fractal/SKILL.md)

### 8. graph-theory-fractal - 分形式图论分析技能

**功能说明**：本技能采用分形递归思想结合图论思想，从系统/模块分析开始，通过多层级、逐步细化的方式识别节点、定义边、分析图结构、提出优化建议。

**分形层级**：
- L0：图主题定义
- L1：节点识别
- L2：边的定义
- L3：图的分析
- L4：优化建议（可选）

**详细文档**：[graph-theory-fractal/SKILL.md](./graph-theory-fractal/SKILL.md)

### 9. knowledge-fractal - 分形式知识体系构建技能

**功能说明**：本技能采用分形递归思想，从知识主题开始，通过多层级、逐步细化的方式构建知识体系，可用于写帮助文档或总结 achievement。

**分形层级**：
- L0：知识主题
- L1：知识分类
- L2：知识结构
- L3：知识内容
- L4：详细展开（可选）

**详细文档**：[knowledge-fractal/SKILL.md](./knowledge-fractal/SKILL.md)

### 10. refactor-fractal - 分形式代码重构技能

**功能说明**：本技能采用分形递归思想，从重构目标开始，通过多层级、逐步细化的方式制定重构计划并执行。

**分形层级**：
- L0：重构目标
- L1：范围确定
- L2：策略选择
- L3：计划制定
- L4：执行验证（可选）

**详细文档**：[refactor-fractal/SKILL.md](./refactor-fractal/SKILL.md)

### 11. requirements-fractal - 分形式需求分析技能

**功能说明**：本技能采用分形递归思想，从用户的初步想法开始，通过多层级、逐步细化的方式将概念转化为可落地的需求文档。

**分形层级**：
- L0：原始想法
- L1：需求分类
- L2：需求清单
- L3：详细描述
- L4：验收条件（可选）
- L5：测试用例（可选）

**详细文档**：[requirements-fractal/SKILL.md](./requirements-fractal/SKILL.md)

### 12. task-scheduler-fractal - 分形式项目任务规划器

**功能说明**：本技能采用分形思想，通过多层级、逐步细化的方式制定详细、可执行的项目任务计划文档。针对文档过多的情况，采用分批次读取策略。

**工作流程**：
- 第一层级：文档概览
- 第二层级：框架规划
- 第三层级：细化深化
- 第四层级：验证确认

**详细文档**：[task-scheduler-fractal/SKILL.md](./task-scheduler-fractal/SKILL.md)

## 目录结构

```
skills/
├── frontend-ui-test/
│   └── SKILL.md
├── full-review-repair/
│   └── SKILL.md
├── auto-task-experience-summarizer/
│   └── SKILL.md
├── brainstorm/
│   └── SKILL.md
├── bug-hunter-fractal/
│   └── SKILL.md
├── fractal-designer/
│   └── SKILL.md
├── full-review-repair-fractal/
│   └── SKILL.md
├── graph-theory-fractal/
│   └── SKILL.md
├── knowledge-fractal/
│   └── SKILL.md
├── refactor-fractal/
│   └── SKILL.md
├── requirements-fractal/
│   └── SKILL.md
├── task-scheduler-fractal/
│   └── SKILL.md
├── img_v3_02vv_78e65a44-baa5-4a9b-9624-f275a4c5ebeg.jpg
├── img_v3_02vv_a7eb49fb-934a-4b36-ab04-e8c0db32881g.jpg
└── README.md (本文件)
```

## 使用说明

每个技能模块都包含一个 `SKILL.md` 文件，其中定义了：
- 技能的名称和描述
- 功能说明和使用步骤
- 适用场景
- 工具要求

在项目中使用技能时，AI 助手会根据用户的请求自动选择并调用相应的技能模块。
