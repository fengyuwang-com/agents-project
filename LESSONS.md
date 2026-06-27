---
AIGC:
    Label: "1"
    ContentProducer: 001191440300708461136T1XGW3
    ProduceID: 7af529a0f6360cc6a80ea7b1bc937927_3a4a67eb71c311f1b2f55254006c9bbf
    ReservedCode1: EudFrC5Il4bJKkJkEfRue2o+PpS45FwE97O+3ct7W9DGVTErWEaAs4qU2yidrzJe3lqc/aiPFt0NFJxIDMaQ3U5sSHCqIVIiwXtcxoajA8qfhE6AqhLtMoVWj1FEXsGGV+BFgnthsdbThWBFhDyO47pra4ixRUQMfCL2Px9/nxbshTLsLqgkRK+IzHU=
    ContentPropagator: 001191440300708461136T1XGW3
    PropagateID: 7af529a0f6360cc6a80ea7b1bc937927_3a4a67eb71c311f1b2f55254006c9bbf
    ReservedCode2: EudFrC5Il4bJKkJkEfRue2o+PpS45FwE97O+3ct7W9DGVTErWEaAs4qU2yidrzJe3lqc/aiPFt0NFJxIDMaQ3U5sSHCqIVIiwXtcxoajA8qfhE6AqhLtMoVWj1FEXsGGV+BFgnthsdbThWBFhDyO47pra4ixRUQMfCL2Px9/nxbshTLsLqgkRK+IzHU=
---



# LESSONS.md

> 每次犯错都是资产。记录下来，不再重复。

---

## 格式说明

每条教训使用以下模板：

```markdown
### [日期] 简短标题

- **严重程度**: 🔴 Critical | 🟡 Medium | 🟢 Low
- **场景**: 在什么情况下发生
- **错误**: 具体做错了什么（附代码/命令/截图）
- **根因**: 为什么会犯错
- **教训**: 学到了什么
- **预防**: 以后如何避免（具体的规则/检查项/自动化手段）
- **标签**: #debugging #deployment #testing #security #performance #tooling #process #architecture #communication
```

---

## 教训记录

> 以下为示例，实际项目中请删除示例并填写真实教训。

### 2026-01-15 未检查 Docker 镜像是否存在就直接部署

- **严重程度**: 🔴 Critical
- **场景**: 使用 docker compose up -d 部署服务
- **错误**: 直接执行 `docker compose up -d`，但 ghcr.io 镜像在国内网络下 TLS 握手超时，导致服务无法启动
- **根因**: 未预先验证镜像是否可拉取，忽略了网络限制
- **教训**: 中国大陆环境部署前，先 `docker pull` 测试镜像可达性；ghcr.io 镜像需通过 `ghcr.nju.edu.cn` 代理拉取
- **预防**: 部署脚本中增加镜像预拉取和可达性检查步骤
- **标签**: #deployment #tooling

### 2026-02-20 环境变量名与代码不一致

- **严重程度**: 🔴 Critical
- **场景**: 配置 .env 文件后启动应用
- **错误**: 按 .env.example 中的 `EMAIL_USER` 填写，但代码实际读取的是 `EMAIL_ADDRESS`，导致功能静默失败
- **根因**: 信任模板文件，未 grep 验证代码中实际引用的环境变量名
- **教训**: .env.example 可能与代码不一致，部署前必须用 `grep -r "process.env"` 验证所有环境变量
- **预防**: 在 CI 中添加环境变量一致性检查脚本
- **标签**: #debugging #deployment

---

## 编写原则

1. **具体而非模糊**：写清楚错误命令、错误日志、文件路径，不要写"部署出了问题"
2. **诚实而非遮掩**：承认判断失误、假设错误，这比任何成功经验更有价值
3. **可执行而非说教**：每条教训必须有具体的预防措施（一行命令、一条检查项）
4. **追溯而非孤立**：关联相关的 Issue、PR、Commit，形成知识图谱
5. **定期回顾**：每周 / 每个里程碑回顾一次 LESSONS.md，检查是否有重复踩坑

## 什么值得记录

✅ 导致返工的错误假设
✅ 选错工具/方案后的对比分析
✅ 排查了 30 分钟以上的 Bug
✅ 上线后回滚的真实原因
✅ 第三方服务踩坑（API 限制、文档错误等）

## 什么不值得记录

❌ 通用最佳实践（写在文档里即可）
❌ 「以后要注意」这种空话
❌ 已经在官方文档里写清楚的内容
❌ 纯个人偏好（如「我不喜欢这个框架」）
*（内容由AI生成，仅供参考）*
*（内容由AI生成，仅供参考）*
