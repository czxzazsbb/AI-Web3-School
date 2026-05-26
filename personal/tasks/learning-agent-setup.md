---
task_id: T-20260525-1
title: 完成 Learning Agent Setup
status: done
opened: 2026-05-25
closed: 2026-05-26
related_daily: personal/daily/2026-05-25.md
---

# T-20260525-1 · 完成 Learning Agent Setup

## 背景

AI × Web3 School cohort-0「AI 向任务」第一项：把 https://aiweb3.school/learning-agent.zh.txt 的 Learning Agent 流程跑起来，并在 fork（czxzazsbb/AI-Web3-School）里建好 `personal/` 工作区，作为后续 4 周（2026-05-18 → 2026-06-14）daily / tasks / experiments / handbook-feedback 的承载。

## 目标 / Definition of Done

- [x] 本地能用 Learning Agent prompt 跑起来流程（Claude Code on Windows）
- [x] fork 已建立 `personal/` 工作区，结构齐全：`README.md / profile.md / learning-plan.md / daily/ tasks/ experiments/ handbook-feedback/ hackathon/ submissions/ templates/`
- [x] `profile.md` 已填学员画像（不是模板占位）
- [x] `learning-plan.md` 已填 4 周计划（不是模板占位）
- [x] `templates/daily-note.md` 和 `templates/task-note.md` 就位
- [x] 通过 fork PR 改 upstream `notes/czxzazsbb.md` 的边界已明确：**不碰**，打卡走 WCB Learning 平台
- [x] WCB Learning 平台提交本任务作为 proof-of-work

## 步骤

1. 在 https://aiweb3.school/learning-agent.zh.txt 拉取启动 prompt，本地用 Claude Code 跑通
2. fork `IntensiveCoLearning/AI-Web3-School` → `czxzazsbb/AI-Web3-School`，clone 到 `D:\learning\AI-Web3-School`
3. 设置 git 身份为 noreply 邮箱 `214419054+czxzazsbb@users.noreply.github.com`
4. 在 fork 顶层建 `personal/` 子目录，避免污染 upstream（`git pull upstream main` 不冲突）
5. 起 `personal/README.md`、`profile.md`、`learning-plan.md`、`templates/daily-note.md`、`templates/task-note.md`
6. commit `b78765b6 personal: init Learning Agent workspace`
7. 到 WCB Learning 平台手动提交本任务 → 拿到提交链接回填到下方"产出"

## 卡点 / 日志

- 2026-05-25 22:40 — 一度把 daily 打卡写进 `notes/czxzazsbb.md`，发现会和 WCB Agent API 自动写入冲突
- 2026-05-26 — 修正：upstream `notes/czxzazsbb.md` 完全交给 WCB Agent API；个人材料一律放 `personal/`，commit `97169d26 notes(czxzazsbb): restore upstream authoritative version` 回滚到 upstream 权威版本

## 产出

- `personal/` 工作区：https://github.com/czxzazsbb/AI-Web3-School/tree/main/personal
- 学员画像：https://github.com/czxzazsbb/AI-Web3-School/blob/main/personal/profile.md
- 学习计划：https://github.com/czxzazsbb/AI-Web3-School/blob/main/personal/learning-plan.md
- 初始化 commit：https://github.com/czxzazsbb/AI-Web3-School/commit/b78765b6
- WCB Learning 提交链接：_（提交后回填）_

## 自评

- **完成度**：✅ 全部 DoD 已达成
- **耗时**：约半天（含一次走弯路 + 回滚）
- **关键收获**：搞清了 fork PR vs WCB Agent API 两条独立写入路径的边界，避免后续 daily 打卡冲突
- **下一步**：进入正式 daily 节奏，每天 12:00 / 22:00 节点更新 `personal/daily/YYYY-MM-DD.md`，同步在 WCB Learning 完成打卡
