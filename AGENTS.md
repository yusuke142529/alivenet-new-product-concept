# AGENTS.md

本リポジトリでエージェント（私）が作業するための指針です。配下ディレクトリすべてに適用されます。

## 目的（スコープ）
- 本プロジェクトは「アライブネットの新規事業アイデア創出（日本語）」を主目的とする。
- コードや実装は原則行わない。成果物は文書（企画・要件・検証計画）に限定する。

## 作業モード（重要）
- 言語: 日本語（必要に応じて英語用語を併記）。
- 出力形式: 箇条書き優先、1トピック1行を基本。必要に応じて短い段落。
- 日付: 相対表現を避け、絶対日付で記載（例: 2025-10-17）。
- ウェブ参照: ユーザーが明示した場合のみ検索を実施。実施時は出典を明記。
- 機密性: 会社・個人の秘匿情報は記載せず、必要時は伏字または変数名（例: <顧客A>）。

## 先に合意すべき前提事項（Ideation 前のチェックリスト）
以下はアイデア創出・比較・評価を円滑にするための前提。未確定は「仮」と明記し、検証項目に回す。

1) 戦略整合
- 事業方針: 収益化重視/成長重視/技術検証 等
- 対象市場: 国内/海外、優先業界、想定顧客（B2B/B2C/官公庁）
- 期間・里程標: 0→PoC→β→GA のマイルストンと目標時期

2) 内部アセット/強み
- 既存チャネル（販売・導入・サポート）、保有データ/ドメイン知見、技術スタック/特許、主要パートナー

3) 制約条件
- 初期予算レンジ、チーム規模/スキル、規制・業法（個人情報/電気通信/医療 等）、ブランド/レピュテーション制約

4) 収益モデルの方針
- SaaS（月額/年額/従量）、取引課金、ライセンス、広告、紹介/成果報酬、プロサービス の可否と優先

5) 成功指標（KGI/KPI）
- 例: 年次ARR、初期ロゴ数、GRR/NRR、CAC回収期間、PoC→本契約移行率、NPS、主要機能のWAU/MAU

6) リスク許容度
- 技術・法務・営業の各リスクに対する許容水準、想定回避/低減策

7) 意思決定プロセス
- ステークホルダー（決裁者/実務責任者）、合議フロー、レビュー頻度、承認基準

## 成果物（ドキュメント）
- `docs/idea-canvas.md`: 事業アイデアの標準キャンバス（1アイデア=1セクション）。
- `docs/idea-scorecard.md`: アイデア評価表（定量/定性指標）。
- `docs/validation-plan.md`: 検証計画（仮説→実験→学び→判断）。
- `docs/brd-template.md`: ビジネス要件定義テンプレート（必要時）。

※ 本ファイル作成時点では上記は未作成。ユーザーの指示があり次第追加する。

## アイデア・キャンバスの項目定義（標準）
- 顧客セグメント: ペルソナ/業種/規模/意思決定者。
- 重要課題（Jobs/Pains）: 数値/頻度/現在の代替手段。
- 提供価値（Value Proposition）: Before→After、差別化ポイント（10倍/唯一性/スイッチング理由）。
- ソリューション仮説: コア体験（1分で語れる）、MVP境界。
- 主要機能: Must/Should/Could の3段階。
- 収益モデル: 価格仮説、単価×数量、収益ドライバ。
- コスト構造: 固定/変動の主因。
- 市場/競合: TAM/SAM/SOMの粗推定、競合/代替とディフェンス戦略（ロックイン/ネットワーク効果/規模/規制）。
- GTM: 取得チャネル、販売モーション、導入障壁と対策。
- KPI/メトリクス: 成功シグナルとヘルス指標。
- 検証計画: 仮説→実験方法→合格基準→タイムライン。
- リスク/法務: 規制・準拠・データ/プライバシー。
- ロードマップ: 0→PoC→β→GA→拡張の段階計画。
- 前提/未決: Assumption(A)/To-Validate(V)/Decision(D) のタグ運用。

## 評価スコアカード（初期軸）
- 市場魅力度（規模/成長）
- 顧客ペイン強度（緊急度/予算）
- フィット（自社アセット/チャネル）
- 差別化の持続性（模倣困難/規模利益）
- 単位経済性（粗利/CAC回収）
- リスク（法務/実装/販売）
- 実行容易性（期間/リソース）

各項目は 1〜5 点で評価し、重み付けは合意後に設定。

## ドキュメント運用ルール
- テンプレートに従い、各見出しは空欄でも作成。未知は「TBD」か「仮説」。
- バージョン管理: ドキュメント冒頭にメタデータを記載。

