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

## 贡献

欢迎提交 Pull Request 添加新的技能！

## 许可证

MIT License

## 联系

- GitHub: https://github.com/miracoder11/claude-skills
