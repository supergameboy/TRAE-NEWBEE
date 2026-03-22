---
name: frontend-ui-test
description: 前端界面操作测试技能：启动前端服务器、访问页面、截图和页面快照、对比变化。每次前端代码修改后必须调用；每次需要验证功能的后端修改后必须调用；Invoke when user wants to test frontend UI functionality or perform browser interactions.
---

# 前端界面操作测试技能

## 功能说明

此技能用于进行前端界面操作测试，包括：
- 检测前端后端开发服务器是否启动
- 如未启动，启动前端后端开发服务器
- 使用浏览器访问页面
- 使用 MCP integrated_browser 服务的browser_take_screenshot 截图
- 使用 MCP integrated_browser 服务的browser_snapshot 获取页面快照
- 读取截图文件
- 点击页面元素（按钮等）
- 再次使用 MCP integrated_browser 服务的browser_take_screenshot 截图
- 再次使用 MCP integrated_browser 服务的browser_snapshot 获取页面快照
- 读取截图文件
- 对比操作前后的变化（包括截图和快照）
- 循环执行多轮测试
- 输出最终测试报告

## 技能核心逻辑

前端界面越来越复杂，需要同时获取截图和页面快照才能完整反映用户真实看到的界面。截图用于视觉对比，快照用于DOM结构验证。利用AI看图片的能力，正确识别真实的用户界面，针对性的对用户界面进行调整。
不要偷懒！

偷懒，通俗指刻意减少付出、逃避应做之事，以更低成本换取休息或便利的行为。它不是简单的休息，而是带有主观逃避性、违背责任或效率原则的选择，横跨日常行为、心理动机、社会评价与进化逻辑多个层面。
关键特征：
- 主观故意：不是能力不足，而是不愿做
- 目标偏向舒适：优先满足当下轻松，而非完成目标
- 常伴随责任逃避：本该由自己承担的义务、后果、风险或角色任务，主动选择回避、推卸、否认、拖延，不愿面对和承担的行为与心理状态。
- 短期获益，长期可能受损：省时省力，但常导致质量下降、后果堆积

## 使用步骤

### 1. 检查并启动后端服务器
- 读取后端开发服务器端口配置
- 检查后端服务器状态，如未运行则启动
- 默认端口: 6123
- 使用 `npm run dev` 在 backend 目录启动

### 2. 检查并启动前端服务器
- 读取前端开发服务器端口配置
- 检查前端服务器状态，如未运行则启动
- 默认端口: 6124
- 使用 `npm run dev` 在 frontend 目录启动

### 3. 浏览器导航到目标页
- 使用浏览器访问本地开发地址
- 等待页面加载完成

### 4. 获取页面截图和快照
- 获取当前页面状态
- 使用 MCP integrated_browser 服务的browser_snapshot 获取页面快照
- 使用 MCP integrated_browser 服务的browser_take_screenshot 截图
- 读取截图内容

### 5. 执行交互操作
- 点击按钮或其他交互元素
- 等待变化

### 6. 获取操作后截图和快照
- 再次使用 MCP integrated_browser 服务的browser_snapshot 获取页面快照
- 再次使用 MCP integrated_browser 服务的browser_take_screenshot 截图
- 读取截图内容
- 对比变化（截图对比 + 快照对比）

### 7. 循环执行（3→4→5→6）
- 根据测试需求，循环执行多个页面或多个操作的测试
- 每轮测试都包含完整的截图和快照获取及对比

### 8. 输出测试报告
- 汇总所有轮次的测试结果
- 记录发现的问题
- 输出完整的测试报告

## 工具要求

- 必须使用 MCP integrated_browser 服务
- 需要浏览器导航、截图、快照、点击、控制台消息、网络请求等工具

## 注意事项

- 根据项目前端路由风格选择目标页，如果是app类型的路由风格，则必须从首页进入到目标页。
- **必须同时使用 browser_snapshot 和 browser_take_screenshot**，不要只使用其中一个
- 子Agent没有权限使用 MCP integrated_browser 服务，请主Agent使用 MCP integrated_browser 服务
- 子Agent使用playwright MCP进行测试
- 出现问题时，注意浏览器控制台消息，注意后台终端消息，注意网络请求的传输。
- 截图文件保存到 `项目根目录/_screenshot/` 目录下，方便清理
- 测试完成后清理截图文件。
- 截图和快照都需要AI自己去获取，然后对比图片的细节变化，不能依赖人工对比。
- 如果有疑问或需要项目中没有的特定信息，使用AskUserQuestion 工具询问用户。