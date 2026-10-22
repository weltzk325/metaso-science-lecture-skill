# Metaso Science Lecture Skill

一个用于生成「秘塔 AI 学点啥」理工科课程材料的 Codex skill。它把研究资料整理成一份连续、完整、可朗读的教学讲义，通常以带内嵌图片的 PDF 交付，并保留可编辑的 LaTeX 源文件。

## 适用场景

- 从论文、技术资料和用户笔记中构建一条从物理基础到公式、机制、计算与验证的讲解链。
- 生成可上传给秘塔连续讲解的单一课程文件，而不是把主要内容拆成一问一答。
- 在用户听完课程之后，再进入追问和费曼复述。

## 安装

将本仓库克隆到 Codex 的 skills 目录：

```powershell
git clone https://github.com/weltzk325/metaso-science-lecture-skill.git "$env:USERPROFILE\.codex\skills\metaso-science-lecture"
```

重启或刷新 Codex 后，可通过 `$metaso-science-lecture` 调用。

## 文件结构

- `SKILL.md`：核心工作流与触发条件。
- `references/`：科学内容写作、采样与验证、仿真与代码、LaTeX交付规范。
- `assets/main.tex`：支持中文的课程文档起始模板。
- `agents/openai.yaml`：skill 展示信息。

## 设计原则

先讲清物理对象和因果链，再讲数学表达与计算实现；明确假设、单位、边界条件和验证层级；示意图要解释因果关系，数据图要说明横纵轴、分布含义和可验证结论。对随机模拟，重点解释目标分布、采样率与统计比较，避免把“画出相似图”误说成“复现了完整物理过程”。

## 相关项目

GitHub 上另有通用的 [personal-ai-learning](https://github.com/yuewenyumenle/personal-ai-learning) skill，其内容提到秘塔并设计了对话式学习流程。它适合学习规划与复盘，但没有针对秘塔讲课材料的理工科讲义构建流程。

## 使用许可

本仓库当前未声明开源许可证。