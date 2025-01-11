---
date: 2024-10-09
is_project: true
description: 用 Cursor AI 做一个 Obsidian 插件
---

![Demo](assets/demo.png)

Journal Prompts 是一个简单的 Obsidian 插件，它允许用户从预设的提示语库中随机挑选一个写作主题，以激发写作灵感。这个插件是[开源的](https://github.com/realwya/journal-prompts-plugin)。目前我还没有提交到 Obsidian 的官方插件库中，只能手动安装。具体安装方法请参考 Github 仓库的说明。

## 背景

> 灵感往往来自于一个小小的提示。

我一直很喜欢 Apple 的手记 App 中的提示语功能。这些简单的问题或主题尝尝会激发我的写作灵感。作为一个 Obsidian 用户，我想在我的主力笔记软件中也使用这样的功能。我在Reddit 上找到了一份很棒的[提示语清单](https://www.reddit.com/r/Journaling/comments/r7bsmz/long_list_of_journal_prompts/)，这成为了我插件的默认提示语库。

## 核心功能

插件的功能并不复杂：

1. 插件会自动创建一个名为 Journal Prompts Library 的笔记，包含默认的提示语清单。用户可以自由编辑这个文件，每一行文字会被当做一个提示语。
2. 点击左侧栏的 lightbulb 图标或者通过命令面板中的 “Get Journal Prompt” 命令来随机获取一条提示语。点击刷新按钮获取新的提示。
3. 点击“insert”按钮，当前的提示语会以 Callout 格式插入到正在编辑的笔记中。

## 开发过程

尽管我只有基础的前端开发知识，但在 [Cursor](https://www.cursor.com/) AI 辅助的帮助下，我几乎没有亲自编写多少代码就完成了这个插件。整个开发过程大致如下：

1. 研究 [Obsidian 的官方文档](https://docs.obsidian.md/Plugins/Getting+started/Build+a+plugin)和[示例插件](https://github.com/obsidianmd/obsidian-sample-plugin)。
2. 与 AI 协作，逐步实现功能。例如，我会提出需求(本来是准备把所有的对话记录截图分享的，但是由于我没有保存 cursor workspace，所以丢失了对话记录……下次吧)：
	- when I enable this plugin I wanna create a new note called "Journal Prompts Library" which contains some journal prompts
	- create a ribbon icon and click it will open a modal that shows a random prompt from the prompts library with two buttons, one will refresh the random prompt and one will insert the prompt to the opened note file
3. 测试 AI 生成的代码，并根据实际效果提出进一步的需求或修改建议


Cursor 给出的代码准确很高，几乎不需要怎么调整，从构思到完成仅用了不到一个下午的时间。

## 后续计划

目前这个插件的状态已经足够我个人使用了。如果接下来我还有动力的话，我可能会：

1. 把插件提交到 Obsidian 的官方插件库，让更多用户能方便的安装和使用
2. 开发新建 Daily Notes 时自动在开头添加提示语的功能，使日常记录更加丰富
3. 为提示语添加标签或分类，允许用户根据特定主题（如工作、学习、情感等）筛选提示

