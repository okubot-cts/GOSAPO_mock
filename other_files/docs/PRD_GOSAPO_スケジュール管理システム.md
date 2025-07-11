# GOSAPO 研修オファー・日程調整管理システム PRD

## 1. プロジェクト概要

### 1.1 プロジェクト名
GOSAPO 統合研修管理システム（オファー・日程調整機能）

### 1.2 背景・課題
現在の研修手配プロセスには以下の課題があります：

**オファー管理の課題：**
- オファー情報がメール・Slackに散在し、情報が流れてしまう
- 講師への打診状況の追跡が困難
- オファー情報の一元管理ができていない

**日程調整の課題：**
- メール + Excelでの調整で間違いが多発
- 20-40回のレッスンを一括調整する際の複雑性
- 企業・受講生・講師の三者間調整の非効率性
- 確定後のカレンダー登録が手動作業

### 1.3 目標
- オファー情報の一元管理と可視化
- 効率的な日程調整ワークフローの実現
- エラー削減と作業時間短縮
- 外部システム連携による自動化

## 2. ターゲットユーザー

### 2.1 プライマリユーザー
- **GOSAPO運営スタッフ**: オファー作成・管理、日程調整
- **講師**: オファー確認、日程回答
- **企業担当者**: 日程候補提示、確認

### 2.2 セカンダリユーザー
- **受講生**: 日程確認、カレンダー登録
- **管理者**: システム設定、データ分析

## 3. 機能要件

### 3.1 オファー管理機能

#### 3.1.1 オファー作成・編集
- **オファー基本情報入力**
  - 案件名、クライアント名、研修期間
  - 言語、レベル、レッスン形態
  - 講師料、支払い条件
  - 開講場所、時間、回数
  
- **講師マッチング機能**
  - 条件に基づく適格講師の自動提案
  - 講師のスケジュール空き状況表示
  - 過去の実績・評価表示

#### 3.1.2 オファー一覧・検索
- **一覧表示機能**
  - ステータス別フィルタリング（未送信、打診中、承諾、却下など）
  - 期間、言語、クライアント別絞り込み
  - 優先度・緊急度による並び替え

- **詳細検索機能**
  - 複数条件による高度な検索
  - 保存検索条件の管理

#### 3.1.3 打診管理
- **講師への一括打診機能**
  - 複数講師への同時打診
  - 打診テンプレートの管理
  - 自動リマインダー機能

- **回答追跡機能**
  - 講師回答状況の可視化
  - 回答期限管理
  - 自動エスカレーション

### 3.2 日程調整機能

#### 3.2.1 日程候補管理
- **候補日程作成**
  - 複数日程の一括入力
  - カレンダーUI での直感的操作
  - 20-40回のレッスン日程を効率的に設定

- **三者間調整ワークフロー**
  1. 企業・受講生からの希望日程収集
  2. 講師への候補日程提示
  3. 講師からの可否回答収集
  4. 企業・受講生への最終確認
  5. 日程確定・通知

#### 3.2.2 スケジュール表示
- **統合カレンダービュー**
  - 月次・週次・日次表示
  - 講師別・クラス別表示切り替え
  - コンフリクト検知・警告表示

- **ガントチャート表示**
  - プロジェクト全体の進行状況可視化
  - クリティカルパスの識別
  - 遅延リスクの早期発見

#### 3.2.3 調整ステータス管理
- **進捗状況追跡**
  - 各日程の調整ステータス
  - 回答待ち・確定済み・保留中の分類
  - 全体進捗率の表示

### 3.3 コミュニケーション機能

#### 3.3.1 通知システム
- **自動通知機能**
  - 新規オファー・日程候補の通知
  - 回答期限リマインダー
  - ステータス変更通知

- **通知チャネル管理**
  - メール・Slack・Teams 連携
  - ユーザー別通知設定
  - 緊急度別通知方法

#### 3.3.2 コメント・履歴管理
- **コミュニケーション履歴**
  - オファー・日程調整に関する全やり取りの記録
  - 添付ファイル管理
  - 検索可能な履歴データベース

### 3.4 外部連携機能

#### 3.4.1 カレンダー連携
- **Google Calendar 連携**
  - 確定日程の自動同期
  - 受講生・講師への招待送信
  - 変更時の自動更新

- **Microsoft 365 連携**
  - Outlook カレンダー同期
  - Teams 会議室自動作成
  - 社内スケジュール共有

#### 3.4.2 チャットツール連携
- **Slack 連携**
  - 専用チャンネルでの進捗共有
  - Bot による自動アップデート
  - ワンクリック承認機能

