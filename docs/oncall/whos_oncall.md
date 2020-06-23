---
cover: assets/img/covers/whos_on-call.png
description: Organizational structures vary, but these are general guidelines about the way different functions in a business relate to incident response.
---
![Who's On-Call?](../assets/img/headers/who_oncall.png)

組織構造には様々ありますが、インシデント対応に関係するビジネス上の方法に関する、ガイドラインがいくつかあります。

一般的には、全ての部門には、連絡できる窓口や、オンコールローテーション、明確なエスカレーションパスなどを用意すべきです。
組織は常に、依存関係を最小にして、対応チームに可能な限りの権限を与えるべきすが、今までにない状況では誰に助けを求めるべきかわかりません。
: clear system for recruiting responders from all parts of the business ensures that when the unexpected happens, responders don’t waste time on manual processes or ambiguous points of contact.

## エンジニア

エンジニアは典型的な、インシデントの対応社で、[内容領域専門家](../before/different_roles)でもあります。
どのエンジニアリングチームがどの対応に関係するかは、会社の運用モデルによって異なります。
場合によっては「運用」「サイト・リライアビリティ・エンジニアリング」チームが、トリアージと問題の評価の初期対応をする場合があります。
PagerDutyでは、影響するサービスのオンコールのエンジニアが、最初のトリアージと問題の評価をします。

## カスタマーサポート/カスタマーサクセス

サポートは障害対応中には、顧客の声となります。
カスタマーサポートチームのメンバーは、対応チームの初期の顧客窓口([Customer Liaison](../training/customer_liaison))となり、Twitterや内部Slackなどを通して、顧客の障害対応の状況を更新します。
また社内のステークホルダーにも、内部の窓口としての役割を果たすこともあります。

## マーケティング

マーケティングや広報は、広報でのインシデントに対応する最初のチームです。

そしてマーケティングや広報は、会社のブランディングやイメージを損なう重大なリスクを伴うインシデントへの対応や、一斉送信メールや会社ブログを通じて顧客にアップデート情報を通知することもあります。

## プロダクトマネージャーとデザイナー

プロダクトマネージャーとデザイナーは、複数サービスや複数製品に影響する場合に、対応チームの意思決定を助ける役目があります。
たとえば対応チームが最初に復旧するサービスを決める時、プロダクトマネージャーはどのサービスが顧客に影響があるかを考慮します。

またプロダクトマネージャーは[post-mortem](../after/post_mortem_process)にも関与して、
問題を解決するために修正が必要な製品に対して、フォローアップのスケジューリングやアドバイスなどをします。

## 経営陣


重大なインシデントに対応している時、組織のリーダーシップが必要な背景と情報を知らせることで、経営陣が[現場に飛び込んでくる](../training/glossary/#executive-swoop)ことを防ぎます。
インシデントの司令官はインシデント対応中の最終決定の権限を持ちますが、重大なインシデントでは会社の最高レベルのアクションが求められる場合があります。
For example, a senior executive may want to reach out to an impacted customer or partner to manage their relationship and help assure them the issue is getting the attention it needs.

## 営業

営業は一般的に、インシデント対応中のステークホルダーとなります。
デモや顧客との会話に影響するような場合には営業担当者に知らせる必要がありますし、アカウントの所有者は影響を知っておく必要があります。

## 人事

人事は一般的に、従業員の健康や安全を脅かすインシデント対応に取り組む必要があります。
さらにセキュリティインシデントでは、セキュリティチームは内部攻撃者と従業員の保護のために、人事と連携することもあります。

## 経理

経理はインシデント対応中のステークホルダーとなることが多く、請求、会計、または月ごと、4半期ごとの処理への影響を常に考える必要があります。

However, finance should also have a clear on-call rotation and escalation path, as there may be components of incident response that require third-party account management or related actions.

!!! tip "組織全体を考えてください"
    対応者またはステークホルダーとして、インシデント対応が必要な他の部署があるかもしれません。
    業務の様々な分野を特定し、その状況で誰が関係するかを考えるのは大事です。
    そしてオンコールを受け取る誰もが、適切なインシデント対応のトレーニングと責務を理解することが重要です。
