# ZEN ファームウェア

ZEN用のファームウェアを作成するためのリポジトリです。

GitHubに慣れていない方でも、リポジトリをforkして、Keymap Editorでキー配置を編集し、GitHub Actionsでファームウェアを作成できます。

## はじめに読むもの

詳しい手順は以下のガイドにまとめています。

- [ZEN ファームウェア案内](https://e24-gh.github.io/zen/firmware.html)

## このリポジトリでできること

- ZEN用ファームウェアのビルド
- Keymap Editorでのキー配置編集
- GitHub ActionsからのUF2ファイル作成

## 作成されるファームウェア

GitHub Actionsで作成される `firmware` というzipファイルには、以下のUF2ファイルが含まれます。

- 設定リセット用UF2ファイル
- `zen_right_trackball_pmw3610_central.uf2`
- `zen_right_trackball_paw3222_central.uf2`
- `zen_right_trackpad_central.uf2`
- `zen_left_peripheral.uf2`

通常使用するファイルは以下です。

- 右手: `zen_right_trackball_pmw3610_central.uf2`
- 左手: `zen_left_peripheral.uf2`

PAW3222やTrackpadを使用する場合は、それぞれ名前に対応する右手用UF2ファイルを使用します。標準構成ではPMW3610用を使用してください。

無線接続がうまくいかない場合や、別のファームウェアから切り替える場合は、先に設定リセット用のUF2ファイルを使います。

## 最短手順

1. このリポジトリを自分のGitHubアカウントへforkします
2. Keymap Editorでforkしたリポジトリを開きます
3. 必要に応じてキー配置を編集して保存します
4. GitHub Actionsでファームウェアがbuildされるのを待ちます
5. `firmware` のダウンロードボタンからzipファイルをダウンロードします
6. 右手と左手の対応コントローラへUF2ファイルを書き込みます
7. PCやMacの接続設定から `ZEN` として接続します

## 対象

このリポジトリは、PMW3610トラックボール版を標準構成とし、PAW3222およびTrackpadを使用するカスタム構成にも対応しています。

## うまく接続できない場合

無線接続がうまくいかない場合は、以下を試してください。

1. PCやMacの接続設定から `ZEN` を削除します
2. 設定リセット用のUF2ファイルを書き込みます
3. USBを外します
4. ZENの電源を入れます
5. もう一度通常ファームウェアを書き込みます
6. 接続設定から `ZEN` を再接続します

## ライセンス

MIT