メタデータ例（フロントマター風）:
```
Title: <文書名>
Owner: アライブネット 新規事業PJ
Version: 0.1 (Draft)
Status: WIP | Review | Approved
Last-Updated: 2025-10-17
Related: <関連文書/課題番号>
```

## コミュニケーションと進め方
- 着手前に「前提事項チェックリスト」を確認し、不明点は質問する。
- 1回の作業で広げすぎず、アイデアは最大3件→スコアリング→上位1件を深掘り。
- ユーザーが明示しない限り、コード/ツール設定は追加しない。
- 作業ログは簡潔に共有（何を作り、次に何をするか）。

## 変更管理
- 本ファイルより深い階層に別の `AGENTS.md` を置く場合、そちらのルールが優先される。
- 本指針とリポジトリの「Repository Guidelines」に相違がある場合、ユーザーの直接指示を最優先とする。

## アイデアID/命名規約（追加）
- ID形式: `IDEA-001`（3桁ゼロ埋め。1000件超は4桁に拡張）。
- ファイル配置: `docs/ideas/IDEA-001-<短いスラッグ>.md`。
- 関連アセット: `assets/ideas/IDEA-001/` に保管（図、スクショ、調査メモ）。
- スラッグ規則: 英数字とハイフンの`kebab-case`、20文字以内、機密名は使用しない。

## ステージゲートと進級基準（追加）
- フェーズ: Discovery → Validation → Commit。
- 進級判定（初期値）:
  - スコアカード総合 ≥ 75 点。
  - 最重要仮説（H1〜H3）の合格。
  - 法務・規制レッドフラグなし（是正計画を含む）。
  - 半手動でもエンドツーエンド価値提供を再現可能。
  - 必要リソース/体制を確保できる見込み。

## レビュー体制/頻度（追加）
- 定例レビュー: 週次（例: 水曜）。参加: 決裁者/PO/営業/法務/担当。
- 決定事項は `docs/decisions/` のADRに記録し、対象文書へリンクを追記。

## 机上調査（Web参照）の扱い（追加）
- Discovery: 原則オフ（依頼がある場合のみ実施、出典を明記）。
- Validation: 出典付きで許可。機密情報は要約のみ、外部共有不可。
- 参照は脚注的にURLではなく出典リンク（CLIの規約に従う）。

## 守秘・匿名化ルール（追加）
- 区分: Internal / Confidential。顧客名は〈顧客A〉等の仮名を使用。
- 個人情報・機微データは持ち込まない。必要時は合成データで代替。

## 変更管理の詳細（追加）
- 各文書末尾にChange Logを追記: `YYYY-MM-DD / 変更者 / 要約`。
- メジャー変更は版番号を+0.1し、コミットメッセージはConventional Commits準拠。

## スコアカード重みの改定手順（追加）
- 合計100固定。改定提案 → 影響メモ → 定例で承認 → `docs/idea-scorecard.md`の「重み」章へ履歴追記。

## 決定記録（ADR）の運用（追加）
- 置き場所: `docs/decisions/ADR-YYYYMMDD-<テーマ>.md`。
- 記載: 背景/選択肢/判断/根拠/影響/フォロータスク。ステータス: Proposed/Accepted/Superseded。

## 用語集（追加）
- `docs/glossary.md` に社内・業界用語を集約（略語/日本語/英語/定義/備考）。

## 付録（YAML）: 会社構造サマリー（docs/company/alivenet-business-structure-initial-ja-2025-10-16.md）

