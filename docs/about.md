---
cover: assets/img/covers/incident_response_docs.png
---
![PagerDuty](../assets/img/headers/pagerduty_logo.png)


このサイトはPagerDutyのインシデント対応手順を記述しています。
これはPagerDutyにおいて、オンコールを始める従業員や、重大インシデントで利用されている、内部ドキュメントの一部を切り出したものです。
このドキュメントはインシデントに備えるものだけでなく、インシデント発生中、また発生後の対応についても述べています。

重大インシデントへの内部手順を議論している会社は少ないようです。
私達は、PagerDutyの手順をコミュニティに公開して、手順を制定したい人が参考にしてくれることを願いします。
そして、全ての人が助かる改善提案の機会に慣ればと思います。

## これはなに？

このドキュメントには、重大インシデントに効果的な対応方法や、オンコールを効果的に実行するための情報をまとめています。
ハードウェイで学ぶレッスンや、すばやく習得できるトレーニング資料を含みます。

## 誰のためのドキュメント？

これはオンコールを実施する人と、運用インシデント対応に関与している人、またインシデント対応手順を制定したいと思っている人を対象としています。

## なぜ必要か？

インシデント対応は決して必要ないと祈りたいですが、必要になったときはスムーズでシームレスに行いたいです。
通常、社内でのインシデント対応の知見は、ンシデントに遭遇する度に良くなっていきます。
PagerDutyのようなツールは、より早くインシデントから復帰するのに役立ち、インシデント対応する人にとって本当に大事なものに集中できます。
このドキュメントではPagerDutyで数年に渡り積み重ねられたものから、学ぶことができます。
重大インシデントへの対応方法を先取りして、最速の復旧時間を実現します。

## このドキュメントがカバーすること

[オンコール](/oncall/being_oncall.md)の準備や、[深刻度](/before/severity_levels.md)の定義、インシデント呼び出しの[エチケット](/before/call_etiquette.md)、[post-mortem](/after/post_mortem_process.md)の進め方とテンプレートなどです。
また[セキュリティインシデントの対応手順](/during/security_incident_response.md)もあります。

## このドキュメントがカバーしないこと

これはPagerDutyの内部ドキュメントの複製ではなく、いくつかの情報が削除されています。
電話番号、オープンソース化してない内部ツールやシステム名、ダッシュボードの画像などです。
基本的にはPagerDuty特有のものや共有できないものはありません。

## License

この邦訳、および原文の[PagerDuty Incident Reponse](https://response.pagerduty.com/)はApache License 2.0以下で配布されています。
このドキュメントの編集や利用して、商用およびプライベート利用が可能です。
その場合は元のコピーライトと、LICENSEファイルを含んでください。

PagerDutyの顧客であってもなくても、このドキュメントをあなたの社内で使えるようにしたいです。
このドキュメントのソースコードはGitHub上で公開されており、自由にフォークや独自の内部ドキュメントのベースに利用できます。

This documentation is provided under the Apache License 2.0. In plain English that means you can use and modify this documentation and use it both commercially and for private use. However, you must include any original copyright notices, and the original LICENSE file.

Whether you are a PagerDuty customer or not, we want you to have the ability to use this documentation internally at your own company. You can view the source code for all of this documentation on our GitHub account, feel free to fork the repository and use it as a base for your own internal documentation.
