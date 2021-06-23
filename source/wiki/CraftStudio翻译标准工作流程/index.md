---
layout: wiki
order: 10
seo_title: CraftStudio翻译标准工作流程
wiki: CraftStudio翻译标准工作流程
description: CraftStudio软件本地化以及翻译小组面对翻译项目时的标准工作流程
---

**作者：Cubik65536**

<!-- more -->

**所有CraftStudio软件本地化以及翻译小组成员必须熟悉该文内容**

**此文档不适用于软件本地化项目**

## 分工

目前 CraftStudio 软件本地化以及翻译小组组长为 [`@WUTONK`](https://github.com/WUTONK)，组长拥有分配团队成员，决定项目优先级的权利。同时，组长应对项目完成质量负责。

所有翻译小组成员均需要以下能力：

- 达标的英语能力（我们不求翻译的跟出版社一样，但是我们要保证看到的人都能看懂）
- 熟悉 Markdown 语法
- 熟悉 Git 以及 GitHub 的使用（可以查看[本文](https://xaoxuu.com/wiki/git/)取得基本知识）

一个翻译项目需要以下成员：

- 翻译者
- 校稿/校对
- 审核

注意：
: 一个成员可以同时担任多个职位

### 成员审核流程

#### 由现有成员邀请

1. 将信息提交给组长，组长预先进行审核（仅通过提交的信息）
2. 组长认为合格后，将资料提交给管理层
3. 管理层使用（有可能是正在制作的）项目内容进行翻译审核，通过后加入小组

#### 由组长邀请

与上文相似，但只需要组长直接提交资料随后进入第三步

## 项目流程

推荐使用的软件（本次实例使用这些软件作为示例）

- [GitHub Desktop](https://desktop.github.com) - GitHub 客户端
- [Typora](https://typora.io) - Markdown 编辑器

### 立项

管理层成员与组长经过讨论决定翻译的项目，组长开始分配人手，决定每个成员的职位，负责（翻译/校对）的部分

> 如果人手不够组长需要让成员身兼多职，尽量不要让翻译/校对的部分一样，让成员互相校对

### 各成员开始工作

**此文档以《使用 LWJGL3 开发 3D 游戏（3D Game Development with LWJGL 3）》一书的翻译工作为例**

1. 成员前往[工作室的 GitHub 仓库](https://github.com/CraftStarStudio)，以此次为例，仓库链接为：https://github.com/CraftStarStudio/lwjglbook-bookcontents-zh_CN
2. 点击右上角的 `Fork` 来 Fork（分支）该仓库
3. 你应该会被跳转至自己的仓库，这时候你的屏幕右上角应该显示：
   > `你的 GitHub 用户名` / `仓库名`
   > **forked** from CraftStarStudio / `仓库名`
4. 点击绿色的 `Code`，选择 `Open with GitHub Desktop`，依照你的浏览器/操作系统，浏览器会提示你是否要开启 GitHub Desktop，选择 `是`
5. GitHub Desktop 启动后，会有一个标题为 `Clone a Repository` 弹窗，</br>你可以更改 `Local Path` 来更改保存的地方，然后点击蓝色的 `Clone`
6. 等待一段时间，你的电脑正在下载文件，时长多长基本上由你的网络情况决定，如果有弹窗 `How are you planning to use this fork?`，</br>选择 `To contribute to the parent project` 然后选择 `Continue`
7. 打开你保存的文件夹（`Local Path`），GitHub Desktop 右侧会有 `Show in Finder` (macOS) 或者 `Show in Explorer`（Windows）来让你直接打开文件夹
8. 编辑文件，进行翻译

### Commit

> 当管理层让你 `Commit` 的时候不要说 `这是什么？` 了！

**简单解释，这就是保存你的进度**

编辑一个或者多个文件之后，进入 GitHub Desktop，在右下侧的 `Summary (required)` 处简单描述本次更改的内容（最好用英语），然后点击 `Commit to master`

> 注意，此处的 master 可能会变，但是通常为 `master` 或者 `main`

> 如果你仅仅编辑了一个文件，此处的 `Summary (required)` 可能会变成
> `Edit <文件名>`， `Add <文件名>`， `Remove <文件名>` 或者 `Rename <文件名>` 
> **不要**这么留着！

### Push

> 当管理层让你 `Push` 的时候不要说 `这是什么？` 了！

**简单解释，这就是让你把内容传到GitHub上**

Commit之后，你的GitHub Desktop顶部最右侧会有一个 `Push origin`，点它即可，成功了之后它应该会变成 `Fetch origin`

### 提交PR

> 当管理层让你 `提交PR`，`开PR`，`提交Pull request` 的时候不要说 `这是什么？` 了！

**简单解释，这就是让你把内容提交到工作室仓库里，让负责审核的人可以进行审核，如果没有问题就会把你的更改加入工作室仓库**

1. 打开GitHub（右上角写着
   > `你的 GitHub 用户名` / `仓库名`
   > **forked** from CraftStarStudio / `仓库名`

   的仓库）
2. 点击上方的 `Contribute` （一般应该在 `This branch is 1 commit ahead of CraftStarStudio:master.` 的右侧。注意！此处的数字可能会变！这里也有可能出现behind！），点击 `Open pull resuqest`
3. 你应该进入了一个标题为 `Comparing changes` 的界面，右上角写的是 CraftStarStudio / `仓库名`，点击 `Create pull request`
4. 在 `Title` 处简单描述你做完的工作，必要时使用 `Leave a comment`（可以使用中文）
5. 在右侧的 `Reviewer` 处选择你的校稿/校对人员（最好不超过3个）， `Assignees`处选择你自己，校稿/校对人员，`Labels` 处选择 `Localization`
6. 点击 `Create pull request`，你的工作告一段落了

### 校稿/校对
 
#### 校稿/校对人员

如果你是校稿/校对人员而且你收到了要求你Review的通知，进入Pull request界面，开始你的工作

1. 点击任何一次Commit，这时你应该看到编辑前后的差异
2. 点击右上角的 `Changes from 1 commit`，将它改成 `Changes from all commits` (点击 `Show all changes`)
3. 如果你需要添加建议，将鼠标放在需要添加建议的地方，然后点击左侧蓝色的 `+`
4. 输入你的建议，你可以填写包括但不限于：翻译建议，纠错等内容，然后点击 `Add a review comment` （如果是第一条的话请点击 `Start a review`
5. 完成之后，在右上角点击 `Finish your review` （如果没有任何建议的话，该按钮显示 `Review changes`），然后在 `Leave a comment` 处提出总体建议
6. 在下方选择 `Approve`（你觉得没有问题）或者 `Request changes`（你觉得需要更改），然后点击 `Submit reivew` 提交
7. 当所有校稿/校对人员都提交Approve之后，在 `Reviewer` 和 `Assignees` 处添加组长，组长查看下面组长部分的工作流程

#### 翻译者

如果你是翻译者而且你收到了组长或校稿/校对人员，甚至是部门负责人的 `Request changes`时，对你的翻译进行更改，可以在群内或者在GitHub处讨论，更改完成后重新Commit并Push（你不需要重新开PR了）

#### 组长

如果你是组长而且所有校稿/校对人员都提交了Approve，进入Pull request界面，开始你的工作

1. 做一次最终审核，审核流程依照校稿/校对人员流程
2. 当你和所有校稿/校对人员均提交Approve之后在 `Reviewer` 和 `Assignees` 处添加部门负责人

#### 部门负责人

如果你是部门负责人~~（不，你不是）~~，而且组长以及所有校稿/校对人员都提交了Approve，进入Pull request界面，开始你的工作

1. 做一次最终审核，审核流程依照校稿/校对人员流程
2. 当你，组长和所有校稿/校对人员均提交Approve后，进入Merge流程

### Merge

**这部只能由部门负责人操作，故暂不列出**