```yaml
meta:
  title: "株式会社アライブネット：事業内容・事業構造（初版）"
  source_file: "docs/company/alivenet-business-structure-initial-ja-2025-10-16.md"
  last_updated: "2025-10-16"
  generated_on: "2025-10-17"
  status: "初版"

company:
  name: "株式会社アライブネット"
  hq_address: "東京都渋谷区渋谷3-19-1 オミビル7F"
  representative: "松尾 直樹"
  capital_jpy: 100000000
  telecom_registration_number: "A-14-05394"

domain:
  category: "コールソリューション（B2B）"
  positioning: "コールセンター向けクラウドCTI＋通話料割引（Alive Line）"

brands_products:
  - name: "Voiper Dial"
    category: "クラウドCTI"
    key_features: ["全通話録音", "リアルタイムモニタ", "プレディクティブ/再架電", "NG分析", "CRM連携"]
  - name: "Voiper Call"
    category: "アウトバウンドCTI"
    key_features: ["録音", "モニタ", "プレディクティブ発信", "オペレーター割当/解除"]
  - name: "Voiper SMS"
    category: "SMS配信"
    key_features: ["最大660文字", "2秒以内の高速送信", "キャリア直収接続"]
  - name: "Alive Line"
    category: "通話料割引"
    pricing_examples:
      unit: "JPY/秒"
      fixed_line_per_sec: 0.06
      mobile_per_sec: 0.25
      notes: "秒課金の表記（分換算: 固定2.6円/分, 携帯12.5円/分）"

oem_partner_ecosystem:
  primary:
    - name: "BlueBean"
      vendor: "ソフツー"
      relationship: "OEM/代理店制度あり"
  alias_terms:
    - alias: "CT-1"
      possibly_refers_to: "CT-e1/SaaS（コムデザイン）"
      status: "社内確認が必要"

value_proposition:
  - "通話仕入れ力（Alive Line）によるコスト優位"
  - "クラウドCTIでの短期立ち上げ/在宅・多拠点対応"
  - "営業→納品/設定→サポートの一気通貫（ワンストップ）"

customer_segments:
  industries: ["BPO", "通販/EC", "金融/保険", "医療/予約センター", "SaaS/ITサポート", "教育", "物流"]
  org_size: "小規模（数席）～中規模（数十席）"
  use_cases: ["取次", "予約", "案内", "DMコール", "督促/回収", "本人確認", "SMSリマインド/不達フォロー"]

business_model:
  revenue_streams: ["通話料マージン", "ライセンス/席課金", "初期構築/設定", "運用・保守", "オプション（レポート/CRM連携/SMS大量配信）"]
  cost_structure_major: ["回線/番号の仕入れ", "OEM/ライセンス費", "サポート/運用人件費", "監視/インフラ費", "個別連携/教育"]

swot:
  strengths: ["通話仕入れ力による価格優位", "Voiper群＋一気通貫の導入/運用"]
  weaknesses: ["CTIコアのOEM依存（価格・機能ロードマップの主導権）"]
  opportunities: ["日本語会話に強いAI活用", "WebRTCによる在宅・分散化定着", "データ利活用需要"]
  threats: ["海外系CCaaS/CPaaSの拡販", "通話単価の下落", "法規・キャリア仕様の変更"]

risks_and_mitigations:
  - risk: "キャリア/番号・料金条件の変更"
    mitigation: "LCR（最適経路選択）と複数キャリア分散"
  - risk: "OEM価格/機能の変更"
    mitigation: "公開イベント契約＋Adapter化で置換容易性を確保"
  - risk: "品質事故（音質/輻輳）"
    mitigation: "SBC/モニタリングでMOS/RTCP収集、QoS設計の標準化"
  - risk: "個人情報/PCIのリスク"
    mitigation: "録音の一時停止/再開・DTMFマスキング・監査ログ"

future_policy_outline:
  concept: "回線の強みをAPI化（CPaaS）し、上位にイベント駆動SaaSを重ねる二段構え"
  cpaas_core:
    apis: ["通話API（発信/転送/録音/DTMF）", "番号API（発番/休止/在庫）", "課金API（CDRレーティング）"]
    capabilities: ["不正呼対策（IRSF）", "品質監視（MOS/RTCP）", "LCR（価格×品質×地域）"]
  value_add_saas:
    components: ["イベントハブ（Webhook/Streaming）", "Agent Assist（要約/次アクション/ACW草案）", "Insight（可視化/分析/外部API）", "Flow（ノーコード自動化）"]
  portability: "BlueBean/CT-1上でも価値提供し、将来自社コアへ置換可能"

open_items:
  - "CT-1の正式製品名・提供元（社内確認）"
  - "OEM契約の範囲（一次サポート/SLA/価格/変更権限）"
  - "内部KPI（売上構成・粗利・チャーン等）の確定"
```

## 付録（YAML）: 運用・規制・料金ポリシー（docs/company/alivenet-ops-policy-2025-10.md）

