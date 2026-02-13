## Tech Stack
- `Swift`
- `SwiftUI` (`NavigationStack`, `Form`, `sheet`, `@StateObject`, `@AppStorage`)
- `MVVM` architecture (`Views` / `ViewModels` / `Models`)
- `Combine` (`ObservableObject`, `@Published`)
- `Swift Concurrency` (`Task`, cancellation, async timing control)
- `AVFoundation` (`AVAudioPlayer`, `AVAudioSession`) for white noise + chime playback
- `CoreHaptics` (`CHHapticEngine`) for phase-synced haptic feedback
- `UserDefaults` + `Codable` for persistent settings
- `String Catalog` (`Localizable.xcstrings`) for localization (JA / EN)

## Technical Highlights
- Built a breathing cycle engine (`inhale → hold → exhale`) with cancellable async loops.
- Synchronized visual animation, audio fading, and haptic intensity per breathing phase.
- Implemented presets + custom routines with persistent user preferences.
- Designed fallback-safe audio/haptics modules using `canImport(...)` guards.
- Kept presentation and logic cleanly separated with MVVM for maintainability.
