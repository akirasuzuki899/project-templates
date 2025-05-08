# Expo アプリ開発環境の構築 (macOS)

## 目次
- [Nodeのインストール](#Nodeのインストール)
- [Watchmanインストール](#Watchmanインストール)
- [Expo アプリの作成・実行](#android-アプリ開発環境の構築)
- [アプリの実行](#アプリの実行)

## Nodeのインストール
1. node のバージョン管理ツール nvm をインストール
```zsh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
nvs --version
```
2. Node.js をインストール

[LTSステータスのNode.js](https://nodejs.org/ja/about/previous-releases)をインストール
```zsh
nvs add 22
```

## [Watchmanインストール](https://docs.flutter.dev/get-started/install/macos/mobile-ios)
```zsh
brew install watchman
```
