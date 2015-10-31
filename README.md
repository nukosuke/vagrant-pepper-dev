# vagrant-pepper-dev
pepperのpythonによる開発用

## セットアップ
リポジトリをクローンします。

```sh
$ git clone git@github.com:imkitchen/vagrant-pepper-dev.git
```

### Pepper Python SDK
SDKの再配布ができそうにないので各自で取得してください。

[ALDEBARANの公式サイト](https://community.aldebaran.com/ja/resources/software)からPepper Python SDKをダウンロードしてください。
ダウンロードには事前にAldebaranコミュニティのアカウントを取得しておく必要があります。お金はかかりません。

[![https://gyazo.com/a2775d0a4d9f2ee93f7407652dfd5647](https://i.gyazo.com/a2775d0a4d9f2ee93f7407652dfd5647.png)](https://gyazo.com/a2775d0a4d9f2ee93f7407652dfd5647)

VMはUbuntu 14.04なのでLinux用のSDKをダウンロードします。

ダウンロードが完了したら `data` ディレクトリにアーカイブファイルをそのまま配置します。

```sh
$ cd vagrant-pepper-dev
$ mv ~/Downloads/pynaoqi-python2.7-2.3.1.25-linux64.tar.gz ./data
```

### VM起動
VMを起動する前にansibleというプロビジョニングツールをホスト側にインストールしておく必要があります。

Macをお使いでHomebrewが入っている場合は

```sh
$ brew install ansible
```

でインストール可能です。

以下のコマンドでVMを起動します。

```sh
$ vagrant up
```

しばらく時間がかかるのでコーヒーでも飲んでいてください。
これで完了です。sshで接続できます。

```sh
$ vagrant ssh
```

`data` ディレクトリに置いたファイルはゲスト・ホスト間で共有されますのでホスト側でお好きなエディタを使って開発することもできます。
