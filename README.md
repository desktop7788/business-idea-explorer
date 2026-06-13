# business-idea-explorer

事業・Webサービス・アプリのアイデアを、**毎回同じ評価軸・同じ出力**で探索し評価するための Claude スキル。

思いつきの種から、「**既にコストを払っているのに十分解決できていないペイン**」を見つけ、商材アイデア → 事業モデルと値決め案 → 最初の100人を集める施策 → 検証設計、までを一気通貫で出す。成功するアイデアは低確率でしか当たらないからこそ、「速く・安く・ブレない基準で何度も打席に立つ」ことに価値がある。

## 何をするか（全7フェーズ・フェーズ対話型）

0. **前提インテイク** — 規模志向 / B2B・B2C / 当事者性 / 流通の持ち札 を確認
1. **対象を絞る** — 広い領域から具体的サブ領域へ
2. **ペインのあぶり出し** — レビュー・解約理由・Q&A・コミュニティを横断
3. **ランク付け** — 「支払いの濃さ × 既存解決策の不在 × 到達可能性」で並べる（件数順にしない）
4. **商材アイデア＋競合の厳密確認** — どの一点が本当に空いているか
5. **事業モデル＆お品書き** — 収益レイヤーと仮の値決め
6. **最初の100人を集める施策** — 流通の持ち札に応じて出し分け
7. **検証設計** — 生の声50件 → 5人ヒアリング → 前金テスト → 手動MVP、GO/NO-GO基準

各フェーズの区切りで結果を見せて確認しながら進む。ユーザーの言語で対話・出力し、市場が異なれば情報源・価格・コミュニティを各市場にローカライズする。

## 中核思想

- **「既に金を払っている」を入口にする**（ただの「面倒」は払ってくれない）
- **件数の多い順に並べない**（声が大きい＝レッドオーシャンのことが多い）
- **流通が最大の制約**（特に観客資産が薄いと、勝敗はペインの深さより「届けられるか」で決まる）
- **「自分が使う/払うか」は最強のシグナル**
- **ホワイトスペースは厳密に確かめる**（「空いてそう」で突っ込まない）
- **作る前に検証**（出力は必ず安い検証手順と GO/NO-GO で終える）

## インストール

### Claude Code（ワンクリック・プラグイン）
この repo はプラグインマーケットプレイスとして公開されている。Claude Code で：

```
/plugin marketplace add desktop7788/business-idea-explorer
/plugin install business-idea-explorer@tatsu-tools
```

更新は repo に push したあと、利用側で `/plugin marketplace update`。

### Cowork（Claudeデスクトップ・コード不要）
1. [business-idea-explorer.skill](https://github.com/desktop7788/business-idea-explorer/raw/main/dist/business-idea-explorer.skill) をダウンロード
2. Cowork の会話にこのファイルを添付（ドラッグ＆ドロップ）
3. 表示される「Save skill」を押す（設定 → Capabilities に追加される）

### 手動（スキルだけ使う）
`skills/business-idea-explorer/` をスキル読み込みディレクトリ（例：`~/.claude/skills/business-idea-explorer/`）にコピー。

インストール後は、「〇〇の領域で事業アイデア探したい」「このアイデア評価して」等で自動的に起動する。

## 構成

```
business-idea-explorer/                 # repo root（= マーケットプレイス root = プラグイン root）
├── .claude-plugin/
│   ├── marketplace.json                # マーケットプレイス定義（プラグイン一覧）
│   └── plugin.json                     # プラグイン マニフェスト
├── skills/
│   └── business-idea-explorer/
│       ├── SKILL.md                    # スキル本体（ワークフロー・評価軸・出力テンプレ）
│       └── references/
│           └── playbook.md             # 情報源・値決めアンカー・検証質問バンク
├── dist/
│   └── business-idea-explorer.skill    # 梱包済み（Coworkインストール用）
├── README.md
└── LICENSE
```

`skills/` 配下は Claude Code が自動検出するため、`plugin.json` でスキルを明示宣言する必要はない。

## 再パッケージ

`skills/business-idea-explorer/` を編集したら、Cowork配布用の `.skill` は skill-creator の `package_skill` で作り直せる。プラグインとしての配布は repo に push するだけで反映される。

## ライセンス

MIT License（`LICENSE` 参照）。自由に使用・改変・再配布可。
