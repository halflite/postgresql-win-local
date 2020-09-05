# PostgreSQL Windows Local with Vagrant/Virtualbox

- VirtualBox/Vagrant で CentOS7 のインスタンスをWindows10のローカルに作ります
- CentOS7 のインスタンスにDocker/Docker-Compose を使って、 PostgreSQL 12 を建てます

### 1st step

2020/09/01 時点の環境です

- Virtualbox 6.1.12 ダウンロード/インストール
    - https://www.virtualbox.org/wiki/Downloads
- Vagrant 2.2.10 ダウンロード/インストール
    - https://www.vagrantup.com/downloads.html

### 2nd step

- このリポジトリをチェックアウト
- ディレクトリに移動し、以下のコマンドでVirtualBoxを起動

```cmd
vagrant plugin expunge --reinstall
vagrant plugin update
vagrant up --provision
```

- 以下のデータベースが作成されます
    - ホスト `192.168.33.11`
    - ポート `5432`
    - データベース `testdb`
    - 接続ユーザー `dbuser`
    - 接続パスワード `dbpassword1`
