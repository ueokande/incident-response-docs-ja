---
cover: assets/img/covers/post-mortem_process.png
description: For every major incident (SEV-2/1), we need to follow up with a post-mortem. A blame-free, detailed description, of exactly what went wrong in order to cause the incident, along with a list of steps to take in order to prevent a similar incident from occurring again in the future.
---
![Post-Mortem](../assets/img/headers/pagerduty_post_mortem.jpg)

全ての重大インシデント (SEV-2/1) において、post-mortemでフォローアップが必要です。
誰かのせいにせず、より詳細で、正確に何がインシデントを引き起こしたかの説明と、将来似たようなインシデントが再発しないための手順のリストを記述します。
またその時のインシデント対応手順も含める必要があります。
A blame-free, detailed description, of exactly what went wrong in order to cause the incident, along with a list of steps to take in order to prevent a similar incident from occurring again in the future. The incident response process itself should also be included.

!!! warning "Post-Mortemを軽視しないで"
    インシデント後のpost-mortemをおろそかにしないでください。
    post-mortemが無いと、何が正しいのか、どこが改善できるのか、そして最も重要な再発防止の方法がわからなくなります。
    よく設計された、誰も責めないpost-mortemは、チームに継続的に学ぶ機会をあたえ、インフラとインシデント対応手順を反復的に改善できます。


## オーナーの指名

最初のステップは、post-mortemのオーナーを指名することです。
これはインシデント・コマンダーが、大規模インシデント呼び出しの終了後または直後に行われます。
もしあなたがpost-mortemのオーナーなら、インシデント・コマンダーから直接指名されます。
オーナーはpost-mortemの記録し、ログをさかのぼり、フォローアップの調査を管理し、全ての関係ある人に情報を提供する責務があります。
詳細ステップのリストは次で説明します。

## オーナーの責務

post-mortemのオーナーであるあなたは、以下の責務があります

* post-mortemのミーティングを（共有カレンダーで）設定し、関係のある人を招待します（SEV-1の場合は**3営業日以内**に、SEV-2の場合は**5営業日以内**にすべきです）。
* インシデントの調査をし、他のチームから調査を手助けできそうな人を引き抜きます。
* 必要な内容をまとめてページを更新します。
* フォローアップ用のJIRAチケットを作ります（_あなたの責務はJIRAチケットを作ることであって、解決のためのフォローアップをすることではないです_）。
* ミーティング前に関係者とpost-mortemのレビューをする。
* post-mortemのミーティングでトピックについて説明する（インシデントコマンダーがミーティングの進行をするが、実際はあなたがほとんど話すだろう）。
* post-mortemの結果を内部に伝える

## ステータスの記述

我々のpost-mortemsは、post-mortemsの現在どのステップ化を表す "Status" フィールドがあります。
我々は以下のステータスを使います。

| **Draft**     | post-mortemの内容をまだ書いている途中です
| **In Review** | post-mortemの内容が完了して、post-mortemのミーティングでレビュー可能です
| **Reviewed**  | ミーティングが終了して、内容がレビューされ内容が確認されました。<br/>
                  もし外部への告知がある場合は、カスタマーサポートチームが告知をして、ステータスページを適切に更新します。
| **Closed**    | post-mortemに関する新たなアクションはありません（まだ解決してない問題はJIRAで追従されます）<br/>
                  もし外部への告知がない場合は、メーティングが終わるとすぐにこのステータスをスキップできます。
                  もし外部への告知がある場合は、サポートチームが告知を出してからサポートチームがステータスを更新します。

## Post-Mortem

あなたはpost-mortemのオーナーに指名されました。
まずは関連する情報から、post-mortemの作成と更新をしてみましょう。

1. （まだインシデントコマンダーによって作られてなければ）インシデントに対する新たなpost-mortemを作成します。

1. SEV-1の場合は **3営業日** 以内に、SEV-2の場合は **5営業日** 以内に、post-mortemのミーティングを設定します。
post-mortemを埋める前にミーティングを設定したほうが良いです。カレンダーに載るから。
    * ミーティングは、共有の"Incident Post-Mortem Meetings"カレンダーに設定します

1. 持っている全ての情報を記入します
    * タイムラインに主眼を置くべきです。
        * タイムラインには重要なステータス/影響や、対応者が行った重要なアクションを記入スべきです。
    * Slackの履歴をさかのぼって対応者を特定し、津生きます。
        * 同時にインシデントコマンダーと書記 (Scribe) も特定します

1. post-mortemにより詳細を記入します
    * タイムラインのそれぞれの項目に、データのもととなるメトリクスや、サードパーティのページを特定します。
      たとえばDatadogのグラフ、SumoLogicの検索結果、ツイートなどです。
      タイムラインで説明するものは何でも構いません。
    * インシデント呼び出しのレコードへのリンクを追加します。

