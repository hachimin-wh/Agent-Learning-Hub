# CLAUDE.md

个人 Agent 学习仓库：按 README.md 的「Learning Todo List」（Stage 0-8）主线学习，配合「Project Ladder」（Level 1-11）做实战项目，学习记录与产物推送到远程。

## 目录结构

```text
├── README.md / index.html / CONTRIBUTING.md   # 指南本体（上游维护），禁止修改
├── PROGRESS.md                                # 学习进度总表（唯一的打勾处）
├── stages/                                    # 学习过程（按 Stage）
│   └── stage-N-slug/
│       ├── docs/                              # 学习笔记 + 英文资料翻译/摘录
│       │   ├── notes.md                       # 笔记，开头是本 stage 的 checklist
│       │   └── <文章短名>.zh.md               # 英文资料翻译，读的时候创建
│       └── code/                              # 练习脚本（有代码时才创建）
│           ├── 01-xxx.py                      # 编号对应 checklist 项
│           └── requirements.txt               # 本 stage 依赖
└── projects/                                  # Project Ladder 成品（按 Level）
    └── LNN-name/                              # 自包含：README（运行步骤、示例输入输出、失败记录）+ 代码 + 依赖
```

## 约定

1. 指南本体（README.md、index.html、CONTRIBUTING.md）不修改，保持可同步上游；checklist 打勾只写在 PROGRESS.md。
2. 目录随学习进度创建，不预铺空目录；docs/、code/ 子目录仅在实际有内容时创建。
3. 新开一个 stage 时：目录命名 `stage-N-英文slug`，先把该 stage 的 checklist 和产出要求抄进 docs/notes.md 作为待办。
4. stages/ 与 projects/ 分工：stages/ 放学习过程（练习脚本、笔记、trace，允许一次性验证代码）；projects/ 放满足「别人能 clone 下来跑」标准的成品。两条线相互独立，指南本身没有 stage 与 project 的对应关系；仅当某个 stage 的产出恰好可以成为某档 project 时，成品放 projects/，并在该 stage 的 notes.md 里链接过去。
5. 练习脚本命名 `NN-描述.py`，编号对应 checklist 顺序。
6. 依赖按 stage / project 各自维护 requirements.txt，不建全局依赖。
7. 文档以中文为主；英文资料翻译文件命名 `<文章短名>.zh.md`，与 notes.md 同目录。
8. 含密钥的文件（.env 等）不入库（.gitignore 已覆盖）；小型运行产物（trace、输出）可放对应 stage 目录。