```yaml
meta:
  title: "アライブネット 運用・規制・料金ポリシー（2025-10）"
  source_file: "docs/company/alivenet-ops-policy-2025-10.md"
  last_updated: "2025-10-16"
  generated_on: "2025-10-17"
  scope: ["Alive Line", "Voiper (Dial/Call/SMS)", "OEM連携（BlueBean 等）"]

pricing_and_costs:
  voice:
    unit: "JPY/秒"
    examples:
      fixed_line_per_sec: 0.06
      mobile_per_sec: 0.25
      fixed_line_per_min: 2.6
      mobile_per_min: 12.5
    rounding: "秒課金（丸め規則は商品仕様で統一）"
  ancillary_fees:
    universal_service_fee: "番号あたり月額・別計上"
    relay_service_fee: "該当時に適用"
  sms:
    max_chars: 660
    send_latency_sec_max: 2
    connectivity: "キャリア直収接続"
    pricing_note: "送信方式/文字種別で変動"
  invoice_breakdown: ["通話料", "チャネル/席料", "付帯料"]
  tax_note: "税区分を併記"

legal_and_compliance_minimums:
  - law: "特定電子メール法"
    requirements: ["オプトイン取得", "送信者表示", "オプトアウト提供", "なりすまし禁止"]
  - law: "個人情報保護法（APPI）"
    requirements: ["録音/通話メタの目的明示", "安全管理措置", "国外移転時の情報提供/相当措置または本人同意"]
  - law: "PCI DSS 配慮"
    requirements: ["DTMFマスキング", "録音のポーズ/レジューム", "暗号化"]
  - law: "緊急通報（制約の説明）"
    requirements: ["IP/050の制約を案内", "代替経路（携帯等）を必須記載"]
  - law: "特商法（電話勧誘販売）"
    requirements: ["不実告知・迷惑勧誘の禁止", "クーリングオフ案内", "録音保全"]

product_outline:
  voiper_dial_call: ["全通話録音", "リアルタイムモニタ", "ACD", "プレディクティブ"]
  voiper_sms: ["直収訴求", "高速/長文"]
  oem_foundation: "BlueBean 等のパートナー制度（詳細条件は契約で確定）"

quality_and_network_baselines:
  bandwidth_per_call_kbps: 150
  one_way_delay_ms_max: 150
  jitter_ms_max: 30
  packet_loss_percent_max: 1
  ops_kpis: ["ASR", "ACD", "PDD", "MOS≥4.0", "放棄率", "FCR", "稼働率", "SMS到達率"]
  predictive_abandon_rate_daily_max_percent: 3

cdr_reconciliation_and_billing:
  three_way_keys: ["キャリアCDR", "OEM/CTI CDR", "自社集計（相手先・開始時刻（秒）・秒数・課金種別）"]
  variance_alert_thresholds:
    count_percent: 0.5
    amount_percent: 0.2
  first_check: "丸め規則の不一致有無"
  invoicing: "月次締めで内訳化（通話料・席/チャネル・付帯料）。税・インボイス対応"

oem_boundary_and_substitutability:
  contract_should_define: ["顧客所有権", "SLA/メンテ通知", "データ所有権/持出し", "価格改定・解除条項", "一次サポート責任"]
  replacement_plan: ["API/データ互換", "録音/メタの移送", "段階移行（隊列/キャンペーン単位）"]

security_operations:
  access: ["RBAC/最小権限", "特権の二要素", "監査ログ（1年以上）"]
  data: ["録音/メタの暗号化保管", "鍵管理（KMS/ローテ・分離）"]
  vulnerability: ["定期スキャン", "ペンテ/是正SLA", "インシデント時の法令報告・本人通知SOP"]

onboarding_monitoring_support:
  onboarding_sop: ["要件", "回線/番号", "ネットワーク試験", "ACD/席設計", "録音/同意掲示", "教育", "本稼働", "初月チューニング"]
  monitoring: ["ASR/ACD/PDD/5xx", "遅延・ジッタ・ロス", "SMS到達/拒否"]
  response_to_deviation: ["LCR/経路切替", "キャリアエスカレーション"]
  support: ["プラン別の応答/復旧SLA", "障害時の状況→影響→回避策→復旧見込の開示"]

billing_collection_and_fraud_resilience:
  credit_and_deposit: ["初回与信", "途上与信の閾値定義", "延滞時の同時通話枠一時制限"]
  irsf_and_abuse: ["高リスク国/時間帯の制限", "異常ASR/PDD/MOSの検知遮断", "ホットリスト更新"]

roadmap:
  short_term_0_3_months: ["CDR三者突合の自動化", "放棄呼3%基準の監視", "SMS特電法の証跡テーブル/オプトアウトAPI", "緊急通報の案内整備"]
  mid_term_3_9_months: ["Event/Command公開契約の社内標準化", "LCR×品質（ASR/MOS）最適化", "DTMFマスキング導入", "国外移転の相当措置モニタ"]
  long_term_9_18_months: ["CPaaS（通話/番号/課金API）試験提供", "イベントストリーミング（RecordingReady/Transcript）公開", "Agent Assist/可視化の商用化"]

references:
  - "https://alivenet.com/"
  - "https://www.bluebean365.jp/"
  - "https://www.ppc.go.jp/"
  - "https://www.no-trouble.caa.go.jp/spam/"
  - "https://www.pcisecuritystandards.org/"
  - "https://www.cisco.com/"
  - "https://www.ofcom.org.uk/"

note: "料金・SLA・契約条件の最終版は社内正式文書を唯一のソース。本書は公開情報と社内運用ベストプラクティスの統合ガイド。"
```
