<div align="center">

# XXD Panel 016

### 把照片里真正发生的关系，压缩成一枚锚点和一场运动

[![Codex Skill](https://img.shields.io/badge/Codex-Skill-000000?style=flat-square)](./SKILL.md)
[![Four Modes](https://img.shields.io/badge/Modes-4-c4573a?style=flat-square)](#四种输出不是四个模板)
[![Raster Output](https://img.shields.io/badge/Output-PNG-2f6f62?style=flat-square)](#边界与信任)

<strong>简体中文</strong> · <a href="README.en.md">English</a> · <a href="README.ja.md">日本語</a>

</div>

> ONE SUBJECT · ONE MOTION · A LARGE FIELD OF AIR

XXD Panel 016 是一个面向 Codex 与兼容 Agent 的图像生成 Skill。它不把照片套进固定滤镜，而是先阅读主体、姿态、方向、光线、距离和没有说完的关系，再把这些事实压缩成一张粗粝、克制、可追溯的 Riso／丝网印刷作品。

照片提供事实。016 决定哪一种运动值得被留下。

## 为什么需要它

普通风格迁移很容易把不同照片做成同一张装饰画：主体被通用太阳、波浪和几何图标替代，颜色与原图无关，标题换一张照片也能继续使用。

016 反过来工作：先锁定一枚可辨认的小型视觉锚点，再从姿态、光线或空间关系中推导唯一的运动逻辑。画面可以极简，但不能失去“为什么只能来自这张照片”的证据。

```text
源照片 → 锁定主体事实 → 提炼关系与潜台词 → 选择一种运动 → 生成版画 → 精确收口与复核
```

## 016 的视觉承诺

- **一个锚点**：主体被压缩成一枚小而可辨认的核心，不增加第二焦点。
- **一种运动**：坠落、上升、流动、扩散或波纹回响只能选择一种主导逻辑。
- **大片留白**：通常保留 60%–78% 的纸面空气，让运动与静止同时成立。
- **源图配色**：一个主色、暖白纸色与可选少量黑，总体控制在 2–3 色。
- **真实印刷感**：网点、纸纤维、干墨、套印偏差和颗粒是结构，不是滤镜贴纸。
- **文字参与空间**：标题和微型文字沿运动、轴线与留白生长，而不是贴在商业标题框里。

## 四种输出，不是四个模板

调用时若没有指定，Skill 会先询问模式。尺寸可以同时给出，精确像素优先。

| 模式 | 默认画布 | 成品 |
| --- | ---: | --- |
| `top-bottom` | 3:4 | 原照片在上，016 版画在下，严格等高 |
| `left-right` | 3:2 | 原照片在左，016 版画在右，严格等宽 |
| `design-only` | 3:4 | 只保留变化后的完整版画，不显示原照片 |
| `wallpaper-pack` | 四种设备尺寸 | 手机、iPad、电脑、儿童手表各一张独立 PNG |

双联模式里的摄影始终保持真实，只允许克制调色和必要的环境延展。单画面与壁纸模式中，原照片只作为内容证据，不出现在成品里。

### 四端壁纸：独立探索或连贯套装

壁纸套装默认输出：手机 `1440×3200`、iPad `2048×2732`、电脑 `3840×2160`、儿童手表 `1024×1024`，也可以逐设备覆盖尺寸。

- **连贯套装（推荐）**：先生成并验收 iPad 定调图；另外三张都使用“原照片＋同一张定调图”重新构图。
- **四张独立**：四张都只参考原照片，允许更自由的构图变化。

两种方式都会生成四张独立文件。连贯套装不是把一张主图裁成四个尺寸，也不会采用 iPad → 手机 → 电脑 → 手表的串联垫图。

## 文字不是装饰，它要让人重新看懂照片

所有模式默认有文字；只有用户明确要求无字时才关闭。

自动文案先读取表层事实、关系张力与有证据的潜台词，再通过精准命名、反差、低调陈述、双重含义或轻微反转，提炼一个极短标题。标题必须通过“换图测试”：如果放到一张无关照片上仍然成立，就必须重写。

用户提供最终成稿时逐字保留；提供方向或可编辑草稿时，Skill 会先理解受众、传播目的、必留词、语气和潜台词，再在授权范围内精炼。

语言按目标受众解析，而不是按下指令时的语言机械输出：

```text
目标市场／受众地区 > 指定成品语言 > 文案方向语言 > 当前请求语言
```

中文请求中的“日本版”会转创为自然日语，“韩国受众”使用自然韩语，“英国版”使用英式英语。Skill 不会根据人物长相或场景猜国籍，也不会用伪外文制造国际感。

## 精确布局交给脚本，审美判断留给生图

生成模型负责版画；`scripts/compose_panel.py` 只负责画布规划、像素级 50/50 合成、最终尺寸和审计，不用代码假装创作视觉。

```bash
python3 scripts/compose_panel.py --plan --layout top-bottom
python3 scripts/compose_panel.py --plan --layout left-right --size 2560x1440
python3 scripts/compose_panel.py --audit result.png --layout design-only --size 2048x2048
```

上下双联的总高度必须为偶数，左右双联的总宽度必须为偶数；Skill 不会偷偷修改用户给出的精确尺寸。

## 开始使用

### 安装

```bash
git clone https://github.com/nevertoday/xxd-panel-016.git
mkdir -p ~/.codex/skills
ln -s "$(pwd)/xxd-panel-016" ~/.codex/skills/xxd-panel-016
```

Claude Code 用户可将同一目录链接到 `~/.claude/skills/xxd-panel-016`。安装后重新开启 Agent 会话。

### 调用

```text
$xxd-panel-016
请把这张照片做成左右双联，2560×1440，文字使用日语。
```

也可以只调用 Skill 并上传照片；它会先用分行编号菜单询问输出模式。选择壁纸套装时，如果没有说明图片关系，会继续询问“连贯套装”或“四张独立”。

完整生成规范：

- [Skill 工作流](SKILL.md)
- [中文完整提示词](references/xxd-panel-016-prompt.zh-CN.md)
- [English full prompt](references/xxd-panel-016-prompt.en.md)

## 边界与信任

- 一张源照片只进入自己的任务，不借用其他照片、旧成品或示例素材。
- 每次调用都会创建新的任务子文件夹，不会把历史结果武断地当作本次完成。
- 成品是 PNG 位图，不用 SVG、HTML、Canvas 或程序化矢量图替代生图。
- 位图桥接器只返回脱敏状态，不打印 provider、端点、请求头、凭据、Prompt 或服务端正文。
- `top-bottom`、`left-right`、`design-only` 各输出一张；`wallpaper-pack` 严格输出四张独立文件，不生成拼贴总览。

运行本地合成脚本需要 Python 3 和 Pillow；安全位图桥接器使用 Python 3.11+ 的 `tomllib`。实际生图仍需要宿主 Agent 的内置位图能力，或已经配置好的兼容位图路径。

## 仓库结构

```text
xxd-panel-016/
├── SKILL.md
├── README.md / README.en.md / README.ja.md
├── agents/openai.yaml
├── scripts/
│   ├── compose_panel.py
│   └── configured_imagegen.py
└── references/
    ├── xxd-panel-016-prompt.zh-CN.md
    ├── xxd-panel-016-prompt.en.md
    └── 016-source.md
```

## 关于 XXD

XXD 是小小东的品牌名缩写。本项目由 [@xiaoxiaodong01](https://x.com/xiaoxiaodong01) 创作与维护。

## 付费社群

如需了解 XXD 付费社群、加入方式或项目相关问题，请扫描下方微信二维码联系。

<p align="center">
  <a href="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png"><img src="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png" alt="XXD 付费社群微信二维码" width="320"></a>
</p>

<div align="center">

**让运动来自照片，而不是来自模板。**

</div>
