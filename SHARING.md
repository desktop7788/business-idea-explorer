# business-idea-explorer 紹介文（コピー用）

リポジトリ: https://github.com/desktop7788/business-idea-explorer
.skill 直リンク（Cowork用）: https://github.com/desktop7788/business-idea-explorer/raw/main/dist/business-idea-explorer.skill

---

## ① ひとことキャッチ

> 思いついた瞬間に、事業アイデアを「同じ評価軸・同じ手順」で検証できる Claude スキル。ペイン発掘から値決め・集客・検証設計まで一気通貫。

---

## ② Cowork 向け（非開発者OK・こちらが主）

### 短文（SNS / Slack / LINE 向け）

事業アイデアを「同じ基準で何度も検証する」ための Claude スキルを無料で公開しました。

領域を伝えるだけで、〈既にお金を払ってるのに解決されてない不満〉を起点に、商材アイデア → 事業モデルと値段の付け方 → 最初の100人の集め方 → 検証のやり方まで、毎回ブレない手順で出してくれます。コード不要、Claude Desktop の Cowork で使えます。

導入は3ステップ：
1. スキルファイルをダウンロード → https://github.com/desktop7788/business-idea-explorer/raw/main/dist/business-idea-explorer.skill
2. Claude Desktop の Cowork の会話に、そのファイルを添付（ドラッグ＆ドロップ）
3. 表示される「Save skill」を押すだけ

あとは「〇〇の領域で事業アイデアを探したい」と話しかければ起動します。

### 導入手順（そのまま案内に使える）

1. **ダウンロード**：[business-idea-explorer.skill](https://github.com/desktop7788/business-idea-explorer/raw/main/dist/business-idea-explorer.skill) を開く（自動でダウンロードされます）
2. **読み込み**：Claude Desktop を開き、Cowork の会話にこの `.skill` ファイルを添付（またはドラッグ＆ドロップ）
3. **保存**：チャットに出る「**Save skill**」ボタンを押す → 設定 → Capabilities に追加されます
4. **使う**：「新しいWebサービスの事業アイデアを探したい」「このアイデア評価して」などと話しかける

> もっとスムーズに配りたいときは、`.skill` ファイルを直接（メール/DM/チャットで）送るのが一番やさしい。GitHub に不慣れな人には、リンクより「ファイルを受け取って Save を押すだけ」の方が迷いません。

---

## ③ Claude Code 向け（開発者）

開発者にはプラグインのワンクリック導入が便利：

```
/plugin marketplace add desktop7788/business-idea-explorer
/plugin install business-idea-explorer@tatsu-tools
/reload-plugins
```

→ https://github.com/desktop7788/business-idea-explorer

---

## ④ 紹介文（ブログ / Zenn / note / コミュニティ投稿向け・両対応）

### business-idea-explorer — 事業アイデアを「同じ基準で何度も検証する」ための Claude スキル

成功する事業アイデアは低確率でしか当たりません。だからこそ大事なのは「速く・安く・ブレない基準で何度も打席に立つ」こと。このスキルは、思いついた領域を放り込むと、毎回同じ評価軸・同じ出力でアイデアを探索・評価してくれます。

**何をするか（全7フェーズ・対話型）**

1. 前提確認（規模志向／B2B・B2C／当事者性／流通の持ち札）
2. 対象を絞る（広い領域 → 具体的サブ領域）
3. ペインのあぶり出し（レビュー・解約理由・Q&A・コミュニティを横断）
4. ランク付け（「支払いの濃さ × 既存解決策の不在 × 到達可能性」で並べる。件数順にしない）
5. 商材アイデア＋競合の厳密確認（どの一点が本当に空いているか）
6. 事業モデル＆お品書き（収益レイヤーと仮の値決め）
7. 最初の100人を集める施策 ＆ 検証設計（生の声→ヒアリング→前金テスト→手動MVP、GO/NO-GO基準）

**特徴（よくある"アイデア出し"との違い）**

- **「既に金を払っているのに未解決」を入口にする**（ただの「面倒」は払ってくれない）
- **声の大きい順に並べない**（声がデカい＝レッドオーシャンのことが多い。到達可能性まで含めて評価）
- **流通を最初から組み込む**（フォロワー0なら検索型/当事者/バイラル、観客や予算があれば別の手、と持ち札に応じて出し分け）
- **作る前に検証**（出力は必ず安い検証手順と GO/NO-GO で終わる）

**こんな人に**：新規事業・副業・個人開発のネタを探している人、思いついたアイデアの筋の良さを素早く確かめたい人、参入余地や値決めの当たりを付けたい人。

**使い方**

- **Cowork（Claude Desktop・コード不要）**：[business-idea-explorer.skill](https://github.com/desktop7788/business-idea-explorer/raw/main/dist/business-idea-explorer.skill) をダウンロード → Cowork の会話に添付 → 「Save skill」。
- **Claude Code**：`/plugin marketplace add desktop7788/business-idea-explorer` → `/plugin install business-idea-explorer@tatsu-tools` → `/reload-plugins`。

導入後は「〇〇の領域で事業アイデアを探したい」「このアイデア評価して」などと話しかけるだけで起動します。

無料・オープンソース（MIT）。改良・再配布自由です。
→ https://github.com/desktop7788/business-idea-explorer

---

## 補足：もっと"非開発者フレンドリー"に配るなら

GitHub 自体が非開発者には少し敷居が高め。よりやさしくするなら：

- **GitHub Release を作る**：repo の「Releases」→「Draft a new release」→ タグ `v1.0.0` → `dist/business-idea-explorer.skill` を添付 → Publish。すると専用のダウンロードページができ、リンクが安定して見た目もやさしくなる。
- **ファイルを直接渡す**：メール・DM・チャットで `.skill` を送る（受け手は Save を押すだけ）。
- **無料の配布ページ**：Gumroad 等に無料商品として `.skill` を置けば、メアド取得＝見込み読者リストも兼ねられる（将来のニュースレター導線に）。
