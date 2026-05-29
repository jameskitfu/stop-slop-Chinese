# Stop Slop Chinese

面向中文写作的「去 AI 味」技能。它帮助模型在起草、改写、审稿时删掉中文互联网语境里常见的模板腔、营销腔、翻译腔和空话。

<img width="3840" height="2160" alt="G-Yg4RVbIAAhVxW" src="https://github.com/user-attachments/assets/902afc15-1f40-4a9d-af24-8cd67afb8ebf" />

## 这是什么

中文 AI 文案有自己的痕迹：

- 开头先铺垫「在当今时代」「随着技术发展」
- 中间用「不仅是 A，更是 B」「不是 X，而是 Y」制造转折
- 结尾升华到「这背后反映的是」「未来值得期待」
- 大量使用「赋能」「闭环」「抓手」「底层逻辑」等泛商业词
- 用整齐排比、四字格和假设问句撑场面

这个技能把这些痕迹列出来，并给出更适合中文读者的改写规则。

## 目录结构

```text
stop-slop-Chinese/
├── SKILL.md              # 核心规则
├── references/
│   ├── phrases.md        # 中文场景需要删除或替换的词句
│   ├── structures.md     # 中文 AI 文常见结构问题
│   └── examples.md       # 中文改写示例
├── README.md
└── LICENSE
```

## 快速使用

**Claude Code:** 把这个目录加入 skill。

**Claude Projects:** 上传 `SKILL.md` 和 `references/` 里的参考文件。

**自定义指令:** 复制 `SKILL.md` 的核心规则。

**API 调用:** 把 `SKILL.md` 放进 system prompt，需要时再加载参考文件。

## 它会检查什么

**中文套话**：删掉「值得注意的是」「不可否认」「总的来说」「在某种程度上」「这背后」等提示模型腔的铺垫。见 `references/phrases.md`。

**中文商业黑话**：把「赋能」「抓手」「闭环」「颗粒度」「底层逻辑」「生态矩阵」换成可执行的普通话。见 `references/phrases.md`。

**结构套路**：避免「不是 A，而是 B」「一方面，另一方面」「首先，其次，最后」「这不仅是 A，更是 B」等模板。见 `references/structures.md`。

**句子规则**：少用「我们需要认识到」「可以说」「从某种意义上」这类虚弱主语。少用被动句。少用「极大地」「深刻地」「显著地」等程度副词。不要让抽象名词像人一样行动。

## 评分

每项 1 到 10 分：

| 维度 | 问题 |
|------|------|
| 直接 | 句子在说事，还是在宣布自己要说事？ |
| 口气 | 像中文作者，还是像翻译过来的白皮书？ |
| 具体 | 有没有人、动作、数字、场景？ |
| 节奏 | 句长和段落是否自然变化？ |
| 密度 | 有没有可删的套话和重复？ |

低于 35 分就重写。

## 作者

原版 Stop Slop 由 [Hardik Pandya](https://hvpandya.com) 创建。本分支改成中文写作场景。

## License

MIT. Use freely, share widely.
