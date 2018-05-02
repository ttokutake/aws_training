# AWSに触ってみる

IoT事業本部第1開発部4課 徳武

---

## 目的

- サーバーインフラをふんわり理解する
- PaaSやSaaSのありがたみを理解する

---

## AWSって？

- AWS(Amazon Web Services)はAmazonの提供するWebサービスのこと
- IaaS(Infrastructure as a Service)やPaaS(Platform as a Service)、SaaS(Software as a Service)を提供している

>>>

## IaaS？PaaS？SaaS？

- IaaS: Amazon EC2など。ユーザーがサーバーの細かい設定を気にしないといけない
- PaaS: Amazon RDS, Herokuなど。ユーザーは使う上でサーバーの細かい設定を気にしなくて済む
- SaaS: Amazon Rekognition, Gmailなど。ユーザーは使う上でサーバーのリソースとか気にしないで済む

>>>

## IaaSが出現する以前は...

- 自社にサーバーを用意したり
- データセンターのラックを借りたり
- VPSを利用したり

<img src="./image/datacenter-286386_1280.jpg" alt="ラックサーバー" width="320px">

>>>

## IaaSが出現して以降は...

- ボタンポチポチで簡単にサーバーが立てられる！
    - コンピューターリソースの進化
    - コンピューターの仮想化技術の発達

<img src="./image/dance_yorokobi_mai_man.png" alt="喜びの舞" width="320px">

>>>

## いろいろなクラウドベンダー

- AWS
- Microsoft Azure
- GCP(Google Cloud Platform)

---

## 実際に触ってみよう

1. Amazon EC2を触る
2. Amazon RDSを触る
3. クリーンアップ作業
    - 上記作業中に作成したコンポーネントやサービスをメモしておこう
    - (あとで滞りなくクリーンアップするためです)

---

## Amazon EC2

- 仮想サーバーを提供するサービス
- とりあえずログインして、サービス一覧からEC2を選べ！

TODO: リンク書く

>>>

## EC2の仮想サーバーを立ち上げる

- TODO: EC2起動までの手順を書いてく

>>>

## EC2インスタンスにNginxをインストール

- TODO: ssh
- TODO: Nginxをインストール/自動起動の設定
- TODO: Nginxのwelcomeページを表示

>>>

## 現状のインフラ構成図

TODO: 図を貼る

>>>

## 現状の構成の問題点

- TODO: 問題点書く

>>>

## Load Balancerを導入する

- TODO: ALBとターゲットグループの準備手順書く
- TODO: AMIの準備
- TODO: もう一台EC2インスタンスを準備する

>>>

## Auto Scaling Groupを導入する

- TODO: Auto Scaling Groupと起動設定の準備手順を書く
- TODO: Auto Scalingに紐づいていないインスタンスは削除する

>>>

## 現状のインフラ構成図

TODO: 図を貼る

---

## Amazon RDS

- マネージドなRDB(Relational DataBase)を提供するサービス
- サービス一覧からRDSを選べ！

>>>

## PostgreSQLをインストール

- Homebrew, GCC, asdfがインストールされていることを確認
    - `brew --version`
    - `gcc --version`
    - `asdf --version`
- PostgreSQLのインストール
    - `asdf plugin-add postgres`
    - `asdf install postgres 9.6.6 && asdf global postgres 9.6.6`
    - (エラーが起こらないことを祈る)

>>>

## RDBって？

>>>

## RDSの何が嬉しいの？

>>>

## RDSインスタンスを立ち上げる

- TODO: RDS起動までの手順を書いてく
- TODO: 注意点も書いておく
    - VPC内アクセス限定にしろ
    - セキュリティーグループ使え

>>>

## CLI Clientから操作

- TODO: テーブル作成
- TODO: レコード挿入
- TODO: スナップショット作成
- TODO: テーブル削除
- TODO: スナップショットから復元

---

## クリーンアップ作業

- TBD
