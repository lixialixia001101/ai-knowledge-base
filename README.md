# ai-knowledge-base

个人 AI 知识库——结构化 Markdown，Git 管理，供本人及 AI 应用（检索/RAG）直接消费。

## 目录结构

```
├── projects/    项目档案：踩坑记录、修复过程、架构分析（一律脱敏）
├── domain/      领域知识：指标口径、判别逻辑、工艺规则
├── skills/      可复用技能模块（代码/SQL/脚本），从现有项目提炼
├── sop/         标准作业流程、汇报模板
└── public/      对外公开候选区——攒够料后抽出去建公开仓库
```

## 写入原则（红线）

1. 🔴 **一领域一文件夹，一主题一文件**，文件名用中文短句，别堆大杂烩
2. 🔴 **密码、连接串、内部 IP（10.x.x.x）、库名、第三方代码细节，任何目录都不允许出现**
3. 🟡 公司项目相关内容只进 projects/ 且必须脱敏，不进 public/
4. 🟢 别追求完美结构，先平铺着写，写多了再重组

## 配置与安全

- 敏感配置一律走 `.env`（已被 .gitignore 排除），仓库只放 `.env.example`
- 已配置 pre-commit 密钥扫描，启用方式：

```bash
pip install pre-commit
pre-commit install
```

## 本地使用

用 Obsidian / Typora 直接打开本目录即可编辑，Git 同步：

```bash
git add . && git commit -m "notes: xxx" && git push
```
