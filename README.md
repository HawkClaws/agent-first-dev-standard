# エージェント前提開発基準 (Agent-First Development Standard)

コーディングエージェント(Claude Code、Codex 等)に実装を委譲することを前提とした開発チームのための、理解・PR・マージ・レビューの運用基準。

特定のエージェント製品には依存しません。どのエージェントを使うチームでも(混在していても)適用できます。

- 本体: [standard.md](standard.md)
- PRテンプレート: [templates/pr-template.md](templates/pr-template.md)
- 変更履歴: [CHANGELOG.md](CHANGELOG.md)

## 思想(3行)

- 「全部読む」は物理的に破綻した。「読まない」は障害の夜に破綻する。この基準は、その間に線を引くための道具である
- 人間の理解はレビューのためではなく、将来の保守・障害対応・意思決定のためにある
- 守られない基準は無いより悪い。重すぎる項目は厳格化ではなく削除する

## このリポジトリの範囲

一般原則のみを含みます。特定の組織への適用(実測値・閾値・チーム構成・チケット運用)は各組織の内部ドキュメントとして管理し、このリポジトリには含めません。適用する場合は、内部ドキュメント側に「本基準 vX.X に準拠」と明記し、更新への追従は意識的に行うことを推奨します。

## 関連する先行事例・研究(2026年8月調査)

主要OSSプロジェクトのAI生成コードポリシーは、いずれも一律の扱いを定めている:[QEMU](https://www.qemu.org/docs/master/devel/code-provenance.html)(AI生成コンテンツを拒否)/ [Gentoo](https://wiki.gentoo.org/wiki/Project:Council/AI_policy)(全面禁止)/ [NetBSD](https://www.netbsd.org/developers/commit-guidelines.html)(汚染推定+コア承認)/ [Fedora](https://communityblog.fedoraproject.org/council-policy-proposal-policy-on-ai-assisted-contributions/)(許可+説明責任と開示)/ [curl](https://github.com/curl/curl/blob/master/docs/CONTRIBUTE.md)(通常品質基準+開示)。

コードの性質に応じて**理解の深さを段階化**した公開基準は、これらにも政府系ガイドラインにも確認できていない。関連研究として、リスクに応じて監督形態を段階化する [Graduated Human Oversight(arXiv:2606.22484)](https://arxiv.org/pdf/2606.22484) がある(軸が異なる)。「無い」ことの証明はできないので、既存の類似基準をご存知であればissueで教えてほしい。

## Contributing

issue / PR 歓迎です。ただし、特定の組織・プロダクトが識別できる情報(社名、実測値、固有のドメイン語彙など)は書かないでください。知見は一般化した形で共有をお願いします。

## License

TODO: 公開時に決定(CC BY 4.0 を想定)
