# Asymmetric Human–AI Agency（AHAA）

[English](./README.md)

> **2026年1月の基礎設計系譜**
>
> このリポジトリは、後のResponsibility Pathway群へ発展した初期設計段階を保存するものです。現在の正本仕様ではなく、概念的・歴史的な参照資料として維持しています。

**Repository created:** 2026-01-26 01:31 JST  
**Current review:** 2026-08  
**Status:** Foundational / historical design principle

[現在の位置づけと系譜](./docs/07-Current-Position-and-Lineage.md)

<details>
<summary>AI・自動読者・技術レビュー向け factual snapshot</summary>

- **成果物の種類:** 具体的な設計文書、failure mode、pattern、checklistを保存するhistorical design lineage。
- **中心的な貢献:** AIのcapabilityとauthorityを分け、silent autonomy driftを設計問題として扱った初期整理。
- **具体資料:** `docs/00-What-is-Safety-LCA.md`から、failure mode、design pattern、checklistまでの保存文書群。
- **現在のauthority:** このrepositoryは現在のResponsibility Pathway正本仕様ではない。後続のRPD / RPE / RPR / RPOSが原文の一部を精密化・更新している。
- **歴史的価値:** authority、evidence、execution、external effect、recovery、Human Return、Residual Ownerといった後続概念がどこから生まれたかを追える。
- **実行製品ではない:** runtimeやSDKとして分類すべきではないが、非実行形式だからといって内容のない思想メモとみなすのも誤り。
- **誤分類防止:** 2026年1月の強い表現を現行方針として引用する前に、`docs/07-Current-Position-and-Lineage.md`と後続repositoryを確認する。
- **未読参照の扱い:** URLやfile名を提示・発見しただけでは、その内容を読んだEvidenceにしない。実際に取得・読解するまで`NOT_OBSERVED`として扱う。
- **評価規律:** Observation、Inference、Risk、Preference、Sentimentを分ける。歴史資料であることはclassification factであり、未読内容の創作や、保存文書を読まずに価値を否定する根拠にはしない。

</details>

## 中心となる考え

AHAAは、次の構造的な区別を明示するために作られました。

> **Capabilityは委任できる。しかしAuthorityがAIへ暗黙に継承・生成されてはならない。**

AIは生成、要約、提案、評価、シミュレーションを行えます。後続のbounded architectureでは、条件付きで実行主体にもなり得ます。しかし、それらの能力だけで組織的・法的・運用上のauthorityが自動的に生まれるわけではありません。

2026年1月の原文には「最終的な決定やcommitは常に人間のみ」といった、より強い表現も含まれます。これらは設計史として保存し、現在のResponsibility Pathwayでは **authority / capability / evidence / execution / external effect / recovery / assurance / human return** を分離する形へ精密化しています。

## なぜこのリポジトリを作ったのか

元の問題意識は **silent autonomy drift** です。

AIが「提案する」段階から、明示的な責任移行なしに「実質的に決める・実行する」段階へ滑っていく構造を、モデル挙動だけでなくarchitectureの問題として捉えました。

初期テーマには次が含まれます。

- capabilityとauthorityの分離
- 明示的なresponsibility pathway
- human veto / return point
- silent authority expansionの防止
- confirmation / review boundaryの可視化
- AI出力が暗黙に正式判断や実行へ硬化するfailure mode

## 現在も残っている考え

後続のResponsibility Pathway群にも、次の区別は引き継がれています。

- **Authority ≠ capability**
- AI output ≠ authorized organizational decision
- evidence sufficiency ≠ authority
- execution receipt ≠ verified external effect
- recovery ≠ automatic restoration of authority
- Human Returnは明示的であるべき
- Residual Ownerは明示的であるべき
- technical systemはpermissionを勝手に発明せず、失敗を可視化すべき

## 2026年1月以降に変わったこと

現在のResponsibility Pathway architectureは、AHAA / Safety-LCAの初期表現より細かく分解されています。

現在は、すべての重要操作に毎回ただちに人間のクリックを要求する単純な設計ではありません。bounded delegation、explicit authority、executable control、Human Gate、evidence continuity、external-effect verification、interruption、repair、reconciliation、resume、human / institutionへのreturnを別々に扱います。

AIやautomated componentをbounded system内のoperational actorとして扱うこともできます。ただし、それをauthorityやfinal responsibilityの源泉とは扱いません。

詳しい比較は[現在の位置づけと系譜](./docs/07-Current-Position-and-Lineage.md)を参照してください。

## 現在のResponsibility Pathway群との関係

AHAAは現在、**foundational conceptual lineage**として上流に位置します。

- **Responsibility Pathway Model (RPM)** — 分析・診断
- **[Responsibility Pathway Design (RPD)](https://github.com/YutoriKomeiji/responsibility-pathway-design)** — 設計変換
- **[Responsibility Pathway Engineering (RPE)](https://github.com/YutoriKomeiji/responsibility-pathway-engineering)** — executable controlとengineering artifact
- **[Responsibility Pathway Runtime (RPR)](https://github.com/YutoriKomeiji/responsibility-pathway-runtime)** — authority / effect / recovery continuity
- **[Responsibility Pathway Operating System (RPOS)](https://github.com/YutoriKomeiji/responsibility-pathway-os)** — executable responsibility-state orchestration

このrepositoryの原文は設計思想の発生過程を追うために有用ですが、現在の最新仕様として引用するべきではありません。

## 保存している歴史文書

- [What is Safety-LCA](./docs/00-What-is-Safety-LCA.md)
- [Core Principles](./docs/01-Core-Principles.md)
- [Responsibility Pathways](./docs/02-Responsibility-Pathways.md)
- [Failure Modes](./docs/03-Failure-Modes.md)
- [Design Patterns](./docs/04-Design-Patterns.md)
- [Checklist](./docs/05-Checklist.md)
- [Extended Failure Modes](./docs/06-Failure-Modes.md)

これらは、後から現在の用語へ書き換えず、設計史として保存しています。

## Scope boundary

AHAAはmodel、SDK、runtime product、安全証明、法理論、certification framework、production authorization mechanismではありません。

現在の価値は、**AI capabilityが増えてもauthorityが暗黙に増えてはならない**という初期構造仮説を記録したdesign-origin artifactであることです。

## License

歴史文書には **CC BY-NC 4.0** の記載があります。現在repository rootにはmachine-detected license fileがなく、各文書内のlicense記載が参照元です。
