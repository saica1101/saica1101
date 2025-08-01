# [saica1101](https://github.com/saica1101)
<p align="left"> 
  <img alt="Top Langs" height="150px" src="https://github-readme-stats.vercel.app/api/top-langs/?username=saica1101&layout=compact&show_icons=true&theme=onedark" />
  <img alt="github stats" height="150px" src="https://github-readme-stats.vercel.app/api?username=saica1101&theme=onedark&show_icons=ture" />
</p>
  
___
# My Coding Rules
## フォーマットと構造
* インデント
    - 1Tab or 4 space
* 行の長さ
    - 80文字以内
* 空白行
    - 関連するコードブロックの間に適切な空白行を挿入する
* ブレークのスタイル
    - 使用しているブレースのスタイルは統一する
* ファイル構造
    - 各ファイルは特定の目的や機能を関連するコードのみを含ませる
* ファイルクラスの行数
    - 各クラス400行以内
* 関数の行数
    - 1関数は100行以内
* 関数名・変数名の最大長
    - 50文字以内

## 命名規則
* 明確さ
    - 変数、関数、クラスの目的や機能を正確に表す
* 短縮形や略語の使用
    - 一般的に理解される略語や短縮形を使用する
* 一貫性
    - 同一概念、同一目的の変数や関数に対してはプロジェクト全体で一貫した命名前付けを行う
* 複数形と単数形
    - 配列やリストを示す変数の名前は複数形
    - 単一のアイテムを示す変数の名前は単数形
* 前置・後置の接頭語/接尾辞の使用
    - Boolean型は `is`, `has`, `should`, `can` などの接頭辞で始める
        - 状態の確認 `is`
            - 用途：何かの状態や条件が成立しているか確認する
            - 例：`isActicve`, `isFinished`, `isValid`
        - 所有関係の確認 `has`
            - 用途：何かが特定の属性や要素を持っているかを確認する
            - 例：`hasItem`, `hasErrors`, `hasAccess`
        - 行動の推奨 `should`
            - 用途：何かのアクションや動作を行うべきかを示す
            - 例：`shouldUpdate`, `shouldRetry`, `shouldAlert`
        - 可能性の確認 `can`
            - 用途：何かのアクションや動作が可能かどうか確認する
            - 例：`canSubmit`, `canEdit`, `canAdvance`
## アーキテクチャとデザインパターン
* デザインパターンの採用
    - 適切なデザインパターンを採用してコードの再利用性、拡張性、および保守性を向上させる
* モジュール性と組織化
    - システムを構成する部品を明確に識別し、それぞれを独立したモジュールとして設計する
    - モジュール間の依存関係を明確に、設計は疎結合・高凝集の原則に従う
## SOLID原則
* 単一責任の原則(SRP)
    - 各クラスやモジュールは1つの明確な責務や役割のみを担わせる
    - 変更が必要になった場合、その影響範囲は該当のクラスやモジュールのみに限定させる
* オープン/クローズド原則(OCP)
    - 新しい要件や機能を追加する際に、既存のコードを変更せず拡張できるように設計する
    - 既存のコードの安定性は新しい変更によって損なわれないようにする
* リスコフの置換原則(LSP)
    - 派生クラスは、基底クラスと置換可能な形で設計する
    - 基底クラスの代わりに派生クラスを使用した場合も、期待する動作が保証されるようにする
* インターフェース分離の原則(ISP)
    - クラスは不必要なインターフェースを持たない
    - 与えられたインターフェースは、その使用するクライアントの要件に特化して設計する
* 依存性逆転の原則(DIP)
    - 高水準のモジュールは低水準のモジュールに直接依存させない
    - モジュール間の依存関係は抽象(インターフェースや抽象クラスなど)を介する
## コードのクリーンさ
* アーリーリターン
    - 関数やメソッド内で、条件が満たされないケースやエラーケースを最初にチェックし適切にリターンする
    - ネストが深くなるのを避ける
* マジックナンバーを避ける
    - ハードコードされた数字や文字列は使用しない
    - そのような値の代わりに、意味を持たせた定数や設定値を使用する
* デッドコードの削除
    - 使用されていない変数、関数、クラスは存在させない
* DRY原則
    - 同じコードが複数の場所で繰り返されないようにする
    - 異なるロジックを持つものに関してはDRY原則を適用しない
    - 重複を削減するための共通の関数やモジュールを活用できるように配置する
* KISS原則
    - コードはシンプルかつ明確に問題解決させる
    - 必要以上の複雑な設計や実装は避ける
* YAGNI原則
    - 現時点で必要とされていない機能やコードをあらかじめ追加しない
    - 必要となる前に追加したコードが存在する場合、それが本当に必要か判断する
* ボーイスカウトの原則
    - コードを改変した箇所は、改変する前よりも良い状態にする
## セキュリティ
* データの検証
    - 外部から取り込むデータ全てに対して、適切な入力検査やバリデーションを実施する
    - 不正な形式や攻撃コードが含まれる入力は適切に拒否またはサニタイズする
* センシティブデータの取り扱い
    - APIキー、パスワード、セッショントークンなどのセンシティブデータはコード内にハードコードしない
    - センシティブデータは環境変数や専用の秘密管理ツールを利用し、安全に保管する
* データの暗号化
    - パスワードや他の個人情報は適切な手段で暗号化し、安全にデータベースに保存する
