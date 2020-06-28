---
cover: assets/img/covers/severity_levels.png
description: Incidents are typically classified by severity or priority. At PagerDuty we use 'SEV' levels, with lower numbered severities being more urgent. Operational issues can be classified at one of these severity levels, and in general you are able to take more risky moves to resolve a higher severity issue.
---

どのようなインシデント対応手順でも最初のステップは、何が[インシデントを引き起こしている](/before/what_is_an_incident.md)かを特定することです。
その後インシデントは重要度によって種類分けされ、通常は低い数字になると緊急度が高くなる "SEV" 定義が利用されます。
運用上の問題はこの深刻度レベルによって分類され、深刻度の高い問題を解決するために、リクスの高い行動をトルことができます。
SEV-3とり深刻なものは自動で重大インシデント (Major Incident) とみなされ、通常インシデントよりも集中的な対応がとられます。

!!! tip "常に最悪の場合を考える"
    もしインシデントがどれに分類されるかわからない場合（たとえば、SEV-2かSEV-1かわからない場合など）は、より深刻度の高いものとして扱います。
    インシデント対応中は、深刻度を議論したり決めたりする時間ではありません。
    重要度の高いものとして扱い、post-mortemで振り返りましょう。

!!! question "SEV-3は重大インシデントか？"
    全てのSEV-2は重大インシデントですが、全ての重大インシデントがSEV-2である必要はありません。
    低い深刻度の問題であっても、連携した対応が必要な場合は、インシデント対応手順を発動するのです。
    インシデント司令官がインシデント対応が必要かどうかを判断します。

<table class="custom-table">
  <thead>
    <tr>
      <th class="sev">深刻度</th>
      <th>解説</th>
      <th>典型的な対応</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td class="sev-1">SEV-1</td>
      <td>
        <p class="intent">外部への通知と幹部との連絡が必要な、致命的な問題</p>
        <ul>
          <li>システムは致命的な状態で、多くの顧客に影響がある状態。</li>
          <li>長期的にわたり機能的に利用できず、SLAを破っている。</li>
          <li>顧客データが漏洩する可能性のある脆弱性が報告されている。</li>
        </ul>
      </td>
      <td>
        <p class="response">重大インシデント対応</p>
        <ul>
          <li>Slackでインシデント司令官を呼び出す<code>!ic page</code>.</li>
          <li><a href="/during/during_an_incident">インシデント対応中</a>を読む</li>
          <li>社内のステークホルダーに通知する</li>
          <li>外部へ通知する</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td class="sev-2">SEV-2</td>
      <td>
        <p class="intent">顧客が製品を利用するのに影響がある致命的なシステムの問題</p>
        <ul>
          <li>通知パイプラインに重大な障害が発生している。</li>
          <li>インシデント対応の機能(応答、解決、など)が利用できない。</li>
          <li>Webアプリが利用できないか、多くのユーザーにパフォーマンス劣化が発生している。</li>
          <li>重大インシデントに対するPagerDutyの監視システムが停止している</li>
          <li>PagerDutyの従業員がインシデント対応が必要だとみなしたイベント</li>
        </ul>
      </td>
      <td>
        <p class="response">重大インシデント対応</p>
        <ul>
          <li>Slackでインシデント司令官を呼び出す<code>!ic page</code>.</li>
          <li><a href="/during/during_an_incident">インシデント対応中</a>を読む</li>
        </ul>
    </tr>
    <tr>
      <td class="warning" colspan="3">このラインを超えるのは「重大インシデント」と扱います。我々のインシデント対応手順は、あらゆる重大インシデントに対して発動されるべきです。</td>
    </tr>
    <tr>
      <td class="sev-3">SEV-3</td>
      <td>
        <p class="intent">サービス所有者が直ちに対応する必要がある、安定性や一部の顧客に影響がある軽微な問題。</p>
        <ul>
          <li>一部の機能が使えないが、多くの顧客には影響しない。</li>
          <li>何もしなければSEV-2になる可能性があるもの。</li>
          <li>サービスの冗長度がないもの（もう1つのノードが停止すると障害になる）</li>
        </ul>
      </td>
      <td>
        <p class="response">サービスチームへの緊急度の高い呼び出し</p>
        <ul>
          <li>最優先で問題に取り掛かる。</li>
          <li>影響するシステムのエンジニアと連絡をとり、原因の特定する。</li>
          <li>最近の開発によるものならロールバックする。</li>
          <li>ステータスを監視して事態が悪化しているか、いつから悪化しているかを知らせる。</li>
          <li>エスカレーションする可能性のある人にSlackで通知する。</li>
          <li>必要ならインシデント対応を発動する(<code>!ic page</code>)。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td class="sev-4">SEV-4</td>
      <td>
        <p class="intent">顧客が製品を使うのには影響しない、軽微な問題</p>
        <ul>
          <li>パフォーマンス問題（遅延など）</li>
          <li>1つのホストでの障害（クラスタから1つのノードが抜けるなど）</li>
          <li>遅延したジョブによる障害（イベント、通知パイプラインには影響しない）</li>
          <li>Cronの障害（イベント、通知パイプラインには影響しない）</li>
        </ul>
      </td>
      <td>
        <p class="response">サービスチームへの緊急度の低い呼び出し</p>
        <ul>
          <li>最優先で問題に取り掛かる（通常のタスクよりも上）。</li>
          <li>ステータスを監視して事態が悪化しているか、いつから悪化しているかを知らせる。</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td class="sev-5">SEV-5</td>
      <td>
        <p class="intent">製品を利用する顧客には影響しない、表面的な問題やバグ</p>
        <ul>
          <li>システムを使う上で即座に影響しないバグ</li>
        </ul>
      </td>
      <td>
        <p class="response">JIRAチケット</p>
        <ul>
          <li>JIRAチケットを作成して影響のあるシステムの所有者に割り当てる。</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

!!! note "具体的に"
    これらの緊急度の記述は、PagerDuty内部で使われている定義から、より一般的な説明に置換されています。
    あなたたちの独自のドキュメントでは、ユーザーやアカウントの何%に影響するかなどを参考にして、具体的な独自の定義を作ることをお勧めします。
    通常は、メトリックに基づく深刻度の定義が望ましいです。
