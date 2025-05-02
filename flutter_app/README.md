# Flutter アプリ開発環境の構築 (macOS)

macOS 11以降以降が必要です。


## 目次
- [Flutter開発環境の準備](#flutter開発環境の準備)
- [iOS アプリ開発環境の構築](#ios-アプリ開発環境の構築)
- [Android アプリ開発環境の構築](#android-アプリ開発環境の構築)
- [アプリの実行](#アプリの実行)

## Flutter開発環境の準備(Cursor/VSCode)
1. Cursor/VSCodeに[Flutterの拡張機能](https://marketplace.visualstudio.com/items?itemName=Dart-Code.flutter)をインストール
2. ドキュメントの指示に従って[Flutter SDKをインストール](https://docs.flutter.dev/get-started/install/macos/mobile-android#install-the-flutter-sdk)
3. Rosseta 2 をインストール(Apple Silicon搭載Macのみ)
    ```zsh
    sudo softwareupdate --install-rosetta --agree-to-license
    ```

## [iOS アプリ開発環境の構築](https://docs.flutter.dev/get-started/install/macos/mobile-ios)

### 1. Xcodeのインストールとセットアップ
1. [Xcodeをインストール](https://developer.apple.com/xcode/)
2. コマンドラインツールを設定
   ```zsh
   sudo sh -c 'xcode-select -s /Applications/Xcode.app/Contents/Developer && xcodebuild -runFirstLaunch'
   ```
   > 注: 過去バージョンを使う場合は、パスを適切に変更してください
3. Xcodeのライセンスに署名
   ```zsh
   sudo xcodebuild -license
   ```
4. 仮想デバイスをセットアップ
   ```zsh
   xcodebuild -downloadPlatform iOS
   ```

### 2. CocoaPodsのインストール
1. cocoapods をインストール
   ```zsh
   gem install cocoapods
   ```

手順完了後、以下のコマンドを実行してエラーが出なければ正常に設定できています：
```zsh
flutter doctor
```

## [Android アプリ開発環境の構築](https://docs.flutter.dev/get-started/install/macos/mobile-android)

### Android Studioのインストールとセットアップ
1. [Android Studioをインストール](https://developer.android.com/studio?hl=ja)
2. 以下のAndroidコンポーネントを全てインストール。詳細な手順は[ドキュメントを参照](https://docs.flutter.dev/get-started/install/macos/mobile-android#configure-the-android-toolchain-in-android-studio)
    - Android SDK Platform, API 35.0.2
    - Android SDK Command-line Tools
    - Android SDK Build-Tools
    - Android SDK Platform-Tools
    - Android Emulator
3. Android SDK プラットフォームのライセンスに署名
    ```
    flutter doctor --android-licenses
    ```
4. 仮想デバイスをセットアップ
[ドキュメントに従ってインストールする](https://docs.flutter.dev/get-started/install/macos/mobile-android#configure-your-target-android-device)


手順完了後、以下のコマンドを実行してエラーが出なければ正常に設定できています：
```zsh
flutter doctor
```

## アプリの実行

### パッケージのインストール
```zsh
flutter pub get
```

### アプリの起動
```zsh
flutter run
```
