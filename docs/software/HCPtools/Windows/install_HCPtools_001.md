---
id: install_HCPtools_001
title: "HCPtoolsのインストール(Windowsの場合)"
---

## インストーラの入手

以下のリンクからインストーラがダウンロード可能です。

- <a href="https://github.com/oogasawa/nigsc_HCPtools/raw/main/1.3.0R-45/Windows/HCP_Tools_Client.msi">HCP_Tools_Client.msi</a>
- <a href="https://github.com/oogasawa/nigsc_HCPtools/tree/main/1.3.0R-45/Windows">HCP_Tools_Client.md5sum</a>


過去のバージョンなどは<a href="https://github.com/oogasawa/nigsc_HCPtools">こちらからダウンロード可能です。</a>



## HCP toolsクライアントソフトウェアのインストール

`HCP_Tools_Client.msi`をダブルクリックします。

![](HCPtools_p1.png)


「使用許諾契約書に同意します(A)」にチェックを入れ、「インストール(I)」ボタンをクリックします。

![](HCPtools_1.png)

デバイスの変更許可に「はい」と応えると、インストールが開始します。

![](HCPtools_2.png)

インストールが完了すると、下記の画面が表示されるので、「完了」ボタンをクリックします。

![](HCPtools_p3.png)


インストール後、実行コマンドが`C:\Program Files`の下に、設定ファイルが`C:\ProgramData`の下に存在することを確認して下さい。

- 実行コマンド : 'C:\Program Files\Clealink\HCP Tools\hcp.exe'
- 設定ファイル: 'C:\ProgramData\Clealink\HCP Tools\hcp.conf'



## 設定ファイルの設置

HCP toolsは、ユーザのクライアント計算機内のユーザディレクトリ直下の`.hcp`ディレクトリ（または`_hcp`ディレクトリ）の中にある設定ファイルを参照します。



Windows PowerShellをご使用の場合は以下のコマンドで設定ファイルの雛形をコピーできます。

```bash
mkdir C:\Users\ユーザ名\.hcp
cp "C:\ProgramData\Clealink\HCP Tools\*.conf" C:\Users\ユーザ名\.hcp
```


## 設定ファイルの編集 

HCP toolsの設定ファイルをユーザディレクトリに設置し、ユーザ認証のための公開鍵の設定を追記します。

手順については[設定ファイルの書き方](/software/HCPtools/hcptools_conf)を参照して下さい。
