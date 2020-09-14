---
cover: assets/img/covers/incident_response_docs.png
---
![PagerDuty](../assets/img/headers/pagerduty_logo.png)


このサイトはPagerDutyの障害対応プロセスの一部をドキュメント化しました。
これはPagerDutyの全ての重大インシデントで使用している、全ての新入オンコールエンジニアが利用している、社内ドキュメントの縮小版です。
インシデントの中日だけではなく、インシデント発生中やインシデント収束後についても述べています。

重大インシデントを取り扱うプロセスについて議論している企業は少ししかありません。
私たちのドキュメントコミュニティに後悔して、独自のプロセスを策定したい人にとって役立つことを期待します。
また他の人に改善を提案できる機会を提供し、それがみんなの助けになることでしょう。

## これは何ですか？

A collection of pages detailing how to efficiently deal with any major incidents that might arise, along with information on how to go on-call effectively. It provides lessons learned the hard way, along with training material for getting you up to speed quickly.

## これは誰のためですか？

It is intended for on-call practitioners and those involved in an operational incident response process, or those wishing to enact a formal incident response process.

## なぜ必要ですか？

インシデント対応は絶対に必要ないと願いたいですか、もしやる必要がある場合は、スムーズかつシームレスに済ませたいです。
通常、社内でのインシデントの対応方法は、時間とともに蓄積されて、インシデントとともに改善されています。
[PagerDutyの重大インシデント向けのアプリケーション](https://www.pagerduty.com/applications/#major-incidents-application)などのツールは問題の迅速な収束に役立ちますが、実行するプロセスもまた重要です。
このドキュメントにより、私たちが数年にもわたり築き上げてきたものを最初から学ぶことができます。
可能な限り最短の復旧時間を実現できる、重大インシデントの扱い方を先取りできます。


## 何がカバーされていますか？

[オンコール](/oncall/being_oncall.md)へのなり方、[深刻度](/before/severity_levels.md)の定義、インシデントの[通話中のエチケット](/before/call_etiquette.md)、[ポストモーテム](/after/post_mortem_process.md),の方法、[ポストも〜テムのテンプレート](/after/post_mortem_template.md)などが含まれます。

## なにがカバーされていないですか？

これは社内ドキュメントの複製ですが、一部の状態が削除されています。
電話番号、（まだ）オープンソース化されていない内部ツールとシステムの名前、ダッシュボードの画像などです。
基本的にはPagerDuty固有の情報や、秘密情報が含まれている元は濃ゆ有していません。

## License

このドキュメントはApache License 2.0の元で提供されます。
このドキュメントの仕様および変更ができ、商用および個人利用の両方ができます。
ただし元の著作権情報と、元のLICENSEファイルを含める必要があります。

PagerDutyの顧客であろうとなかろうと、このドキュメントを自社の内部で使用できるようにします。
PagerDutyのGitHubアカウントで、全てのドキュメントのソースコードを閲覧できます。
レポジトリをフォークして、独自のドキュメントのベースとして自由に利用できます。
