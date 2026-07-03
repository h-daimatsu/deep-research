# 引用書式（マークダウン脚注記法）

Deep Research スキルで作成するレポート全てに共通する引用書式。Web ドキュメントのデファクト（Wikipedia 方式）に対応するマークダウン標準の脚注記法を採用する。番号順に引用し末尾に文献リストを置くこの方式は、学術分野で言う**バンクーバー方式**（番号引用方式）にあたる。

## 基本の書き方

本文中は `[^N]` で参照し、URL は末尾の `## 出典` セクションで `[^N]: ...` の形式で定義する。

| 参照番号 | 本文（原文） | 末尾定義（原文） | レンダリング結果 |
|---|---|---|---|
| 1 | `事実A [^1]。` | `[^1]: [タイトル](https://example.com) — 発行元 (2026/4/21)` | `[^1]` が上付き番号リンクとして表示され、末尾定義にジャンプ。末尾側ではタイトルがクリッカブルリンクになる |
| 2 | `主張B [^2]。同ソース再引用 [^1]。` | `[^2]: [タイトル](https://example.com) — 発行元` | 同じソースを複数箇所で再参照可能 |

この記法は GitHub / Obsidian / VSCode / Pandoc で共通してレンダリングされる。

## 禁止形

以下の形式は使わない。

- `[N](URL)` — 旧方式のインラインリンク記法。本文に URL が残り可読性を損なう
- `[[N]](URL)` — ブラケットの二重化
- `[&#91;N&#93;](URL)` / `&#91;N&#93;` — HTML エンティティを含む任意の派生形。SKILL ドキュメント内で `[^N]` をリテラル表示する用途以外では使わない
- 本文中の素の URL 表記（`https://...` を直接本文に書く）
- 末尾脚注定義で URL を `— URL` のようにベタ書きし、タイトルをリンク化しない旧フォーマット

## 1対1対応の必須要件

本文の `[^N]` と末尾の `[^N]:` は完全に対応させる。

- **孤立参照禁止**: 本文に `[^N]` があるのに末尾で定義されていない
- **未使用定義禁止**: 末尾で `[^N]:` が定義されているのに本文で使われていない
- **欠番禁止**: 1 から連続した番号にする（1,2,4 で 3 が飛ぶのは NG）
- **重複禁止**: 同じ番号を複数箇所で定義しない（同じ番号を本文で複数回参照するのは OK）

## 末尾セクションのフォーマット

レポートの最後に `## 出典` セクションを置き、脚注定義を列挙する。

### 基本形

```
[^N]: [タイトル](URL) — 発行元 (日付)
```

### 実例

```markdown
## 出典

[^1]: [Vertiv Reports Strong First Quarter with Diluted EPS Growth of 136%](https://investors.vertiv.com/news/news-details/2026/Vertiv-Reports-Strong-First-Quarter/default.aspx) — Vertiv IR (2026/4/22)

[^2]: [Eaton Reports Record Fourth Quarter 2025 Results](https://www.businesswire.com/news/home/20260202111800/en/Eaton-Reports-Record-Fourth-Quarter-2025-Results) — BusinessWire (2026/2/3)

[^3]: [Claude Cowork desktop architecture overview](https://support.claude.com/en/articles/14479288-claude-cowork-desktop-architecture-overview) — Anthropic Help Center

[^4]: [AWS plants more tombstones in the application graveyard](https://www.theregister.com/2026/04/29/aws_whats_next_application_graveyard_corey_quinn/) — The Register / Corey Quinn (2026/4/29)

[^5]: [From developer desks to the whole organization: Running Claude Cowork in Amazon Bedrock](https://aws.amazon.com/blogs/machine-learning/from-developer-desks-to-the-whole-organization-running-claude-cowork-in-amazon-bedrock/) — AWS Blog (2026/4/21)
```

### フォーマット原則

1. **タイトルはマークダウンリンク `[タイトル](URL)` で書く**: 本文がクリーンになり、マークダウンビューア上でクリッカブルになる
2. **発行元名は短縮形で明示する**: 発行主体が一目で判別できる短縮名を使う（辞書例は次セクション）
3. **日付がある場合は末尾に `(YYYY/MM/DD)` で付ける**: 日付がない永続的なリファレンス（公式ドキュメント、FAQ ページ等）では省略可
4. **筆者が明示的な場合は発行元に続ける**: `{媒体} / {筆者名}` の形（例: `The Register / Corey Quinn`）
5. **URL のクエリパラメータは必要最低限に**: トラッキングパラメータ（`utm_*`, `ref=` 等）は削除し、記事本体に到達する最小形にする
6. **区切りは半角ハイフン ` — ` （em dash）を使う**: ハイフン前後に半角スペース。視覚的に発行元と区切りを作る
7. **脚注定義は箇条書きにせずトップレベルに置き、定義どうしの間に空行を1行入れる**: `- ` を付けると脚注として認識されない。空行がないと脚注非対応のビューアやプレーン表示で定義が1行に繋がって見える

