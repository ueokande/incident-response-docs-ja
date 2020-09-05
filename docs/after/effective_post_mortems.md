---
cover: assets/img/covers/blameless.png
description: Writing an effective post-mortem allows us to learn quickly from our mistakes and improve our systems and processes for everyone. We want to be sure we're writing detailed and accurate post-mortems in order to get the most benefit out of them. This guide lists some of the things we can do to make sure our post-mortems are effective.
---

効果的なポストモーテムを書くことで、ミスに早く気づき、私たちのシステムとプロセスの全てを改善できます。
私たちは最大限の恩恵を受けるため、詳細かつ正確なポストモーテムを書くことを心がけています。
このガイドではポストモーテムが効果的になるようないくつの事柄を説明します。

## やること

* タイムラインがイベントに対して正確であることを確認してください。
* 新しくチームに入った人が理解できるように、技術用語や略語を説明してください。
* [インシデントによって、サービスの正常性や回復性への理解につながるか議論します。](https://www.pagerduty.com/blog/postmortem-understand-service-reliability/).

## やらないこと

* 本当にサービスが停止した場合を除き「停止」という言葉は使わないでください。
  私たちはインシデントの影響を正確に反映したいので、「停止」という言葉は意味が広いです。
  また顧客に対して何もできなかったと思わせることになります。
* 「見栄えを良くする」ために詳細やイベントを書き換えないでください。
  効果的なポストモーテムにならないので、自分自身にも正直である必要があります。
* 名前を挙げたり恥をかかせないようにしてください。
  ポストモーテムは誰かを責めないようにします。
  もし誰かが壊れる変更をデプロイしても、それは彼らの失敗ではなく、破壊的な変更ができるシステムである我々の責任です。


## 推奨事項

* 「ヒューマンエラー」という概念を避けます。
  これは上記の「名前を挙げたり恥をかかせない」と言うのに関連してますが、微妙な違いがあります。
  人に起因するミスはとても稀で、多くの場合は対処すべき要因があります（たとえば、人間が実行するスクリプトにレートリミットが無かったり、ドキュメントが古かったり）。
* タイムライン、または説明の節で、仮定の話は避けます。
  たとえば「早朝からサービスXのトラフィック増加が確認でき、リクエストへの応答が停止した。 _*もしサービスXに*_ レートリミットがあれば、リクエストに失敗 _*していないだろう*_。」「今晩にサービスXのレスポンスが遅くなり始めました。これはCPU使用率の上昇を検知する _*モニタリングが不十分*_ でした。」
  この2つの例は実際に起きた問題と、対策の仮定を混同して議論しています。
  これらは別々に適切に議論できるようにします。
* 以下のビデオは上記の点について詳しく説明しています。
    * "[Three analytical traps in accident investigation](https://www.youtube.com/watch?v=TqaFT-0cY7U)"
    * "[Two views on Human Error](https://www.youtube.com/watch?v=rHeukoWWtQ8)"

## レビュー

設定したミーティングの前にレビューできるSlackルームがあります。
以下の観点でレビューします。

* 詳細が十分に説明されているか？
* 問題の原因を指し示すだけでなく、問題の根本原因まで掘り下げて議論されているか？
* 「何が起こったか」と「どう修正するか」を分けて説明できてるか。
* ポストモーテムが理解できるように書かれているか？
* 外部への告知メッセージは顧客が納得できるか、怒らせてしまわないか？

ポストモーテムのレビューは単なるタイポを指摘するだけではありません（外部告知にはスペルミスがないことを確認する必要があります）。
最大限の恩恵を受けるための、価値のある変更ができる建設的なフィードバックを提供します。

## 例

以下に他社のポストモーテムの例を示します。

* [Stripe](https://support.stripe.com/questions/outage-postmortem-2015-10-08-utc)
* [LastPass](https://blog.lastpass.com/2015/06/lastpass-security-notice.html/comment-page-2/)
* [AWS](https://aws.amazon.com/message/5467D2/)
* [Twilio](https://www.twilio.com/blog/2013/07/billing-incident-post-mortem-breakdown-analysis-and-root-cause.html)
* [Heroku](https://status.heroku.com/incidents/151)
* [Netflix](http://techblog.netflix.com/2012/10/post-mortem-of-october-222012-aws.html)
* [GOV.UK Rail Accident Investigation](https://www.gov.uk/government/publications/kyle-beck-safety-digest/near-miss-at-kyle-beck-3-august-2016)
* [A List of Post-mortems!](https://github.com/danluu/post-mortems)

## 役立つ情報

* [Advanced PostMortem Fu and Human Error 101 (Velocity 2011)](http://www.slideshare.net/jallspaw/advanced-postmortem-fu-and-human-error-101-velocity-2011)
* [Blame. Language. Sharing.](http://fractio.nl/2015/10/30/blame-language-sharing/)
