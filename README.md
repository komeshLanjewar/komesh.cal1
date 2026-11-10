# CalTrack – Smart Calorie Tracker (Kotlin + Jetpack Compose + Room)

Offline calorie tracker: food diary (breakfast/lunch/dinner/snacks), searchable database of ~105 foods
(incl. roti, rice, dal, poha, idli, dosa, paneer, eggs, chicken…), custom foods, calorie ring, macros,
weekly/monthly charts, weight tracking, profile with calorie-target estimate, Material 3 light/dark theme.

## Get the APK (pick one)
### A) GitHub (no installs needed, ~5 min)
1. Create a free GitHub repo and upload everything in this folder (keep the `.github` folder).
2. Open the repo's **Actions** tab → **Build APK** → wait for the green tick (or click *Run workflow*).
3. Open the finished run → **Artifacts** → download **CalTrack-APK** → unzip → `app-debug.apk`.

### B) Android Studio
1. Install Android Studio, choose **Open**, select this folder, let Gradle sync.
2. **Build ▸ Build Bundle(s)/APK(s) ▸ Build APK(s)**.
3. APK: `app/build/outputs/apk/debug/app-debug.apk`

### C) Command line (JDK 17 + Android SDK 34 + Gradle 8.9)
`gradle assembleDebug`

## Install on your phone
1. Copy `app-debug.apk` to the phone (USB, Drive, WhatsApp-to-self, etc.).
2. Tap it. If asked, allow **Install unknown apps** for the app you opened it from.
3. Tap Install → open **CalTrack**.
(Debug APKs are signed with Android's debug key – fine for personal use.)

## Notes
- Data is stored locally in a Room (SQLite) database and persists after closing the app.
- Nutrition values are approximate averages per 100 g; edit/add foods for exact brands.
- Calorie estimate: Mifflin-St Jeor × activity factor, −500 kcal (loss) / +400 kcal (gain).
