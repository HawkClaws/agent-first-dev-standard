# エージェント前提開発基準 (Agent-First Development Standard)

コーディングエージェント(Claude Code、Codex 等)に実装を委譲することを前提とした開発チームのための、理解・PR・マージ・レビューの運用基準。

特定のエージェント製品には依存しません。どのエージェントを使うチームでも(混在していても)適用できます。

### 🗺 まずはこの1枚 — [導入前後のフロー比較図](https://hawkclaws.github.io/agent-first-dev-standard/flow-comparison.html)

この基準を入れると、開発フローの**何が変わり、何が変わらないか**を1画面で見られます。基準本文を読む前の全体像として、また導入をチームに提案するときの説明用に。

### ドキュメント

| | |
|---|---|
| [**standard.md**](standard.md) | 基準本文。これが規範 |
| [**skills/**](skills/) | 基準を日常フローとして実行するスキル6本(flow / design-memo / crosscheck / pr-guide / first-review / update-map)。`flow` は他の5本を順に呼ぶ進行係 |
| [flow-comparison](https://hawkclaws.github.io/agent-first-dev-standard/flow-comparison.html) | 導入前後のフロー比較図(GitHub Pages) |
| [skills/pr-guide/assets/pr-template.md](skills/pr-guide/assets/pr-template.md) | PRテンプレート(pr-guide スキルに同梱。正本はこの1枚) |
| [CHANGELOG.md](CHANGELOG.md) | 変更履歴 |

## 思想(3行)

- 「全部読む」は物理的に破綻した。「読まない」は障害の夜に破綻する。この基準は、その間に線を引くための道具である
- 人間の理解はレビューのためではなく、将来の保守・障害対応・意思決定のためにある
- 守られない基準は無いより悪い。重すぎる項目は厳格化ではなく削除する

## このリポジトリの範囲

一般原則のみを含みます。特定の組織への適用(実測値・閾値・チーム構成・チケット運用)は各組織の内部ドキュメントとして管理し、このリポジトリには含めません。適用する場合は、内部ドキュメント側に「本基準 vX.X に準拠」と明記し、更新への追従は意識的に行うことを推奨します。

## 関連する先行事例・研究(2026年8月調査)

主要OSSプロジェクトのAI生成コードポリシーは、いずれも一律の扱いを定めている:[QEMU](https://www.qemu.org/docs/master/devel/code-provenance.html)(AI生成コンテンツを拒否)/ [Gentoo](https://wiki.gentoo.org/wiki/Project:Council/AI_policy)(全面禁止)/ [NetBSD](https://www.netbsd.org/developers/commit-guidelines.html)(汚染推定+コア承認)/ [Fedora](https://communityblog.fedoraproject.org/council-policy-proposal-policy-on-ai-assisted-contributions/)(許可+説明責任と開示。提案は2025年10月に[承認](https://lwn.net/Articles/1042947/))/ [curl](https://github.com/curl/curl/blob/master/docs/CONTRIBUTE.md)(通常品質基準+開示)。

コードの性質に応じて**理解の深さを段階化**した公開基準は、これらにも政府系ガイドラインにも確認できていない。関連研究として、リスクに応じて監督形態を段階化する [Graduated Human Oversight(arXiv:2606.22484)](https://arxiv.org/pdf/2606.22484) がある(軸が異なる)。「無い」ことの証明はできないので、既存の類似基準をご存知であればissueで教えてほしい。

## Contributing

issue / PR 歓迎です。ただし、特定の組織・プロダクトが識別できる情報(社名、実測値、固有のドメイン語彙など)は書かないでください。知見は一般化した形で共有をお願いします。

## License

**[CC BY 4.0](LICENSE)**(Creative Commons 表示 4.0 国際)。商用利用・改変・再配布いずれも可で、条件は**出典の表示**だけです。

### 帰属の書き方(例)

- **社内ドキュメントに取り込む場合**
  > 本ドキュメントは「エージェント前提開発基準」(HawkClaws, CC BY 4.0) v0.9 に準拠しています。
  > https://github.com/HawkClaws/agent-first-dev-standard

  版を明記すると、こちらの改訂への追従を意識的に判断できます(→ [このリポジトリの範囲](#このリポジトリの範囲))。
- **スキルをコピーして自チーム向けに改変した場合** — 改変した `SKILL.md` の冒頭に出典と「改変あり」を1行入れてください。CC BY は改変の明示を求めています。
- **記事・発表で引用する場合** — 通常の引用の作法で足ります。

### 実務上の注意

**社内の非公開ドキュメントに取り込んで自チームで使うだけなら、再配布に当たらないので帰属義務は発生しません。** それでも出典と版を1行書いておくことを勧めます——義務ではなく、**改訂に追従するかを後から判断できる**ようにするためです。

(法的な助言ではありません。厳密な判断が必要な場合は、正文である [legal code](https://creativecommons.org/licenses/by/4.0/legalcode) を確認してください)