## 確信度タグ（柱の主張の脚注に付与）

結論を支える柱の主張（headline number・論旨の柱）の脚注定義には、末尾に確信度タグを付ける。読者が本文を汚さずに確からしさを判断できるようにする。**枝葉の事実には付けない**（タグなし＝通常）。

| タグ | 意味 |
|---|---|
| `〔一次照合〕` | 一次原本（原典・当事者発信・公式開示）に直接照合済み |
| `〔二次・独立複数〕` | 独立した複数の二次ソースが、異なる一次に由来して一致 |
| `〔要確認: 単一源泉/一次未確認〕` | 源泉を畳むと独立源泉が1つ、または一次文書からしか確定し得ない事実が一次未確認。矛盾の有無に関係なく付与する |

```markdown
[^4]: [タイトル](URL) — SEC EDGAR (2026/5/20) 〔一次照合〕

[^5]: [タイトル](URL) — TradingKey (2026/5) 〔要確認: 単一源泉/一次未確認〕
```

集合知・コンセンサス系（アナリストコンセンサス、市場規模推計等）と解釈・市場観系の柱は、独立複数ソースが一致すれば `〔二次・独立複数〕` が十分な確信度であり、`〔要確認〕` 扱いにしない。`〔要確認〕` は事実抽出系の一次未確認、または源泉が実質1つの場合に限る（`workflow.md` の「主張のタイプ別の確からしさ戦略」参照）。

`〔要確認〕` を付した柱は、本文でも限定詞（ヘッジ語）で確認済み事実と区別する（`tone-rules.md`）。

## 発行元短縮辞書（例）

以下は発行元の短縮形の**例**である。網羅的な辞書ではなく、パターンを示すための参考。実際のソースに応じて同様の原則で命名する。

| 発行元カテゴリ | 短縮例 | 備考 |
|---|---|---|
| AWS 公式ブログ | `AWS Blog` | ブログ系全般 |
| AWS 公式ドキュメント | `AWS Docs` | docs.aws.amazon.com |
| AWS ニュース | `AWS News`、`AWS What's New` | aws.amazon.com/about-aws/whats-new |
| Amazon 公式発表 | `Amazon IR`、`About Amazon` | press.aboutamazon.com |
| Anthropic 公式 | `Anthropic` | 公式サイト・ブログ |
| Anthropic サポート | `Anthropic Help Center` | support.claude.com |
| Anthropic プラットフォーム | `Anthropic Platform Docs` | platform.claude.com/docs |
| Microsoft 公式 | `Microsoft`、`Microsoft Blog`、`Microsoft 365 Docs` | |
| Google 公式 | `Google`、`Google Research`、`Google Cloud Blog` | |
| 企業 IR | `{企業名} IR` | 例: `Vertiv IR`、`Micron IR` |
| プレスリリース配信 | `BusinessWire`、`PR Newswire` | 一次発信企業のプレスを配信 |
| 大手ビジネスメディア | `Forbes`、`Bloomberg`、`Reuters`、`Fortune`、`WSJ`、`FT` | 筆者明示がある場合は `Forbes / {筆者名}` |
| 大手テックメディア | `The Register`、`TechCrunch`、`Ars Technica`、`The Verge`、`Wired` | |
| 記事配信サイト | `Yahoo Finance`、`Morningstar`、`CNBC` | |
| リサーチ会社 | `Gartner`、`IDC`、`Forrester`、`Counterpoint Research` | |
| 日本のテック系 | `Zenn`、`Qiita`、`AWS builders.flash` | |
| コミュニティ | `Reddit`、`Hacker News`、`Stack Overflow`| |
| 公的機関 | `BIS`（米商務省）、`FTC`、`EU Commission`、`METI` | |
| 学術・論文 | `arXiv`、`IEEE`、`ACM`、`Nature` | |
| 個人ブログ・ニュースレター | `{媒体名} / {筆者名}` | 例: `The Product Compass / Paweł Huryn` |
| フォーラム | `Windows Forum`、`Apple Developer Forums` | |

**原則**: 発行主体が「どの組織の、どの部門の、誰が出したか」を短く表現する。迷ったときは「このソースを再度探すとき、何という組織名で検索するか」を基準に決める。

## 複数回引用のパターン

同一ソースを複数箇所で引用する場合は、同じ番号を使い回す。

```markdown
この事実は AWS 公式ブログで示されている [^1]。
（別のセクションで）同じ AWS 公式ブログによれば、別の仕様も明らかにされている [^1]。
```

末尾定義は `[^1]: ...` を1つだけ置く。
