---
cover: assets/img/covers/training_overview.png
title: Training Overview
description: PagerDutyの重大インシデント対応プロセスを学ぶことは、PagerDutyで効率的なオンコールエンジニアになるために重要なことです。
このセクションでは、インシデント対応における様々な役割に対するトレーニング資料と、政府機関からの追加情報とトレーニング資料を紹介します。
---

PagerDutyの重大インシデント対応プロセスを学ぶことは、PagerDutyで効率的なオンコールエンジニアになるために重要なことです。
このセクションでは、インシデント対応における様々な役割に対するトレーニング資料と、政府機関からの追加情報とトレーニング資料を紹介します。

## トレーニングガイド

トレーニングガイドはそれぞれの役割ごとに分けられていますが、その役割に属していなくても読むことをお勧めします。
重大インシデントで彼らがどのようなことをしているかを理解できます。

* [インシデントコマンダーのトレーニング](/training/incident_commander.md) - インシデントコマンダーは重大インシデントを解決に導きします。彼らは他の人を支持する人です。
* [補佐のトレーニング](/training/deputy.md) - 補佐はインシデントコマンダーをサポートしたり、必要に応じて作業を引き継ぎます。
* [記録係のトレーニング](/training/scribe.md) - インシデント発生中に、記録係として担当する人を対象とします。
* [内容領域専門家/解決者のトレーニング](/training/subject_matter_expert.md) - これはチームでオンコールを担当するPagerDutyの全ての人が対象となります。
* [顧客連絡のトレーニング](/training/customer_liaison.md) - 外部に告知して顧客とやり取りする人を対象とします。
* [内部連絡のトレーニング](/training/internal_liaison.md) - これはインシデント発生中に、社内のチームと協力する可能性がある全ての人に関係します。

## トレーニングコース

私たちは一部のトレーニングコースのスライドやビデオも公開しています。
もともとはPagerDuty内部で使っていたものですが、より広く使えるようにしたので、あなたの組織にも利用できます。

* [インシデント対応トレーニングコース](/training/courses/incident_response.md) - インシデント対応とインシデントコマンダーの役割に関する入門コース。

## インシデントの例

