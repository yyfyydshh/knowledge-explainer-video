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

## 动画能力与长期复用（Skill 1.4.0）

除了画风，制作还要先确定观众的观看过程。新版增加：

- [十二原则的知识动画用法](skills/knowledge-explainer-video/references/motion-language.md)：预备动作、关键姿态、路线、速度、接触与反馈，以及多种有语义依据的转场。
- [画面与动画优化推理](skills/knowledge-explainer-video/references/visual-revision-logic.md)：从语义变化、因果、注意力、连续性、阅读与证据定位问题，改善 PPT 感，并把真实录屏与报告指引组织为产品能力展示。
- [字幕与手机可读性](skills/knowledge-explainer-video/references/captions-and-readability.md)：字号与信息层级、自然断句、可选半透明底、字体加载、句间闪烁、高清检查；附本次 Data Hub 参数示例，不作为所有项目默认值。
- [历史反馈与回归项](skills/knowledge-explainer-video/references/feedback-and-regressions.md)：人物是行动组件、避免 PPT 化和无关装饰、无穿模、字幕安全区与全片节奏。区分通用要求和 Git 案例专用选择。
- [特殊视频素材融合](skills/knowledge-explainer-video/references/footage-integration.md)：按源时间码与内容拆解录屏或视频，安排动画切入、局部解释、原声与切出，不只是插入播放框。
- [动作谱模板](skills/knowledge-explainer-video/assets/motion-score.template.json)与 [校验脚本](skills/knowledge-explainer-video/scripts/validate_motion_score.py)：检查动作区间、阶段顺序、文字交接和锚点几何；不自动认定视觉流畅。

- [组件交互契约](skills/knowledge-explainer-video/references/interaction-contracts.md)：容器出入的前后遮挡、跨镜物件所有权、镜头与指针联动，以及多人操作和选择的完整过程。
- [配乐、混音与 MP4 导出](skills/knowledge-explainer-video/references/audio-and-export.md)：按讲解试听选曲、从干净旁白重混、许可署名、版本锁定和输出文件检查。
- [修订审查记录](skills/knowledge-explainer-video/assets/revision-review.template.json)：分别记录几何、静帧、原速动态、音画试听、字幕和完整解码；未执行的检查保持待办，不以渲染成功代替审片通过。

本次只更新 Skill 与使用说明，不替换仓库中的 Git 演示视频；示例成片与最新制作规则的版本分别管理。

```bash
python skills/knowledge-explainer-video/scripts/validate_motion_score.py skills/knowledge-explainer-video/assets/motion-score.template.json
python -m unittest discover -s skills/knowledge-explainer-video/scripts -p test_motion_score.py
```

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

## 用到了哪些技术和“插件”

这套项目不是一个视频模型，而是一条可以复核的制作链：

```text
Codex 读取 Skill 规则 → JSON 项目清单记录讲稿、素材与时间线
→ Node.js 生成 Remotion 工程 → React/TypeScript 组织画面和声音
→ Remotion 渲染视频 → Python + FFmpeg 检查成片
```

