<div align="center">

<img src="assets/aidoit-readme-cover.png" alt="AiDoIt が AI Provider、モデル、コーディングツールを一元化" width="100%" />

<br />

[简体中文](README.md) · [English](README.en.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Deutsch](README.de.md) · [العربية](README.ar.md) · [Español](README.es.md)

<br />

[![リリース](https://img.shields.io/badge/Release-v0.0.9-7c3aed?style=for-the-badge)](https://github.com/AiDoIt-Platform/AiDoIt/releases/latest)
[![Windows](https://img.shields.io/badge/Windows-10%20%7C%2011-0ea5e9?style=for-the-badge&logo=windows11&logoColor=white)](https://github.com/AiDoIt-Platform/AiDoIt/releases/latest)
[![Ubuntu](https://img.shields.io/badge/Ubuntu-x64%20%7C%20ARM64-e95420?style=for-the-badge&logo=ubuntu&logoColor=white)](HelpMd/Ubuntu/README.md)
[![プライバシー](https://img.shields.io/badge/API_Key-ローカル保存-10b981?style=for-the-badge)](#-セキュリティとプライバシー)
[![ライセンス](https://img.shields.io/badge/License-GPLv3-f59e0b?style=for-the-badge)](LICENSE)

### AI コーディングツールとモデルを、ひとつのアプリで

AiDoIt は **Windows と Ubuntu x64 / ARM64** に対応します。Windows では **Codex、ChatGPT、Claude Code、Claude Desktop、DeepSeek Harness** を一元管理し、Ubuntu Server では Codex と Claude Code をすばやく導入できます。

[今すぐダウンロード](https://github.com/AiDoIt-Platform/AiDoIt/releases/latest) · [クイックスタート](#-クイックスタート) · [画像付きガイド](#-ドキュメント) · [問題を報告](https://github.com/AiDoIt-Platform/AiDoIt/issues/new)

</div>

---

## ✨ AiDoIt を選ぶ理由

| 機能 | 得られるメリット |
|---|---|
| **Windows + Ubuntu** | Windows 10/11 と Ubuntu x64 / ARM64 の CLI 環境をサポート |
| **一元管理** | Codex、Claude、DeepSeek Harness を設定ファイルの反復編集なしで管理 |
| **自動検出** | インストール済みアプリ、CLI、ログイン状態、実行環境を検出 |
| **複数 Provider / モデル** | Provider、認証情報、モデル一覧を分離し、既定値をいつでも切り替え |
| **有効化前の実測** | モデルの可用性と実際の応答時間を適用前に確認 |
| **独立した設定** | Codex、Claude、Harness の設定が互いに干渉しないよう分離 |
| **安全な復元** | 有効化前の状態を保存し、無効化時に公式設定へ復元 |
| **アプリ内更新** | `v0.0.7` 以降、後続の安定版をアプリ内で検出・インストール |
| **ローカルの秘密情報** | Provider API Key は端末内に保持し、UI に完全な値を表示しない |

<br />

<img src="assets/aidoit-workflow-intl.svg" alt="Provider とモデルを AiDoIt 経由で Codex、Claude、DeepSeek Harness に接続する流れ" width="100%" />

## 📦 ダウンロードとインストール

### Windows 10/11 x64

Windows の現行安定版は **AiDoIt v0.0.9** です。[GitHub Releases](https://github.com/AiDoIt-Platform/AiDoIt/releases/latest) からのみダウンロードしてください。

| パッケージ | 推奨用途 | ダウンロード |
|---|---|---|
| `AiDoIt_0.0.9_x64-setup.exe` | 一般ユーザーに推奨する標準インストーラー | [Setup EXE](https://github.com/AiDoIt-Platform/AiDoIt/releases/download/v0.0.9/AiDoIt_0.0.9_x64-setup.exe) |

> [!TIP]
> チェックサム確認、上書き更新、MSI のサイレントインストールは [Windows インストールガイド](HelpMd/Windows/Installation/README.md) を参照してください。

### macOS (Apple Silicon)

[AiDoIt v0.0.9 DMG をダウンロード](https://github.com/AiDoIt-Platform/AiDoIt/releases/download/v0.0.9/AiDoIt_0.0.9_aarch64.dmg)

AiDoIt を Applications にドラッグしてください。

このビルドは ad-hoc 署名で、Apple の公証は受けていません。初回起動時は右クリックして「開く」を選択する必要がある場合があります。

### Ubuntu x64 / ARM64

オンラインスクリプトで Codex、Claude Code、または両方を導入します。

```bash
curl -fsSL https://service.aidoit.pro/install | bash
```

アンインストール時は、導入前に保存したユーザー設定を復元できます。

```bash
curl -fsSL https://service.aidoit.pro/uninstall | bash
```

> [!IMPORTANT]
> `curl | bash` はリモートスクリプトを直接実行します。ドメインと配布元を確認し、完全な [Ubuntu 画像付きガイド](HelpMd/Ubuntu/README.md) に従ってください。

## 🚀 クイックスタート

### Windows

1. AiDoIt をインストールして起動し、ローカルツールとログイン状態を検出します。
2. **Codex 接続**、**Claude Code 接続**、または **DeepSeek Harness** を開きます。
3. 信頼できる Base URL と API Key で Provider を追加します。
4. モデルを取得または追加し、先に可用性テストを実行します。
5. 既定の Provider とモデルを選択して接続を有効にします。
6. 無効化すると、有効化前の公式設定へ復元できます。

### Ubuntu

1. Codex または Claude Code を実行する一般ユーザーでサーバーにログインします。
2. 上記のコマンドを実行し、`sk` または `account` を選びます。
3. 導入対象として `both`、`codex`、`claude` のいずれかを選びます。
4. `codex` または `claude` を起動し、`/model` でモデルを選択・テストします。

| 目的 | ガイド |
|---|---|
| Codex / ChatGPT で Provider モデルを使う | [Windows Codex ガイド](HelpMd/Windows/Codex/README.md) |
| Claude Code / Desktop で Provider モデルを使う | [Windows Claude ガイド](HelpMd/Windows/Claude/README.md) |
| Ubuntu で Codex / Claude Code を設定する | [Ubuntu 導入・利用ガイド](HelpMd/Ubuntu/README.md) |

## 🧩 主な機能

<details open>
<summary><strong>Codex と ChatGPT の接続</strong></summary>

- Codex、ChatGPT、Codex CLI、ログイン状態を自動検出。
- 公式モデルと外部 Provider モデルを併用。
- Codex のインストール、選択、起動と、有効化前の実モデルテストに対応。
- アプリ使用中は通常終了または強制終了を選んで続行可能。

</details>

<details>
<summary><strong>Claude Code と Claude Desktop</strong></summary>

- Claude Code を自動検出・インストール・起動。
- Claude Desktop を検出して開くか、ローカルインストーラーを選択。
- Claude の Provider、モデル、認証情報を Codex から分離。
- 無効化時に以前の設定とモデル構成を復元。

</details>

<details>
<summary><strong>DeepSeek Harness の管理</strong></summary>

- DeepSeek Harness Web のインストール、起動、停止、表示を管理。
- Provider、認証情報、モデル、既定モデルを独立管理。
- コンテキストと推論能力を表示し、実応答テストを実行。
- Harness の既存 Agent、ツール、セッション、タスク履歴には干渉しません。
- 実行中の設定を保護し、停止後に編集を再開できます。

</details>

<details>
<summary><strong>Provider とモデルの管理</strong></summary>

- 複数 Provider のエンドポイント、キー、モデル、有効状態を個別に管理。
- 上流モデルを自動取得するか、一覧を手動で編集。
- 認証情報を再入力せず、お気に入りと既定モデルを切り替え。
- 中国語と英語の UI を即時切り替えし、選択を記憶。

</details>

## 📚 ドキュメント

| プラットフォーム | ガイド |
|---|---|
| Windows | [インストールと更新](HelpMd/Windows/Installation/README.md) · [Codex](HelpMd/Windows/Codex/README.md) · [Claude](HelpMd/Windows/Claude/README.md) |
| macOS | [Codex](HelpMd/macOS/Codex/README.md) · [Claude](HelpMd/macOS/Claude/README.md) |
| Ubuntu | [インストール、設定、テスト](HelpMd/Ubuntu/README.md) |

[AiDoIt ヘルプセンター](HelpMd/README.md) からプラットフォーム別に探すこともできます。

## 🔐 セキュリティとプライバシー

- Provider API Key と関連設定は端末内に残り、完全なキーは UI に表示されません。
- Codex、Claude、Harness の認証情報と設定は互いに分離されます。
- 接続前の状態を保存し、後から公式設定へ復元できます。
- Issue、ログ、画像を共有する前に、キー、ユーザー名、ローカルパス、接続先を隠してください。

> [!IMPORTANT]
> AiDoIt が管理するのはローカル設定とルーティングです。外部 Provider へのリクエストには各社のプライバシーポリシー、料金、規約が適用されます。信頼できる Provider のみを使用してください。

## ❓ よくある質問

<details>
<summary><strong>公式設定は上書きされますか？</strong></summary>

有効化時に元の状態を保存し、無効化時に復元できます。Codex、Claude、Harness は独立して管理されます。

</details>

<details>
<summary><strong>モデルの検出やテストが失敗するのはなぜですか？</strong></summary>

Base URL、API Key、ネットワーク接続、Provider が必要なプロトコルに対応しているか確認してください。完全なキーは公開しないでください。

</details>

## 💬 お問い合わせとフィードバック

- プロジェクト：[AiDoIt-Platform/AiDoIt](https://github.com/AiDoIt-Platform/AiDoIt)
- 問題・提案：[Issue を作成](https://github.com/AiDoIt-Platform/AiDoIt/issues/new)
- 過去のバージョン：[GitHub Releases](https://github.com/AiDoIt-Platform/AiDoIt/releases)
- ライセンス：[GNU GPL v3](LICENSE)

<div align="center">

**AiDoIt — あらゆるモデルを、より手軽に AI 開発ワークフローへ。**

</div>
