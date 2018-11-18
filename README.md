# redmine-ansible

Vagrant + Ansibleを用いた、
Redmineのインストール用Playbookのサンプルです。
現在はWEBrickによる表示確認まで完了しています。

## 動作環境

以下の環境で確認しています。

* Vagrant: 2.1.2
* Ansible: 2.7.0

## 実行手順

Vagrantを起動してください。

```sh
vagrant up
```

しばらく待つとVault passwordを聞かれるので、'password'と入力してください。

Ansibleによるプロビジョニングが完了後、以下のようにして起動させます。

```sh
vagrant ssh
cd /opt/redmine
sudo bundle exec rails server webrick -e production --bind=0.0.0.0
```

http://localhost:3000/ にアクセスすると、Redmineの画面が表示されます。

## ライセンス

MITライセンスです。
