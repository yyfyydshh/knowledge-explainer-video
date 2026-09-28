# 知识讲解视频 Skill

把一个主题和参考资料，做成**听得懂、看得明白、能跟上旁白节奏**的讲解动画。这是从[八爪鱼视频制作 Skill 库](https://github.com/Bethxx-Skieer/bazhuayu-vedio-cut)独立出来的项目，适合概念科普、方法说明、产品能力介绍和项目迭代故事。

**演示成片：**[▶ 观看《Git 是什么：从 Vibe Coding 到多人协作》](examples/git-explainer/git-explainer-final.mp4)（横版 1920×1080，约 3 分 15 秒，含人工旁白、字幕和配乐）。[案例说明与配乐署名](examples/git-explainer/README.md)。

## 它解决什么问题

知识视频经常卡在“资料很多，但不知道怎么讲”和“画面只是文字卡片，跟声音对不上”。这个 Skill 把工作拆成可确认的阶段：先核对资料和观众要理解的问题，写自然口语的讲稿；再用人物、物件与动作设计分镜；最后以真实录音为时间基准安排动画、字幕、转场和音乐。它提供工作流、清单、Remotion 起始工程与质检脚本，**不是输入主题后无须审核的一键生成器**。

| 你提供 | Skill 帮你完成 | 最终可交付 |
|---|---|---|
| 主题与资料；可选目标观众、画风、角色、真实视频和平台要求 | 事实核对、讲稿、分镜、角色与插画计划、代表帧和连续转场样片 | 按录音制作的横版讲解视频、字幕文件、工程和质检记录 |
| 正式人工录音（可在讲稿确认后再录） | 按自然句和重点词锁定画面动作、停顿及字幕时间 | 完整声画成片；没有录音时只做到静音预览 |

默认 1920×1080、30fps，时长服从内容和录音，不要求硬塞进固定分钟数。字幕默认开启，可在第一次内容确认时关闭。真实视频和配乐可以使用，但外部素材需记录来源与许可。

## 看一个例子

演示片从一个 Vibe Coding 新手的问题切入：AI 改完网站，哪里变了？改坏后能不能回去？随后用可见的动作讲清保存记录、试验分支和多人协作时的选择。角色会提问、操作与检查，而不是一直站在展示板旁边；前一镜头的物件会承接下一镜头，避免突然切成无关的全屏卡片。

[打开完整 MP4 演示视频](examples/git-explainer/git-explainer-final.mp4)。仓库只收录最终成片，不收录原始录音、中间试片或个人项目缓存。

## 怎么使用

### 1. 安装

下载或克隆本仓库，把 `skills/knowledge-explainer-video/` **整个文件夹**复制到 Codex 的技能目录，保留文件夹名：

- Windows：`%USERPROFILE%\.codex\skills\knowledge-explainer-video`
- macOS：`~/.codex/skills/knowledge-explainer-video`

重启 Codex，在新任务中明确写 `$knowledge-explainer-video`。本 Skill 不自动接管普通教程切片或原声访谈任务。仓库也带有千问办公技能元数据；若在其他宿主使用，需按本机环境验证生成与渲染能力。

### 2. 提供任务

最少给出**主题和资料**即可开始。下面这段可以直接改写后发送：

```text
$knowledge-explainer-video
主题：给 Vibe Coding 新手讲清楚 Git 是什么
资料：这里附上文章、文件、仓库或链接
目标观众：没有编程基础的人
要求：画风素雅，可以有卡通人物；先确认讲稿和分镜，不要直接生成全片
```

如果已有人工录音，也可以一起提供；没有的话先写讲稿，等确认后再录。你还可以指定画幅、字幕开关、是否插入真实视频，以及“这次只要策划／样片／完整成片”。

### 3. 两次确认，然后制作

1. **内容确认：**核对事实、受众、叙事结构与完整口语讲稿，同时确定风格、人物、真实视频策略、画幅和字幕。
2. **视觉确认：**看角色设定、开场／核心／结尾代表帧和一段约 8–12 秒的连续转场样片；确认后再批量做素材。
3. **录音与动画：**用人工录音的真实时间安排“出现 → 操作 → 反馈 → 停留 → 交接”，让关键结果留有理解时间。Remotion 模板提供时间线和基础组件，复杂知识关系需要专门动画。
4. **审片与交付：**检查每个场景边界及复杂动作的起点、中间帧和落点，再核对字幕、混音、整片播放与文件解码。未通过时不标记为成片。

人物贴图和插画默认**不套白框**；只有电脑屏幕、文件、窗口等真实容器才有边界。箭头要有明确起点和目标，转场尽量由上一画面已有的物件自然变化而来。可以多生成素材候选，但成片只保留准确、统一、真正帮助理解的画面。

## 项目结构

```text
skills/knowledge-explainer-video/
├── SKILL.md                  入口、调用边界和制作顺序
├── agents/                   Codex 展示信息与显式调用策略
├── references/               叙事证据、视觉、节奏转场、项目清单和交付标准
├── assets/                   项目清单、分镜与 Remotion 起始模板
└── scripts/                  清单校验、工程生成、测试与成片质检
examples/git-explainer/        Git 讲解成片和案例说明
```

从 [`SKILL.md`](skills/knowledge-explainer-video/SKILL.md) 开始阅读；需要字段说明时看[项目清单规范](skills/knowledge-explainer-video/references/project-manifest.md)。Skill 已自带可复制的 [项目清单模板](skills/knowledge-explainer-video/assets/project-manifest.template.json)。

## 开发与验证

只使用 Skill 策划内容时，不必先安装渲染依赖。要生成 Remotion 工程，需要 Node.js/npm；脚本校验使用 Python，视频检查使用 FFmpeg/FFprobe。具体运行命令和状态闸门以 [Skill 文档](skills/knowledge-explainer-video/SKILL.md)为准。仓库根目录可运行：

```bash
node skills/knowledge-explainer-video/scripts/test.mjs
python skills/knowledge-explainer-video/scripts/validate_project.py skills/knowledge-explainer-video/assets/project-manifest.template.json
```

讲稿、视觉、录音与正式时间线都有各自的确认条件；通过脚本检查不等于通过人工审片。原声访谈请用专门的访谈 Skill；长教程切章节和产品录屏演示请用教程 Skill，不要把这些任务硬套成知识动画。