- **Microsoft Teams 連携**
  - チーム内での情報共有
  - 承認ワークフロー
  - ファイル共有

## 4. 非機能要件

### 4.1 パフォーマンス
- レスポンス時間: 3秒以内
- 同時接続数: 100ユーザー
- データ処理: 1000件の日程を5秒以内で処理

### 4.2 セキュリティ
- SSL/TLS 暗号化通信
- 二要素認証対応
- ロールベースアクセス制御
- 個人情報保護対応

### 4.3 可用性
- 稼働率: 99.5% 以上
- バックアップ: 日次自動バックアップ
- 災害復旧: RPO 1日、RTO 4時間

### 4.4 互換性
- ブラウザ: Chrome, Firefox, Safari, Edge 最新版
- モバイル: iOS 12+, Android 8+
- API: RESTful API 提供

## 5. ユーザーインターフェース要件

### 5.1 デザイン原則
- 直感的で使いやすいUI/UX
- 既存のGOSAPOデザインとの統一性
- レスポンシブデザイン対応
- アクセシビリティ配慮

### 5.2 主要画面
1. **オファー一覧画面**
   - ステータス別タブ表示
   - 検索・フィルタリング機能
   - 一括操作機能

2. **オファー詳細画面**
   - 基本情報表示・編集
   - 打診履歴・コメント
   - 関連日程調整へのリンク

3. **日程調整画面**
   - カレンダー表示
   - 候補日程設定
   - ステータス管理

4. **ダッシュボード画面**
   - KPI表示
   - 進行中案件一覧
   - アラート・通知

## 6. データ要件

### 6.1 マスターデータ
- 講師情報（スキル、料金、稼働状況）
- クライアント情報
- 研修コース情報
- 拠点・教室情報

### 6.2 トランザクションデータ
- オファー情報
- 日程調整履歴
- コミュニケーション履歴
- 承認・却下履歴

### 6.3 データ連携
- 既存Zoho CRM との連携
- 会計システム連携
- 人事システム連携

## 7. 技術要件

### 7.1 アーキテクチャ
- マイクロサービス アーキテクチャ
- API ファースト設計
- クラウドネイティブ構成

### 7.2 技術スタック（推奨）
- **フロントエンド**: React.js / Vue.js
- **バックエンド**: Node.js / Python Django
- **データベース**: PostgreSQL / MongoDB
- **インフラ**: AWS / Azure
- **CI/CD**: GitHub Actions / GitLab CI

### 7.3 外部API連携
- Google Calendar API
- Microsoft Graph API
- Slack API
- Zoom API
- Teams API

## 8. 導入計画

### 8.1 フェーズ分け

#### Phase 1: オファー管理機能（3ヶ月）
- オファー作成・編集・一覧機能
- 基本的な打診管理機能
- 講師マッチング機能

#### Phase 2: 日程調整機能（3ヶ月）
- 日程候補管理機能
- カレンダー表示機能
- 基本的な調整ワークフロー

#### Phase 3: 外部連携・高度機能（2ヶ月）
- カレンダー連携
- チャットツール連携
- 高度な分析・レポート機能

### 8.2 成功指標
- オファー処理時間: 50%削減
- 日程調整ミス: 80%削減
- 講師満足度: 向上
- 処理効率: 3倍向上

## 9. リスクと対策

### 9.1 技術リスク
- **API制限**: 外部サービスのAPI制限に対する代替手段
- **パフォーマンス**: 大量データ処理時の最適化
- **セキュリティ**: 個人情報漏洩防止対策

### 9.2 運用リスク
- **ユーザー教育**: 十分なトレーニング期間の確保
- **データ移行**: 既存データの正確な移行
- **変更管理**: 段階的な導入による影響最小化

## 10. 予算・リソース

### 10.1 開発コスト（概算）
- 開発費用: 800-1200万円
- インフラ費用: 年間100-200万円
- 運用・保守費用: 年間200-300万円

### 10.2 必要リソース
- プロジェクトマネージャー: 1名
- システムエンジニア: 3-4名
- UI/UXデザイナー: 1名
- テスター: 1-2名

## 11. 承認・次ステップ

このPRDをもとに、以下の次ステップを提案します：

1. **ステークホルダーレビュー**: 関係者からのフィードバック収集
2. **技術検証**: POC（概念実証）の実施
3. **詳細設計**: 画面設計・システム設計の作成
4. **開発開始**: Phase 1 からの段階的開発

---

**文書作成日**: 2025年1月26日  
**作成者**: GOSAPO開発チーム  
**承認者**: [承認者名]  
**バージョン**: 1.0 