# Claude Skills Collection

Claude Code 技能（Skills）集合，用于自动化和增强开发工作流。

## 包含的 Skills

### paper-reading

**论文深度阅读器** - 深度阅读和分析学术论文，用故事化叙述还原研究历程

基于认知科学原理：
- **分层理解**：电梯演讲 → 故事摘要 → 深度精读
- **故事化叙述**：场景化还原研究者的困境和顿悟
- **大量实例**：每个概念配备生活类比、代码实例、对比场景
- **预测误差驱动**：预期 vs 实际对比制造认知冲突

**触发方式**：
```
发送 PDF 论文或请求"帮我分析这篇 paper"时自动触发
```

### tutorial-generator

**教学文档生成器** - 为任何开源项目自动生成高质量教学文档

基于认知科学原理：
- **变式练习**：多场景实例强化理解
- **预测误差驱动**：预期 vs 实际制造认知冲突
- **交错对比**：项目间对比建立知识网络

**使用方法**：
```
/tutorial <项目路径>
```

### paper-reading

**论文深度阅读器** - 深度分析 ML/AI 领域学术论文，用故事化叙述还原研究历程

基于认知科学原理：
- **分层理解**：电梯演讲 → 故事摘要 → 深度精读
- **预测误差驱动**：预期 vs 实际制造认知冲突
- **大量实例**：每个重要概念 3-5 个不同场景实例

**使用方法**：
```
# 发送 PDF 论文或论文链接后，自动触发
/paper-reading
```

### tech-sharing

**技术宣讲稿生成器** - 从大量技术文档生成宣讲大纲和稿子，适用于技术分享会、团队内部分享、技术提案汇报

核心特点：
- **文档驱动整合**：从文档内容自然提取主线，不预设框架
- **避免过度简化**：强制证据链 + 风险标记，保留关键细节
- **混合听众适配**：分层内容设计，新手听得懂，专家不觉得浅
- **可视化工具箱**：Mermaid 图、表格、代码块、折叠区域
- **多轮交互确认**：每个阶段都和用户确认方向

**使用方法**：
```
# 提供多篇文档后，自动触发
# 或手动调用
/tech-sharing
```

## 安装

### 安装单个 Skill

```bash
# 复制 skill 到你的 Claude skills 目录
mkdir -p ~/.claude/skills/tutorial-generator
cp skills/tutorial-generator/SKILL.md ~/.claude/skills/tutorial-generator/skill.md
```

### 安装所有 Skills

```bash
# 复制所有 skills
for skill in skills/*; do
    name=$(basename "$skill")
    mkdir -p ~/.claude/skills/$name
    cp $skill/SKILL.md ~/.claude/skills/$name/skill.md
done
```

## 技能列表

| 技能 | 描述 | 状态 |
|------|------|------|
| paper-reading | 论文深度阅读器 | ✅ |
| tutorial-generator | 教学文档生成器 | ✅ |
| paper-reading | 论文深度阅读器 | ✅ |
| tech-sharing | 技术宣讲稿生成器 | ✅ 新增 |

## 贡献

欢迎提交 Pull Request 添加新的技能！

## 许可证

MIT License

## 联系

- GitHub: https://github.com/miracoder11/claude-skills