| 技术／组件 | 在这个仓库里的具体作用 |
|---|---|
| **Codex Skill（Markdown + YAML）** | [`SKILL.md`](skills/knowledge-explainer-video/SKILL.md) 定义何时使用、两次确认和成片标准；[`agents/openai.yaml`](skills/knowledge-explainer-video/agents/openai.yaml) 给 Codex 提供展示信息与显式调用策略。[`.skill-metadata.yaml`](skills/knowledge-explainer-video/.skill-metadata.yaml) 提供千问办公的示例提示词。这些是宿主入口配置，不是视频渲染插件。 |
| **JSON 项目清单** | [`project-manifest.json` 模板](skills/knowledge-explainer-video/assets/project-manifest.template.json) 保存资料来源、批准状态、旁白句、人物与物件、画面时间、素材许可和转场承接物；脚本和动画读取同一份数据，避免各自维护一套时间线。 |
| **Node.js（内置文件系统模块）** | [`build.mjs`](skills/knowledge-explainer-video/scripts/build.mjs) 检查能否进入预览或正式制作，复制已选素材与录音，把字幕 JSON 导出为 SRT，并生成独立的 Remotion 项目。它负责“组装工程”，不负责自动写讲稿或生成插画。 |
| **React 19.3 + TypeScript 5.9** | 把角色、插画、真实视频、文字、字幕和转场写成可复用的画面组件；TypeScript 给场景和项目清单定义数据结构，减少字段与时间线接错的风险。核心代码见[画面组件](skills/knowledge-explainer-video/assets/remotion-template/src/KnowledgeExplainer.tsx)和[类型定义](skills/knowledge-explainer-video/assets/remotion-template/src/types.ts)。 |
| **Remotion 4.0 + `@remotion/cli`** | 用 `Composition`、`Sequence`、逐帧时间和插值动画控制镜头；CLI 打开预览、导出代表帧及 H.264 MP4。复杂知识关系可在 [`CustomScenes.tsx`](skills/knowledge-explainer-video/assets/remotion-template/src/CustomScenes.tsx) 注册专门场景／转场，基础模板不会自动把文字卡片变成完整动画。 |
| **`@remotion/media`** | 在 Remotion 时间线上放入真实视频、人工旁白和背景音乐；模板按旁白句时间给音乐做简单避让，避免盖住人声。 |
| **`@remotion/captions` 与自有字幕层** | 当前使用该包的 `Caption` **类型定义**；实际上屏由项目的 `CaptionLayer` 根据字幕 JSON 和当前帧完成，SRT 由 `build.mjs` 导出。它**没有**在本仓库里自动识别语音或替人断句。 |
| **Python 3 标准库** | [`validate_project.py`](skills/knowledge-explainer-video/scripts/validate_project.py) 检查清单、素材引用、时间范围、授权字段和制作闸门；[`qa_render.py`](skills/knowledge-explainer-video/scripts/qa_render.py) 汇总成片检查报告。不要求额外的 Python 包来运行这两个脚本。 |
| **FFmpeg / FFprobe** | 质检时读取视频编码、画幅、帧率和时长，完整解码，并截取转场边界、动作起中终点和字幕代表帧供人工审片。它们是需在本机安装的外部命令行工具。 |
| **Git / GitHub** | 管理 Skill 与模板版本，并展示这个仓库的 [Git 案例成片](examples/git-explainer/README.md)；它们不是制作视频时的画面或配音引擎。 |

Remotion、React、TypeScript 和三个 `@remotion/*` 包的精确锁定版本见 [`package.json`](skills/knowledge-explainer-video/assets/remotion-template/package.json)与 [`package-lock.json`](skills/knowledge-explainer-video/assets/remotion-template/package-lock.json)。**图片生成、真实视频下载和配音克隆不是本仓库内置插件**：插画可由任务环境里可用的生成工具制作并人工选定；真实视频和音乐要核对授权；正式旁白按这个 Skill 的标准使用人工录音。

## 开发与验证

只使用 Skill 策划内容时，不必先安装渲染依赖。要生成 Remotion 工程，需要 Node.js/npm；脚本校验使用 Python，视频检查使用 FFmpeg/FFprobe。具体运行命令和状态闸门以 [Skill 文档](skills/knowledge-explainer-video/SKILL.md)为准。仓库根目录可运行：

```bash
node skills/knowledge-explainer-video/scripts/test.mjs
python skills/knowledge-explainer-video/scripts/validate_project.py skills/knowledge-explainer-video/assets/project-manifest.template.json
```

讲稿、视觉、录音与正式时间线都有各自的确认条件；通过脚本检查不等于通过人工审片。原声访谈请用专门的访谈 Skill；单纯把已有长教程或产品录屏切章节请用教程 Skill。用户明确选择本 Skill 制作旁白、解释动画与真实操作证据结合的产品能力片时，使用这里的混合制作流程。
