# 夫婦共有生活ダッシュボードアプリ

iPhone向けの「夫婦共有生活ダッシュボードアプリ」を、**React Native + Expo + TypeScript**で段階的に開発するプロジェクトです。  
このREADMEは、**初心者向けに「開発環境構築」と「起動方法」**を迷わず進められるように整理しています。

---

## 0. このREADMEでわかること

- 開発に必要なツール
- Windows環境を前提にしたセットアップ手順
- プロジェクト作成〜起動までのコマンド
- iPhone実機での確認方法
- 日々の開発開始手順

---

## 1. 前提技術スタック

- React Native
- Expo
- TypeScript
- Git / GitHub
- iPhone向け優先（Windowsでも開発しやすい運用）

---

## 2. 開発環境構築

### 2-1. 必要ツール

以下を先にインストールしてください。

- **Node.js LTS（推奨: 20系）**
- **npm**（Node.jsに同梱）
- **Git**
- **Visual Studio Code**
- **iPhone（実機確認用）**
- **Expo Go（iPhoneアプリ）**

### 2-2. バージョン確認

```bash
node -v
npm -v
git --version
```

エラーが出る場合は、インストールやPATH設定を見直してください。

### 2-3. VS Code推奨拡張

- ESLint
- Prettier - Code formatter
- React Native Tools
- Error Lens
- GitLens
- Path Intellisense

---

## 3. プロジェクト作成手順（新規作成する場合）

```bash
npx create-expo-app@latest couple-dashboard
cd couple-dashboard
npm install
npx expo start
```

> 補足: TypeScriptテンプレートを明示する場合は `--template` オプションで選択してください。

---

## 4. 既存プロジェクトの起動方法（このリポジトリを使う場合）

### 4-1. リポジトリ取得

```bash
git clone <your-repo-url>
cd codex-test
```

### 4-2. 依存関係インストール

```bash
npm install
```

### 4-3. Expo起動

```bash
npx expo start
```

必要に応じて以下を使います。

- `npx expo start --tunnel`（同一Wi-Fiでつながりにくい時）
- `npx expo start --clear`（キャッシュ問題の切り分け時）

---

## 5. iPhone実機での確認方法

1. App Storeで **Expo Go** をインストール
2. PCとiPhoneを同じネットワークに接続
3. `npx expo start` 実行後に表示されるQRコードをiPhoneで読み取り
4. Expo Goでアプリを開く

---

## 6. 開発開始時の最短フロー（毎回これだけ）

```bash
git pull
npm install
npx expo start
```

作業前にブランチを切る運用を推奨します。

```bash
git checkout -b feature/<task-name>
```

---

## 7. GitHub運用（初心者向け）

- `main`: 常に動く安定版
- `feature/*`: 機能開発ブランチ
- Pull Requestで差分確認してから `main` にマージ

例:

```bash
git checkout -b feature/shopping-list
# 開発
git add .
git commit -m "feat: add shopping list MVP"
git push -u origin feature/shopping-list
```

---

## 8. 設計・要件ドキュメント

- 要件定義: [`docs/requirements.md`](docs/requirements.md)
- 開発ロードマップ: [`docs/roadmap.md`](docs/roadmap.md)
- UIガイドライン: [`docs/ui-guidelines.md`](docs/ui-guidelines.md)

---

## 9. 補足（よく使うコマンド）

```bash
# Expo開発サーバー起動
npx expo start

# 依存再インストール
rm -rf node_modules package-lock.json
npm install

# キャッシュクリア起動
npx expo start --clear
```
