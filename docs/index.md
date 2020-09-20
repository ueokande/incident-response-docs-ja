---
cover: assets/img/covers/incident_response_docs.png
---
![Incident Response at PagerDuty](./assets/img/headers/pagerduty_ir.jpg)

このドキュメントは、PagerDutyにおけるインシデント対応プロセスが載っています。
重大重大インシデントや、新しくオンコールを始める社員の準備に利用している、PagerDutyの内部ドキュメンの一部を切り出したものです。
このドキュメントではインシデントに備えることだけではなく、インシデント発生中、また収束後の対応についても説明します。
オンコールを担当する人や、インシデント対応プロセスに関与する人（またきちんとしたインシデント対応プロセスを制定したい人）が読むことを想定しています。
このドキュメントが何なのか、なぜ存在するかは、[「このドキュメントについて」](about.md)を参照してください。

!!! tip "どこから手を付けるべきか？"
    もしあなたがインシデント対応が初めてで、組織的な手順がない場合は、まず[「はじめに」](/getting_started.md)で何ができるかを確認してください。
    そして詳細な手順を、[Training Course](training/courses/incident_response.md)から確認することをお勧めします。

## オンコールを始める

まだあなたがオンコールを体験していないのなら、それが何なのかが疑問に思うかも知れません。
このページでは、オンコールに期待されていることと、いくつかの実例を紹介します。

* [オンコールを始める](oncall/being_oncall.md) - _オンコールを始めるには。あなたの責務とそうでないもの_
* [アラートの原則](oncall/alerting_principles.md) - _エンジニアを呼び出すための手段やタイミングなどの原則_

## インシデント発生前

インシデントが発生する前に読むべきものです。
実際にインシデントが発生してから読むものではないでしょう。

* [インシデントとはなにか？](before/what_is_an_incident.md) - _インシデント対応の議論の前に、インシデントとは何なのか？_
* [深刻度レベル](before/severity_levels.md) - _深刻度レベルの分類。SEV-3とSEV-1の違いや、それぞれの対処方法_
* [インシデント発生時の役割](before/different_roles.md) - _インシデントコマンダー（Incident Commander）、記録係（Scribe）などの、インシデント対応中の役割_
* [インシデント通話のエチケット](before/call_etiquette.md) - _インシデント通話に参加するまでに知っておくべきエチケット_
* [複雑なインシデント](before/complex_incidents.md) - _大規模で複雑なインシデントに立ち向かうための手引き_

## インシデント発生中

重大インシデント発生中の、情報と手順を紹介します。

* [インシデント発生中](during/during_an_incident.md) - _インシデント発生中に何をすべきか、どう貢献すべきか_
* [セキュリティインシデント](during/security_incident_response.md) - _セキュリティインシデントでは通常のインシデントと扱い方が異なります_

## インシデント収束後

フォローアッププロセスでは、再発防止に何ができるかなどを確認し、日々改善をします。

* [インシデント収束後](after/after_an_incident.md) - _インシデントが解決したあとにやること_
* [ポストモーテムプロセス](after/post_mortem_process.md) - _ポストモーテムの手順について、何が関係してどうやって書くか_
* [ポストモーテムテンプレート](after/post_mortem_template.md) - _重大インシデントに対するポストモーテムで使っているテンプレート_
* [効果的なポストモーテム](after/effective_post_mortems.md) - _効果的なポストモーテムを書くためのガイド_

## トレーニング

それではインシデント対応について学びたいですか？
あなたは正しい場所にたどり着きました。

* [トレーニング概要](training/overview.md) - _私たちのトレーニングガイドの概要と、3rdパーティーのトレーニング資料_
* [インシデント対応の用語集](training/glossary.md) - _インシデント対応中に使われる用語と定義_

### トレーニングガイド

* [インシデントコマンダーのトレーニング](training/incident_commander.md) - _次のインシデントコマンダーになるためのガイド_
* [補佐のトレーニング](training/deputy.md) - _補佐になりインシデントコマンダーをバックアップするためのガイド_
* [記録係のトレーニング](training/scribe.md) - _記録係のためのガイド_
* [内容領域専門家のトレーニング](training/subject_matter_expert.md) - _重大インシデント発生中の、全ての参加者への責務と振る舞いのガイド_
* [顧客連絡のトレーニング](training/customer_liaison.md) - _インシデント発生中に外部への告知するためのガイド_
* [内務窓口のトレーニング](training/internal_liaison.md) - _インシデント発生中に、社内チームと連携するためのガイド_

### トレーニングコース

* [Incident Response Training Course](training/courses/incident_response.md) - _インシデント対応とインシデントコマンダーの役割の入門コース（英語）_

## 追加資料

インシデント対応に関する、外部の資料とリソースです。

* [読み物](resources/reading.md) - _インシデント対応に関連する、お勧めの読み物_
* [ChatOps](resources/chatops.md) - _ドキュメントで参照しているチャットBotのコマンドについて_
* [アンチパターン](resources/anti_patterns.md) - _試してみてダメだったものや、その失敗からの学び_
