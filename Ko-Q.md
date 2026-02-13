[日本語 (Japanese)](#日本語) | [English](#english)

## 日本語

### 技術スタック
- `Swift`
- `SwiftUI`（`NavigationStack`, `Form`, `sheet`, `@StateObject`, `@AppStorage`）
- `MVVM` アーキテクチャ（`Views` / `ViewModels` / `Models`）
- `Combine`（`ObservableObject`, `@Published`）
- `Swift Concurrency`（`Task`、キャンセル制御、非同期タイミング制御）
- `AVFoundation`（`AVAudioPlayer`, `AVAudioSession`）によるホワイトノイズ・チャイム再生
- `CoreHaptics`（`CHHapticEngine`）による呼吸フェーズ同期ハプティクス
- `UserDefaults` + `Codable` による設定永続化
- `String Catalog`（`Localizable.xcstrings`）によるローカライズ（日本語 / 英語）

### 技術的ハイライト
- キャンセル可能な非同期ループで、呼吸サイクル（`吸う → 止める → 吐く`）のエンジンを実装。
- フェーズごとに、ビジュアルアニメーション・音量フェード・ハプティクス強度を同期制御。
- プリセット呼吸法とカスタム設定を実装し、ユーザー設定を永続化。
- `canImport(...)` を用いて、音声/触覚機能のフォールバック安全性を確保。
- MVVMで表示とロジックを分離し、保守しやすい構成に設計。

## English

### Tech Stack
- `Swift`
- `SwiftUI` (`NavigationStack`, `Form`, `sheet`, `@StateObject`, `@AppStorage`)
- `MVVM` architecture (`Views` / `ViewModels` / `Models`)
- `Combine` (`ObservableObject`, `@Published`)
- `Swift Concurrency` (`Task`, cancellation, async timing control)
- `AVFoundation` (`AVAudioPlayer`, `AVAudioSession`) for white noise + chime playback
- `CoreHaptics` (`CHHapticEngine`) for phase-synced haptic feedback
- `UserDefaults` + `Codable` for persistent settings
- `String Catalog` (`Localizable.xcstrings`) for localization (JA / EN)

### Technical Highlights
- Built a breathing cycle engine (`inhale → hold → exhale`) with cancellable async loops.
- Synchronized visual animation, audio fading, and haptic intensity per breathing phase.
- Implemented presets + custom routines with persistent user preferences.
- Designed fallback-safe audio/haptics modules using `canImport(...)` guards.
- Kept presentation and logic cleanly separated with MVVM for maintainability.
