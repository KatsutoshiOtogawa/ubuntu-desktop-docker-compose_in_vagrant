# vagrant-inside_docker-compose_code
vagrantの中にdokcer-compose、code(visual studio codeのオープンソース版)が入っています。簡単に作成、捨てられる開発環境としてどうぞ。
## 使い方
前提としてvirtualbox,vagrantはインストール済みとします。

`
$ git clone https://github.com/KatsutoshiOtogawa/vagrant-inside_docker-compose_code.git
`

vagrantの中でdocker-compose、codeを使うため、
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

## その他の設定
デスクトップ環境作成後は、ターミナルから下記のコマンドを実行することにより、設定の反映を行ってください。
### キーボードの設定

`
$ sudo dpkg-reconfigure keyboard-configuration
`

### タイムゾーンの設定
デフォルトではUTCに設定されています。

`
# ex) Asia/Tokyoにタイムゾーンを設定する場合
$ sudo timedatectl set-timezone Asia/Tokyo
`

## Referrence

[docker-composeのvagrant](https://app.vagrantup.com/gusztavvargadr/boxes/docker-linux)

