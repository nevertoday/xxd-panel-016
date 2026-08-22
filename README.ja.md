<p align="center">
  <img src="./assets/banner.svg" alt="XXD Panel 016 プロジェクトバナー" width="1200">
</p>

<div align="center">

# XXD Panel 016

### 写真の中で本当に起きている関係を、ひとつの核とひとつの運動へ圧縮する

[![Codex Skill](https://img.shields.io/badge/Codex-Skill-000000?style=flat-square)](./SKILL.md)
[![Four Modes](https://img.shields.io/badge/Modes-4-c4573a?style=flat-square)](#4つの出力モードは4つのテンプレートではない)
[![Raster Output](https://img.shields.io/badge/Output-PNG-2f6f62?style=flat-square)](#境界と信頼性)

<a href="README.md">简体中文</a> · <a href="README.en.md">English</a> · <strong>日本語</strong>

</div>

> ONE SUBJECT · ONE MOTION · A LARGE FIELD OF AIR

XXD Panel 016 は、Codex と互換 Agent のための画像生成 Skill です。写真に固定フィルターを重ねるのではありません。被写体、姿勢、方向、光、距離、そして言葉になりきらない関係を読み取り、その証拠を、抑制の効いた触覚的なリソグラフ／シルクスクリーン作品へ圧縮します。

事実を与えるのは写真です。何の動きを残すべきかを決めるのが 016 です。

## なぜ、この Skill が必要なのか

一般的なスタイル変換では、無関係な写真まで同じ装飾ポスターになりがちです。固有の被写体が、太陽、波、円環、幾何学アイコンへ置き換わり、色は元写真とのつながりを失い、タイトルも別の写真へそのまま流用できてしまいます。

016 は逆向きに考えます。まず、小さくても判別できる視覚的な核をひとつ固定し、姿勢、光、空間関係から、ただひとつの運動ロジックを導きます。画面は極限まで簡潔でも、「この写真からしか生まれない理由」を失ってはいけません。

```text
元写真 → 視覚的事実を固定 → 関係と含意を読む → 運動をひとつ選ぶ → 版画を生成 → 合成と検証
```

## 016 のビジュアル原則

- **核はひとつ**：小さくても判別できる中心を置き、第二の主役を加えません。
- **運動はひとつ**：落下、上昇、流動、放射、波紋／反響のいずれかを主軸にします。
- **余白も構造**：通常は紙面の 60%–78% を空け、静止と運動を同時に成立させます。
- **色は元写真から**：主色一色、温かな紙色、必要に応じて少量の黒。全体で 2–3 色です。
- **物理的な印刷感**：網点、紙繊維、かすれ、粒子、わずかな版ずれを装飾ではなく構造として使います。
- **文字も空間の一部**：見出しとマイクロコピーを運動、軸、余白に沿わせ、広告的なタイトル枠へ閉じ込めません。

## 4つの出力モードは、4つのテンプレートではない

モードが未指定なら、Skill が最初に確認します。サイズは同時に指定でき、正確なピクセル値が最優先です。

| モード | 既定キャンバス | 出力 |
| --- | ---: | --- |
| `top-bottom` | 3:4 | 上に元写真、下に 016 版画。高さを厳密に 50/50 分割 |
| `left-right` | 3:2 | 左に元写真、右に 016 版画。幅を厳密に 50/50 分割 |
| `design-only` | 3:4 | 元写真を表示しない、一枚の完成版画 |
| `wallpaper-pack` | 端末別4サイズ | スマートフォン、iPad、デスクトップ、子ども向け腕時計の個別 PNG |

二分割モードの写真は現実の写真として保ち、控えめな色調整と必要最小限の背景拡張だけを許可します。単画面と壁紙では、写真は内容の根拠として使われますが、完成画像には現れません。

### 壁紙セット：独立制作と連続セット

既定サイズはスマートフォン `1440×3200`、iPad `2048×2732`、デスクトップ `3840×2160`、腕時計 `1024×1024`。端末ごとに変更できます。

- **連続セット（推奨）**：まず iPad 用の基準画像を生成・検証し、残りの三枚は「元写真＋同じ基準画像」を参照しながら各画面へ再構成します。
- **4枚を独立制作**：各端末が元写真だけを参照し、より自由に構図を探索します。

どちらも四つの独立ファイルを返します。連続セットは一枚を四サイズへ切り抜く方式ではなく、iPad → スマートフォン → デスクトップ → 腕時計と順番に参照を連鎖させることもありません。

## コピーは、写真の見え方を変えるためにある

文字は全モードで既定オンです。明示的に「文字なし」と指定した場合だけ外します。

自動コピーは、画面上の事実、関係の緊張、根拠のある含意を読み、正確な命名、対比、抑制、二重の意味、わずかな反転から短いタイトルを作ります。無関係な写真へ置いても同じように成立するタイトルは不採用です。

完成原稿は一字一句保持します。方向性や編集可能な草稿の場合は、読者、目的、必須語句、語調、含意を守った範囲でのみ磨きます。

言語は命令文ではなく、届けたい読者を優先します。

```text
対象市場・読者 > 指定された出力言語 > コピー方針の言語 > 依頼文の言語
```

中国語で「日本向け」と依頼しても、出力コピーは自然な日本語になります。韓国向けなら自然な韓国語、英国向けならイギリス英語です。人物の外見や風景から国籍を推測したり、雰囲気だけの擬似外国語を使ったりしません。

## 正確な幾何はコードへ。表現判断は画像生成へ

版画を作るのは画像生成モデルです。`scripts/compose_panel.py` はキャンバス設計、厳密な 50/50 のラスタ合成、最終サイズ、監査だけを担当し、プログラム描画で作品を代用しません。

```bash
python3 scripts/compose_panel.py --plan --layout top-bottom
python3 scripts/compose_panel.py --plan --layout left-right --size 2560x1440
python3 scripts/compose_panel.py --audit result.png --layout design-only --size 2048x2048
```

上下分割はキャンバス全高、左右分割は全幅が偶数である必要があります。指定された正確なピクセル値を黙って変更することはありません。

## はじめる

```bash
git clone https://github.com/nevertoday/xxd-panel-016.git
mkdir -p ~/.codex/skills
ln -s "$(pwd)/xxd-panel-016" ~/.codex/skills/xxd-panel-016
```

Claude Code では、同じフォルダーを `~/.claude/skills/xxd-panel-016` へリンクできます。インストール後は Agent セッションを再起動してください。

```text
$xxd-panel-016
この写真を 2560×1440 の左右二分割にしてください。コピーは日本語で。
```

写真だけを添えて Skill を呼び出すこともできます。その場合は、改行された番号付きメニューでモードを確認し、壁紙セットなら必要に応じて「連続セット」か「4枚を独立制作」かを続けて確認します。

完全な仕様：

- [Skill ワークフロー](SKILL.md)
- [中国語版フルプロンプト](references/xxd-panel-016-prompt.zh-CN.md)
- [英語版フルプロンプト](references/xxd-panel-016-prompt.en.md)

## 境界と信頼性

- 一枚の元写真は自分のタスク内だけで使い、別の写真、過去の成果物、同梱例から内容を借りません。
- 呼び出しごとに新しいタスクフォルダーを作り、以前の成果物を今回の完了扱いにしません。
- 出力は PNG ビットマップです。SVG、HTML、Canvas、プログラム生成ベクターで代用しません。
- 設定済みビットマップブリッジは匿名化した状態だけを返し、provider、endpoint、header、credential、Prompt、サーバー応答本文を表示しません。
- 通常モードは一枚、`wallpaper-pack` は必ず四枚を返し、一覧用コラージュへまとめません。

ローカル合成には Python 3 と Pillow が必要です。安全なビットマップブリッジは Python 3.11+ の `tomllib` を使用します。実際の画像生成には、ホスト Agent の内蔵ビットマップ生成機能、または設定済みの互換ルートが必要です。

## リポジトリ構成

```text
xxd-panel-016/
├── SKILL.md
├── README.md / README.en.md / README.ja.md
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

## XXD について

XXD は Xiaoxiaodong のブランド名を略したものです。このプロジェクトは [@xiaoxiaodong01](https://x.com/xiaoxiaodong01) が制作・管理しています。

## サポートと会員特典

### Skills Q&A｜CNY 99

この料金は Skills の利用に関する Q&A サポート向けです。購入またはお問い合わせは、以下の WeChat QR コードから Xiaoxiaodong へご連絡ください。

### 知识星球＋会員向けプロンプトライブラリ｜年額 CNY 699

知识星球と [XXD 会員向けプロンプトライブラリ](https://vip.xiaoxiaodong.ai/)は、ひとつの会員特典です。**年額料金を一度支払えば両方を利用でき、二重に購入する必要はありません。**

登録方法は、次のどちらかを選べます。

1. [知识星球](https://wx.zsxq.com/group/15554814142882)で登録後、WeChat で Xiaoxiaodong に連絡し、会員向けプロンプトライブラリの引換コードを受け取る。
2. [会員向けプロンプトライブラリ](https://vip.xiaoxiaodong.ai/)で直接登録後、WeChat で Xiaoxiaodong に連絡し、知识星球への招待を受ける。

<p align="center">
  <a href="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png"><img src="https://xiaoxiaodong.pages.dev/assets/wechat-qr.png" alt="XXD 有料コミュニティの WeChat QR コード" width="320"></a>
</p>

<div align="center">

**動きはテンプレートではなく、写真から生まれる。**

</div>