この通話記録は、[2017年1月](https://status.pagerduty.com/incidents/510k1bnvwv6g)にPagerDutyで発生した重大インシデントを再現したものです。
簡略化とプライバシーの観点で詳細な部分は変更されていますが、それ以外の部分は当時のインシデントのままです。
この記録の詳細については、[PagerDutyのブログ](https://www.pagerduty.com/blog/incident-response-reenactment/)に載っています。

<iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/vw6I5DYWkNA?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

## National Incident Management System : NIMS

私たちのインシデント対応プロセスは、ほぼ[National Incident Management System : NIMS](https://www.fema.gov/national-incident-management-system)に基づいています。

_生命、財産、そして環境への影響を減らすために、政府機関、非政府機関、そして民間部門における、全てのレベルの部門や機関をシームレスに連携し、根本原因、規模、場所、複雑度など、全ての脅威や危険をもたらすインシデントを管理するための、体系的かつ危険予測するアプローチ。_

最初はこれはITの運用環境には適用できないと思われていたが、これらの状況をもたらす重大インシデントからの学びで、私たちの業界にも直接適用できるということを学びました。

[![NIMS](../assets/img/thumbnails/nims_core.png)](https://www.fema.gov/pdf/emergency/nims/NIMS_core.pdf) [![NIMS Training](../assets/img/thumbnails/nims_training.png)](https://www.fema.gov/pdf/emergency/nims/nims_training_program.pdf)

もしNIMOについて詳しく知りたいのなら、[ICS-100](https://training.fema.gov/is/courseoverview.aspx?code=IS-100.b) と [ICS-700](https://training.fema.gov/is/courseoverview.aspx?code=IS-700.a) のオンライントレーニングを受けることをお勧めします。
これらのコースではNIMSとインシデントコマンダーシステム（FEMAから認証を得るためにトレーニング後にオンライン試験があります）について学ぶことができます。
またNIMSには[FEMAによる追加トレーニング資料](https://training.fema.gov/nims/)があるので、そちらもご覧ください。

もしUSを拠点として、コミュニティ内でインシデント対応ロールを引き受ける場合には、[CERT（Community Emergency Response Teams）プログラム](https://www.fema.gov/community-emergency-response-teams)について調べることをお勧めします。
多くの都市がCERTトレーニングを実施しており、コミュニティ内でCERTコントリビューターとしてボランティアができます。
現実世界での災害対応を経験するだけでなく、そのスキルを日常生活で活かすこともできます。

[追加情報](/resources/reading)もご覧ください。

## 世界のインシデント対応

NIMSはUSのインシデント対応フレームワークですが、多くの国で独自のフレームワークがあります。
一部はUSのシステムを元にしてるものもありますが、ほとんどは独自のものが多いです。
世界各国で使われているメソッドとフレームワークを調査することで新たな学びもあります。


"[Comparative Emergency Management: Understanding Disaster Policies, Organizations, and Initiatives from Around the World](https://training.fema.gov/hiedu/aemrc/booksdownload/compemmgmtbookproject/)"（[FEMA website](https://training.fema.gov/hiedu/aemrc/)から入手可能）という本は、30カ国ほどで利用されているシステムを比較し、世界中で利用されている危機管理フレームワークについての情報が載っています。

ここでは私たちPagerDuty内のプロセスに適合して改善するために調べたいくつかのシステムを紹介します。

### イギリス

イギリスの危機管理システムは、[**Gold-Silver-Bronze Command Structure**](https://en.wikipedia.org/wiki/Gold%E2%80%93silver%E2%80%93bronze_command_structure)と呼ばれるコマンド階層を遣います。
このフレームワークは、戦略的（ゴールド）、戦術的（シルバー）、運用（ブロンズ）の、コマンドの決定をする責務3つのレベルが含まれます。

詳細については以下の資料をご覧ください。

* [UK.GOV - Emergency Response and Recovery](https://www.gov.uk/guidance/emergency-response-and-recovery).
* [UK.GOV - Incident Command - 3rd Edition (2008)](https://www.gov.uk/government/publications/fire-and-rescue-manual-volume-1-incident-command).
* [UK Home Office - Critical Incident Management](https://assets.publishing.service.gov.uk/government/uploads/system/uploads/attachment_data/file/735103/critical-incident-management-v12.0ext.pdf) (PDF).


### ニュージーランド

ニュージラーンドには[**Coordinated Incident Management System (CIMS)**](https://en.wikipedia.org/wiki/Coordinated_Incident_Management_System)と呼ばれるシステムがあり、USのインシデントコマンドシステム (Incident Command System : ICS) に基づいています。
CIMSで特に私たちが気に入った部分は、一般的な用語に重点を置いていることで、インシデント発生中の混乱を防いで迅速かつ効率的な対応を可能にしています。
いくつかの用語はICSから変更があります（たとえば"Command"ではなく"Control"にするなど）が、馴染み深いものです。


詳細については以下の資料をご覧ください。

* [Ministry of Civil Defence & Emergency Management - New Zealand Coordinated Incident Management System (CIMS)](https://www.civildefence.govt.nz/resources/new-zealand-coordinated-incident-management-system-cims-2nd-edition/) ([PDF](https://www.civildefence.govt.nz/assets/Uploads/publications/CIMS-2nd-edition.pdf)).
* [Devereux-Blum Training & Development - Emergency Management Training](https://www.emergencymanagement.co.nz/)

### オーストラリア

オーストラリアの[**Australasian Inter-Service Incident Management System (AIIMS)**](https://en.wikipedia.org/wiki/Australasian_Inter-Service_Incident_Management_System)は、USのNIMSから派生したものです。
ICSをベースにしているので、AIIMSは他のフレームワークよりも _管理範囲_ に重点を置いています。
ニュージーランドのシステムのように、用語の使い方にいくつかの相違点があります（たとえば"Incident Commander"ではなく"Incident Controller"など）が、ICSを知っている人には馴染みがあります。

詳細については以下の資料をご覧ください。

* [The Australasian Inter-Service Incident Management System, 3rd Edition](https://training.fema.gov/hiedu/docs/cem/comparative%20em%20-%20session%2021%20-%20handout%2021-1%20aiims%20manual.pdf) (PDF).
* [Incident Management in Australia Handbook](https://knowledge.aidr.org.au/resources/handbook-14-incident-management-in-australia/)

### カナダ

カナダでは独自の[**Incident Command System**](http://www.icscanada.ca/images/upload//ICS%20OPS%20Description2012.pdf)があります。
この規格は[ICS Canada](http://www.icscanada.ca/en/home.html)と呼ばれる組織たちによって管理されておりいます。
このウェブサイトにはカナダの州にごとに応じて、トレーニングコースを見つける方法が載っています。

詳細については以下の資料をご覧ください。


* [ICSCanada - I-100 Introduction to Incident Command System](http://www.aema.alberta.ca/documents/studentreferencenote86439.pdf) (PDF).
* [Canada ICS Forms](http://www.icscanada.ca/en/Forms.html) - _ダウンロードして各自のインシデントに利用できる標準ICSフォーム（同様のものが[FEMA](https://training.fema.gov/icsresource/icsforms.aspx)にもあります）_
