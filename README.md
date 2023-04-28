# test-repo

## 手順

### 必要ツールインストール

- PowerShellを**管理者権限で**起動
- 次を入力: `winget install Microsoft.WindowsTerminal`
- 次を入力: `winget install Microsoft.VisualStudioCode`

### WSL2インストール

- [WSL2を使用してUbuntuをインストールする - 半導体事業 - マクニカ](https://www.macnica.co.jp/business/semiconductor/articles/qualcomm/142363/)

### WSL設定

- Windows Terminal(ターミナル)を起動
- 画面上部タブ一覧の `▽` を押して `Ubuntu` を起動

以下のコマンドを入力して `systemd` を有効化する

```bash
sudo echo "
[boot]
systemd=true
" >> /etc/wsl.conf
```

終わったらPowerShellで `wsl --shutdown` と入力し、WSL再起動

### Docker for Linux インストール

- Windows Terminal(ターミナル)を起動
- 画面上部タブ一覧の `▽` を押して `Ubuntu` を起動
- ↓の手順でWSLをインストール
  - [WSL2 Ubuntu に Docker をインストールする](https://zenn.dev/fehde/articles/ea0e8a0a0a1de4)
- 入力: `sudo service docker start`
  - Docker初回起動チェック。問題があれば誰かに聞こう
- 入力: `sudo systemctl enable docker`
  - Dockerデーモン自動起動
- PowerShellで `wsl --shutdown` と入力し、WSL再起動

### VSCodeインストール

- VSCodeを起動
- 次のExtensionを入れる
  - WSL
  - Docker
  - Git History
