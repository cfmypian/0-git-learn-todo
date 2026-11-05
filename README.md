# 0-git-learn-todo
muye2026-餐饮经营分析初始资源文档库

Obsidian vault 目录：`muye-0-git-learn-todo/`（在 Obsidian 中选择「打开本地仓库」指向这个目录）

- `learning/`：学习笔记
- `0-output/`：产出内容

# github

## init（首次把本地工程推到新仓库）
```bash
git init
git add .
git commit -m "first commit XXX"
git branch -M main
git remote add origin https://github.com/cfmypian/0-git-learn-todo.git
git push -u origin main   # 新分支第一次推送时加 -u：设置上游追踪，本地分支与远程分支绑定，之后可直接 git push / git pull
```

## clone（在另一台电脑上获取）
```bash
git clone https://github.com/cfmypian/0-git-learn-todo.git
```

## update（日常同步）
```bash
git pull origin main          # 先拉取远程最新内容
git status                    # 查看改动
git add .                     # 暂存全部改动（或 git add <文件> 只暂存指定文件）
git commit -m "commit XXX"
git push origin main
```

## 本地仓库与远程仓库各自初始化过（历史不相关）
远程建仓时勾选了 README 等初始文件，本地也已有提交，直接 pull 会报 `refusing to merge unrelated histories`：
```bash
git fetch origin
git merge origin/main --allow-unrelated-histories
git push -u origin main
```

## 常用查看命令
```bash
git remote -v                 # 查看远程地址
git log --oneline             # 查看提交历史
git diff                      # 查看未暂存的改动
git restore <文件>            # 撤销某个文件未暂存的改动
```

## 忽略文件
`.gitignore` 中忽略了 `.DS_Store`（macOS 系统文件）和 `.obsidian/workspace.json`（Obsidian 界面状态，频繁变动）。已被跟踪的文件需要先取消跟踪：
```bash
git rm --cached <文件>
```
