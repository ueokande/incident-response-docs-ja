---
cover: assets/img/covers/incident_response_docs.png
---
![Incident Response at PagerDuty (PagerDutyにおけるインシデント対応)](./assets/img/headers/pagerduty_ir.jpg)

このドキュメントは、PagerDutyにおけるインシデント対応手順を紹介します。
これはPagerDutyにおいて、オンコールを始める従業員や、普段のインシデントで利用されている、内部ドキュメントの一部を切り出したものです。
このドキュメントはインシデントに備えるものだけでなく、インシデント発生中、また発生後の対応についても述べています。
オンコールに対応する人や、インシデント対応する人（またはきちんとしたインシデント対応手順を制定したい人）が利用することを想定しています。
このドキュメントがなにか、なぜあるかは、[about page](about.md)を参照してください。

!!! tip "どこから手を付けるべきか？"
    もしあなたがインシデント対応が初めてで、組織で決められた手順がない場合は、まず[Getting Started](/getting_started.md)で何ができるかを確認して、[Training Course](training/courses/incident_response.md)で詳細な手順について確認することをお勧めします

## オンコールになること

まだあなたがオンコールを体験してないのなら、何が肝心か気になりますよね？
以下のページは、オンコールに期待されることをいくつかの実例と共に紹介します。

* [オンコールになること](oncall/being_oncall.md) - _オンコールになるには、あなたの責務とそうでないもの_
* [アラートの原則](oncall/alerting_principles.md) - _エンジニアを呼び出すための手段やタイミングなどの原則_

## インシデント発生前

インシデントが発生する前に読むべきもの。実際にインシデントが発生してからでは読むべきでは無いでしょう。

* [インシデントとはなにか？](before/what_is_an_incident.md) - _インシデント対応について議論する前に、インシデントとは一体なんなのか？_
* [深刻度レベル](before/severity_levels.md) - _ 深刻度レベルの種類分け、SEV-3とSEV-1の違いや、その時の対応方法_
* [インシデント発生時の役割](before/different_roles.md) - _インシデント司令官 (Incident Commander) や補佐 (Deputy) などの、インシデント発生時の役割_
* [インシデント呼び出しのエチケット](before/call_etiquette.md) - _Our etiquette guidelines for incident calls, before you find yourself in one._
* [複雑なインシデント](before/complex_incidents.md) - _大規模インシデントや複雑なインシデントに立ち向かうための手引き_

## インシデント発生中

通常のインシデント発生時の情報や手順

* [インシデント発生](during/during_an_incident.md) - _インシデント発生中に何をすべきか、なにをするのが効果的か_
* [セキュリティインシデントへの対応](during/security_incident_response.md) - _運用的なインシデントとは異なる、セキュリティインシデントへの対応_

## インシデント対応後

対応後の後処理。再発防止や常に改善するためには。

* [インシデント対応後](after/after_an_incident.md) - _インシデントが解決した後に何をすべきか_
* [Post-Mortemのプロセス](after/post_mortem_process.md) - _post-mortemには何を含むべきか、どうやって書くか、そしでどうやって実行するか_
* [Post-Mortemテンプレート](after/post_mortem_template.md) - _主なインシデントで利用しているpost-mortemのテンプレート例_
* [効果的なPost-Mortem](after/effective_post_mortems.md) - _効果的なpost-mortemを書くには_

## トレーニング

インシデント対応について学ぶには。

* [トレーニング概要](training/overview.md) - _トレーニングガイドの概要と、サードパーティーのガイド_
* [用語集](training/glossary.md) - _インシデント対応で用いられる用語とその定義_

### トレーニングガイド

* [インシデント司令官トレーニング](training/incident_commander.md) - _Incident Commanderを磨くには_
* [補佐のトレーニング](training/deputy.md) - 補佐になる方法とIncident Commanderへのバックアップ_
* [記録を付けるトレーニング](training/scribe.md) - _記録をつけるには_
* [Subject Matter Expertトレーニング](training/subject_matter_expert.md) - _主なインシデントに対応している全ての人の、責任と行動ガイド_
* [Customer Liaisonトレーニング](training/customer_liaison.md) - _インシデント発生中に、外部に向けて情報を公開するには_
* [Internal Liaisonトレーニング](training/internal_liaison.md) - _インシデントと内部チームとの連絡をするには_

### トレーニングコース

* [インシデント対応トレーニングコース](training/courses/incident_response.md) - _インシデント対応とIncident Commanderの入門コース_

## 追加情報

インシデント対応に関する外部の資料一覧


* [読み物](resources/reading.md) - _インシデント対応に関するオススメの資料_
* [ChatOps](resources/chatops.md) - _このドキュメントで参照しているChat Botについて_
* [アンチパターン](resources/anti_patterns.md) - _失敗に基づく知見や、採用できなかったパターン_
