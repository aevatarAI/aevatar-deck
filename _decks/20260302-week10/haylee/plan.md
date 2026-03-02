---
layout: deck
title: "Week 10 Plan"
date: 2026-03-02
week: "2026-W10"
type: plan
member: Haylee
role: QA
---

<style>
.reveal .slides section {
  font-size: 0.74em;
  line-height: 1.12;
}
.reveal .slides section p {
  margin: 0.2em 0;
}
.reveal .slides section ul {
  margin: 0.2em 0 0.2em 1.1em;
}
.reveal .slides section li {
  margin: 0.08em 0;
}
</style>

## 项目 1：Sisyphus（Aevatar research）

测试地址：[https://sisyphus-test.aevatar.ai/](https://sisyphus-test.aevatar.ai/)

**这个项目在做什么**：验证论文从“解析 -> 入库 -> 图谱”整条链路稳定可用，且能 24 小时无人值守运行。

**这周具体怎么测**：
- 先跑 1 篇简单论文，确认流程一次成功、结果可读
- 再跑 3300 页全量任务，连续观察 24 小时是否中断
- 最后抽检 20 个知识节点，核对内容和关联关系

**怎么算通过**：
- 单篇一次跑通，且无 P0/P1 阻断错误
- 全量任务 24 小时不中断，重启次数 = 0
- 抽检 20 个节点中，正确可读 >= 16

**交付什么**：`Sisyphus` 测试报告

---

## 项目 2：NyxID

测试地址：[https://nyx.chrono-ai.fun/](https://nyx.chrono-ai.fun/)

**这个项目在做什么**：验证 NyxID 各模块在“可登录、可连接、可恢复、可排障”四个维度稳定可用。

**测试项目（按模块）**：
- 角色权限：`admin` 与普通用户菜单、操作、越权拦截正确
- `Dashboard` / `API Keys`：总览数据与 Key 状态正确
- `Services` / `Connections` / `Providers`：配置、启停、授权状态一致
- `Settings` / `Authorized Apps`：安全配置、会话、授权管理可用
- `Guide`：文档与示例可读、可复制、可落地

**怎么算通过**：
- 通过：登录/连接/设置链路通过，异常提示清晰，角色权限矩阵通过
- 不通过：关键链路失败，或出现越权成功、P0/P1 阻断

**交付什么**：`NyxID` 测试报告