# vagrant-inside_docker-compose_code
vagrantの中にデスクトップubuntu+dokcer-composeが入っています。簡単に作成、捨てられる開発環境としてどうぞ。
## 使い方
前提としてvirtualbox,vagrantはインストール済みとします。

`
$ git clone https://github.com/KatsutoshiOtogawa/vagrant-inside_docker-compose_code.git
`

vagrantの中でdocker-composeを使うため、
vb.memoryはデフォルトで8Gに設定しています。
大きすぎるならホスト側のpcのメモリに合わせて修正してください。

`
$ vagrant up 
`

上記のコマンドを実行すると、ターミナル上で
デスクトップのインストールが始まります。
何十分かかりますので、気長に待ちましょう。

デスクトップ環境をインストールし終わると、
自動でvagrantがhaltとなるので、
もう一度

`
$ vagrant up
`

と実行します。
デスクトップ環境ができたら成功です。
## 初期パスワード
よくあるように
ユーザー vagrant パスワード vagrant
となっております。
都合が悪いなら

`
$ passwd
`

と実行してパスワードを変更してください。
## その他の設定
デスクトップ環境作成後は、ターミナルから下記のコマンドを実行することにより、設定の反映を行ってください。
### キーボードの設定
下記のコマンドを押すとキーボードの設定になります。
macの場合はキーボードレイアウトは
Apple Alminium (JIS)
になります。

`
$ sudo dpkg-reconfigure keyboard-configuration
`

### タイムゾーンの設定
デフォルトではUTCに設定されています。
Asia/Tokyoにタイムゾーンを設定する場合は
下記のようになります。

`
$ sudo timedatectl set-timezone Asia/Tokyo
`

### システムの言語の設定
デフォルトでは英語でインストールされています。
下記のコマンドにより変更することができます。

`

`

## Referrence

[docker-composeのvagrant](https://app.vagrantup.com/gusztavvargadr/boxes/docker-linux)

