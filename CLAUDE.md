# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

使用中文回答；

## 仓库性质

这是一个用 git 做版本管理的 Obsidian 笔记库（vault），不是代码项目：没有构建、lint 或测试命令。所有内容都是 Markdown 笔记。

## 结构

- `muye-0-git-learn-todo/` 是 vault 根目录（在 Obsidian 中打开的就是这个目录，不是仓库根目录）。
  - `learning/` 放学习笔记（输入）。
  - `0-output/` 放产出内容（输出）。
  - `欢迎.md` 是 Obsidian 默认生成的欢迎笔记。
  - `.obsidian/` 是 Obsidian 配置。`workspace.json` 会随 Obsidian 界面操作频繁变动，提交时一般不要包含它，除非用户要求。

## 笔记约定

- 笔记之间的内部链接使用 Obsidian 的 `[[笔记名]]` wikilink 语法。
- 文件名和内容以中文为主。
