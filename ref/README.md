# ref/ · 参考资料 / 论文

放置研究相关的论文 PDF、外部文档、笔记。

## 协议约定（详见 `AGENTS.md § 8`）

- Agent **默认不主动扫描**本目录，避免污染上下文。
- 当 `idea.md` / `method.md` / `Discussion.md` 中出现 `ref/<path>` 形式的**显式引用**，Agent **必须读取**被引用文件并在下次发言中反映其内容。
- 用户口头要求时同样必须读。

## 建议组织

```
ref/
├── papers/        论文 PDF（按方法或话题归类）
├── notes/         你的阅读笔记 .md
├── slides/        相关 talks / 课件
└── README.md      本文件
```

## 注意

- 大文件（>50MB）建议用 [Git LFS](https://git-lfs.com/) 或单独的外部存储，避免拖慢仓库。
- 如果不想 commit PDF（仅本地参考），可在 `.gitignore` 加 `ref/papers/*.pdf`。
