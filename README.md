# Portfolio: thin-shade (Technical Details)

[日本語](#japanese) | [English](#english)

---

<a name="japanese"></a>
## テクニカル・ポートフォリオ (Japanese)

### 1. 開発概要
* **プラットフォーム**: PC (Unity 3D)
* **レンダリング**: Universal Render Pipeline (URP)
* **開発の主眼**: FPSアクションホラー開発による技術的検証。設計開発、翻訳、シナリオ、演出を一人で担当。AIツールを補助的に活用した効率的なプログラミング。

### 2. ソフトウェアアーキテクチャ
拡張性と保守性を意識した設計を導入しています。
* **デザインパターンの適用**:
    * **Singleton Pattern**: GameManager、AudioManager、ProgressUI 等に適用し、グローバルな状態管理を効率化。
    * **State Machine**: 敵AIにEnumベースのステートマシンを実装。「索敵・追跡・攻撃」の状態遷移を論理的に分離。
* **設計思想**:
    * **Interfaceによる疎結合化**: コンポーネント間をインターフェースで接続し、特定のクラスに依存しない拡張性を確保。
    * **イベントドリブン（Actionシステム）**: ヘルス状態やイベントをC#のActionで通知。発信側と受信側を切り離しバグを抑制。
    * **Co-routine**: 非同期処理をシンプルに実装し、パフォーマンスを最適化。

### 3. ゲームシステム・インタラクション
* **入力・操作**: New Input SystemによるFPS操作の実装。
* **AI・ナビゲーション**: NavMeshによる経路探索。ドアを動的な障害物として設定し、「閉じ込める」等のプレイを可能に。
* **UI**: コンテキストメニュー、長押しによるタスク完了遅延、音量調整機能付き設定画面。
* **ビジュアル**: ShaderGraphによるカスタムシェーダー、敵や環境のアニメーション制御。

### 4. ローカライズ & 翻訳（独自強み）
* **多言語対応**: LocalizationパッケージとString Tableを活用。
* **一気通貫の開発**: 実装から翻訳（日英）までを一人で完結。文脈に即した質の高いローカライズを実現。

---

<a name="english"></a>
## Technical Portfolio (English)

### 1. Development Overview
* **Platform**: PC (Unity 3D)
* **Rendering**: Universal Render Pipeline (URP)
* **Core Focus**: Technical verification through FPS action-horror development. Solely responsible for design, development, translation, scenario writing, and direction.

### 2. Software Architecture
* **Design Patterns**:
    * **Singleton Pattern**: Applied to core systems like `GameManager`, `AudioManager`, and `ProgressUI`.
    * **State Machine**: Enum-based state machine for enemy AI (Search, Chase, Attack).
* **Design Philosophy**:
    * **Decoupling via Interfaces**: Ensures flexible extensibility independent of specific classes.
    * **Event-Driven (Action System)**: Uses C# Actions to notify state changes, minimizing side effects.
    * **Co-routines**: Efficient asynchronous processing for smooth gameplay.

### 3. Game Systems & Interaction
* **Input**: FPS controls using the New Input System.
* **AI & Navigation**: NavMesh pathfinding with dynamic obstacles (doors), enabling strategic gameplay like trapping enemies.
* **UI**: Context-menu commands, long-press task completion, and full settings menu.
* **Visuals**: Custom shaders via ShaderGraph and integrated animation controllers.

### 4. Localization & Translation
* **Multilingual Support**: Implementation using Unity Localization package and String Tables.
* **End-to-End Development**: Seamless integration of implementation and JA/EN translation, ensuring contextual accuracy.