* インジェクション攻撃の防止
    - ユーザー入力をクエリやコマンドに組み込む際、安全なパラメータ化方法やエスケープメカニズムを使用する
    - SQLインジェクションやOSコマンドインジェクションのリスクを十分に認識し、これらの攻撃を防ぐための対策を施す
* XSS(クロスサイトスクリプティング)の対策
    - XSS攻撃に対する脆弱性は無く、外部データの表示には適切なエスケープやサニタイズを適用する
* クロスサイトリクエストフォージェリ(CSRF)の対策
    - CSRF攻撃に対する脆弱性は無く、トークンベースの対策を適切にする
## パフォーマンス
* 効率的な計算
    - 不要な計算や再計算は排除する
    - 無限ループのリスクを回避する
* 効率的なデータベースクエリ
    - N+1問題のリスクを考慮し、避ける
    - JOINを使用する際、必要なテーブル、カラムのみ選択する
    - フルテーブルスキャンの回避や、サブクエリの過度な使用は控える
* データキャッシングの適用
    - 頻繁にアクセスされるデータはキャッシュ化する
    - キャッシュの有効期限や更新策略を適切に設定する
* 外部データサービス連携の最適化
    - 外部APIやサービスのレスポンスタイムや制限を適切に考慮し、設計する
    - 同じリクエストの冗長な発行を避ける為の戦略を取り入れる
* フロントエンドの最適化
    - 画像やリソースは最適なフォーマット、圧縮、サイズで提供する
    - 必要に応じてオフスクリーンのコンテンツや画像は遅延ローディングする
    - クライアントサイドのレンダリングでは不要な再レンダリングや計算を回避する
* 非同期処理の最適化
    - 非同期処理を適切に行い、相互に依存しないタスクはまとめて処理する
    - 計算が重いタスクは適切に同期処理を行い、メインスレッドのブロックを回避する
## テスト
* テストの範囲
    - 想定されるあらゆるケース、エッジケースを適切にテストする
    - 例外処理やエラーケースも適切にテストする
* テストの明確さ
    - テスト名は意味があり、何をテストしているのか明確に示す
    - テストの目的や対象をコメントやドキュメントに明記する
* テストの信頼性
    - テスト結果は一貫しており、環境やランダム性に依存させない
    - テストが失敗した場合のデバッグがしやすいよう、失敗原因や詳細を盟約に出力する
* テストの独立性
    - 各テストは他のテストから独立して実行できるようにする
    - テスト間での依存関係や順序が必要な場合、その理由や条件を明確に文章化する
* ユニットテスト
    - 個々の関数やメソッドは独立してテストする
    - テストは明確な期待値と実際の結果を比較する
* 結合テスト
    - システムの異なる部分が互いに適切に機能するかを確認するテストを行う
    - 依存関係や外部サービスとの連携が正しく動作することを確認する
## エラーハンドリング
* 明確なエラーメッセージ
    - エラーメッセージは具体的に、そのエラーの原因や解決策についての情報を提供する
* エラーのカテゴライズ
    - エラーコードやエラータイプは適切に定義し、それぞれのエラーを正確に分類する
* 外部のエラーハンドリング
    - 外部サービスやライブラリのエラーを適切にキャッチし、その後の処理を適切に行う
    - 予期しないエラー(タイムアウトや通信エラー)に対する適切な処理を行う
* リトライ戦略の適用
    - 一時的なエラーや通信の障害に対して、再試行のロジックを明確に実装する
    - リトライの間隔や上限回数を適切に設定する
* リソースのクリーンアップ
    - 例外やエラーが発生した際、未完了のトランザクションやオープンリソース(ファイル、ネットワーク接続など)は適切に終了・解放する
* エラーロギング
    - 発生したエラーや例外は、適切なログレベルで記録する
    - ログには、エラーの発生箇所、エラーコード、エラーメッセージなど、デバッグに必要な情報を含める
## コメント
* 明確性
    - コードの目的や動作、特に非直感的な部分はコメントで十分に明確に説明する
* 詳細性
    - 複雑なロジックやアルゴリズム、特定の判断背景など詳細なコメントを通じて後のレビューやメンテナンスが容易に理解できる設計にする
* 更新の追従
    - コードが変更された場合、関連するコメントも適切に更新し、情報の不整合が生じないようにする
* 変更理由の記載
    - 大きな変更や重要な修正をコードに加える際、その背景や理由をコメントとして十分に記述する
* 過度なコメントを避ける
    - コード自体が自己説明的である場合、不要で冗長なコメントは避ける
    - コメントには実際に追加の文脈や説明が必要な場面でのみ適切に使用する
* TODOやFIXMEの使用
    - 未完成の部分には `TODO:`、あとで修正が必要な個所には `FIXME:` のようなキーワードを使って明確に記す
# インラインドキュメンテーション
* 関数/メソッドのドキュメンテーション
    - 各関数やメソッドの直前に、その機能、引数のタイプ、戻り値のタイプ、例外などの情報を明確に記載する
* クラスとプロパティの説明
    - クラスとそのプロパティに、それぞれの目的と使用法を示す説明を付ける
* タグの使用
    - jsDocやその他のドキュメンテーションツールでサポートされているタグ(例： `param`, `@returns`, `@throws`)を適切に使用して、ドキュメンテーションの構造を整理する