1. インシデントの解析を行う
    * 全てのインシデントに関係するデータを記録します。何が原因で、どのくらいの顧客に影響が会ったかなどです。
        * どのようにデータを収集したか確認できるように、データを調べるためのコマンドやクエリも追記すべきです。
    * 顧客への影響を把握します（一般的には、イベントの送信、処理の遅延、通知の遅延などです）
    * インシデントの根本的原因を特定します（なにが起こって、 _なぜ_ 起こったか）。

1. 顧客に送信した告知メッセージを記述します。これは顧客に送信する前に、post-mortemのミーティングで確認します。
    * 本当にサービスが停止している場合を除いて、"outage (停止)" という言葉を使わないでください。
      代わりに"incident (インシデント)" や "service degradation (サービスの劣化)" を使ってください。
      顧客は "outage (停止)"という言葉を見ると最悪の状態だと解釈します。
    * 過去のpost-mortemsの例から、どのようなものを送るべきか確認します。

1. 内部関係者でpost-mortemの内容やスタイルをレビューするために、Slackにpost-mortemへのリンクを投稿します。
   これはミーティングの **24時間以内** を目指すべきです。
    * 経験豊富なpost-mortem執筆者が、詳細の具合やpost-mortemの内容についてフィードバックをくれます。
      これでミーティング中の無駄な時間を回避できます。

1. post-mortemミーティングに参加します（詳細は後述します）

1. フォローアップ用のJIRAチケットを作成します（チケットを作成するために方針を決めたい場合は、議論のためのメモを書き留めておきます）
    * Slackの履歴をさかのぼり、全てのTODO項目を特定します。
    * 全てのチケットに緊急度レベルと日付タグを付与します。
    * インシデントの再発防止のためのアクション。
        * (これはトレードオフかもしれないが、それで構わない。ときには、関心領域がそれに費やす労力に見合わないこともあります)。
    * 我々のインシデント対応手順を良くするアクションを特定します。
    * 多すぎるチケットを作成しないよう気をつけてください。絶対に対応スべき、P0/P1のチケットのみを作成します。

1. インシデントから何を学んだかを社内に連絡します
    * 関係するステークホルダーに、結果と主に何を学んだかをメールします。
    * post-mortemのリンクも含めます

## post-mortemミーティング

このミーティングは通常15-30分で、post-mortemのまとめをすることを目的とします。
我々は、何が起こったのかあ、どうすればよかったか、どのようなフォローアップアクションが必要かを話し合います。
その目的は、事実や解析、また推奨アクションに基づいて意見の相違を見つけ出し、我々の信頼性にまつわる問題を引き起こしている問題を広く認知してもらうことです。

post-mortemミーティングでは以下の人々を招くべきです

* 常に
    * インシデントコマンダー
    * インシデントコマンダーの補佐（いれば)
    * インシデントに関係するサービイスオーナー
    * インシデントに関係する、主要なエンジニアや対応者
    * 影響したシステムのエンジニアリングマネージャー
    * 影響したシステムのプロダクトマネージャー
* 任意
    * カスタマー窓口 (SEV-1インシデントのみ)

インシデントコマンダーがミーティングを進行して議題から逸れないようにすべきです。
しかしpost-mortemオーナーがpost-mortemを通してほとんどシャベルことになるでしょう。

ミーティングの主な議題は以下のとおりです。

1. タイムラインの要約をして、全員が同じページを開いてることを確認します。
1. 重要な点や変わった点を要約します。
1. 問題がどのように発見できたかを議論します。
    * [canary](https://www.pagerduty.com/blog/continuous-build-break-fix-fast#canary-releases)で発見できたか？
    * テストやロードテスト環境で見つかったか？
1. 顧客への影響を議論します。カスタマーのコメントなど。
1. 作成されたアクションの項目についてレビューし、適切かどうか、あるいは追加で必要かどうかなどを議論します。

## 例

他社のpost-mortemの例をいくつか列挙します

* [Stripe](https://support.stripe.com/questions/outage-postmortem-2015-10-08-utc)
* [LastPass](https://blog.lastpass.com/2015/06/lastpass-security-notice.html/comment-page-2/)
* [AWS](https://aws.amazon.com/message/5467D2/)
* [Twilio](https://www.twilio.com/blog/2013/07/billing-incident-post-mortem-breakdown-analysis-and-root-cause.html)
* [Heroku](https://status.heroku.com/incidents/151)
* [Netflix](http://techblog.netflix.com/2012/10/post-mortem-of-october-222012-aws.html)
* [GOV.UK Rail Accident Investigation](https://www.gov.uk/government/publications/kyle-beck-safety-digest/near-miss-at-kyle-beck-3-august-2016)
* [A List of Post-mortems!](https://github.com/danluu/post-mortems)

## 参考文献

* [Advanced PostMortem Fu and Human Error 101 (Velocity 2011)](http://www.slideshare.net/jallspaw/advanced-postmortem-fu-and-human-error-101-velocity-2011)
* [Blame. Language. Sharing.](http://fractio.nl/2015/10/30/blame-language-sharing/)
