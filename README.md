<p align="center">
  <img src="./assets/banner.svg" alt="XXD Panel 016 项目介绍" width="1200">
</p>

<div align="center">

# XXD Panel 016

### 把照片里真正发生的关系，压缩成一枚锚点和一场运动

[![Codex Skill](https://img.shields.io/badge/Codex-Skill-000000?style=flat-square)](./SKILL.md)
[![Four Modes](https://img.shields.io/badge/Modes-4-c4573a?style=flat-square)](#四种输出不是四个模板)
[![Raster Output](https://img.shields.io/badge/Output-PNG-2f6f62?style=flat-square)](#边界与信任)

<strong>简体中文</strong> · <a href="README.en.md">English</a> · <a href="README.ja.md">日本語</a> · <a href="README.ar.md">العربية</a>

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

## 样张 · 来自 X

> [小小东（@xiaoxiaodong01）](https://x.com/xiaoxiaodong01/status/2090127008349163643) · 2026-08-19<br>
> GPT2 × 颗粒 × 磁场 × 版画 × 美学提示词 × VOL.016<br>
> 图片来自《中国国家地理》· 新疆

<table>
  <tr>
    <td width="50%"><a href="https://x.com/xiaoxiaodong01/status/2090127008349163643"><img src="https://pbs.twimg.com/media/HQGej5TaQAAMDO-.jpg?format=jpg&amp;name=large" alt="XXD Panel 016 样张 1"></a></td>
    <td width="50%"><a href="https://x.com/xiaoxiaodong01/status/2090127008349163643"><img src="https://pbs.twimg.com/media/HQGekoCaMAAhjX8.jpg?format=jpg&amp;name=large" alt="XXD Panel 016 样张 2"></a></td>
  </tr>
  <tr>
    <td width="50%"><a href="https://x.com/xiaoxiaodong01/status/2090127008349163643"><img src="https://pbs.twimg.com/media/HQGelcbaMAAw0k3.jpg?format=jpg&amp;name=large" alt="XXD Panel 016 样张 3"></a></td>
    <td width="50%"><a href="https://x.com/xiaoxiaodong01/status/2090127008349163643"><img src="https://pbs.twimg.com/media/HQGemgnasAAkmlT.jpg?format=jpg&amp;name=large" alt="XXD Panel 016 样张 4"></a></td>
  </tr>
</table>

<p align="center"><a href="https://x.com/xiaoxiaodong01/status/2090127008349163643">查看原推文与完整说明 →</a></p>

## 四种输出，不是四个模板

调用时若没有指定，Skill 会先询问模式。尺寸可以同时给出，精确像素优先。

| 模式 | 尺寸逻辑 | 成品 |
| --- | ---: | --- |
| `top-bottom` | 源图自适应 | 原照片在上，016 版画在下，每格保留完整原图尺寸，严格等高 |
| `left-right` | 源图自适应 | 原照片在左，016 版画在右，每格保留完整原图尺寸，严格等宽 |
| `design-only` | 源图自适应 | 只保留变化后的完整版画，不显示原照片，沿用源图比例与尺寸 |
| `wallpaper-pack` | 四种设备尺寸 | 手机、iPad、电脑、儿童手表各一张独立 PNG |

双联模式里的摄影始终保持真实，只允许克制调色和必要的环境延展。单画面与壁纸模式中，原照片只作为内容证据，不出现在成品里。

### 四端壁纸：独立探索或连贯套装

壁纸套装不会静默套用尺寸。选择“常用设备预设”时使用手机 `1440×3200`、iPad `2048×2732`、电脑 `3840×2160`、儿童手表 `1024×1024`；也可以逐设备自定义。

- **连贯套装（推荐）**：先生成并验收 iPad 定调图；另外三张都使用“原照片＋同一张定调图”重新构图。
- **四张独立**：四张都只参考原照片，允许更自由的构图变化。

两种方式都会生成四张独立文件。连贯套装不是把一张主图裁成四个尺寸，也不会采用 iPad → 手机 → 电脑 → 手表的串联垫图。

## 文字不是装饰，它要让人重新看懂照片

正式生图前会先确认文字方式：自动文案、自定义文案或无文字。自动／自定义还会确认目标语言或地区；自定义文案可直接输入主标题和可选微型文字。

自动文案先读取表层事实、关系张力与有证据的潜台词，再通过精准命名、反差、低调陈述、双重含义或轻微反转，提炼一个极短标题。标题必须通过“换图测试”：如果放到一张无关照片上仍然成立，就必须重写。

用户提供最终成稿时逐字保留；提供方向或可编辑草稿时，Skill 会先理解受众、传播目的、必留词、语气和潜台词，再在授权范围内精炼。

语言按目标受众解析，而不是按下指令时的语言机械输出：

```text
目标市场／受众地区 > 指定成品语言 > 文案方向语言；以上均未明确时，生图前询问
```

中文请求中的“日本版”会转创为自然日语，“韩国受众”使用自然韩语，“英国版”使用英式英语，“阿拉伯语版”使用自然的现代标准阿拉伯语与从右到左排版。Skill 不会根据人物长相或场景猜国籍，也不会用伪外文制造国际感。

## 精确布局交给脚本，审美判断留给生图

生成模型负责版画；`scripts/compose_panel.py` 只负责画布规划、像素级 50/50 合成、最终尺寸和审计，不用代码假装创作视觉。

```bash
python3 scripts/compose_panel.py --plan --layout top-bottom --source photo.png
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
├── README.md / README.en.md / README.ja.md / README.ar.md
├── agents/openai.yaml
├── assets/banner.svg
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

## 支持与会员权益

### 深度咨询｜299 元/小时

按小时提供一对一 Skills 深度咨询，每小时 299 元。如需预约，请扫描下方微信二维码联系小小东。

### 小小东 Skills 用户交流群｜入群 99 元

一次付费加入用户交流群，用于 Skills 使用经验分享、作品交流与成员互助；不包含按小时的一对一深度咨询。入群请扫描下方微信二维码，备注「Skills 用户群」。

### 知识星球＋成员提示词库｜699 元/年

知识星球与 [XXD 成员提示词库](https://vip.xiaoxiaodong.ai/)属于同一项会员权益：**支付一次年费，两项同时开通，不需要重复付费。**

任选一种开通方式：

1. 在[知识星球](https://wx.zsxq.com/group/15554814142882)开通后，微信联系小小东，领取成员提示词库兑换码。
2. 在[成员提示词库](https://vip.xiaoxiaodong.ai/)自助开通后，微信联系小小东，由小小东邀请进入知识星球。

<p align="center">
  <a href="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png"><img src="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png" alt="XXD 付费社群微信二维码" width="320"></a>
</p>

<div align="center">

**让运动来自照片，而不是来自模板。**

</div>
