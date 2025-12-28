# Learn AWS by Coding 学習ログ

[Learn AWS by Coding](https://tomomano.github.io/learn-aws-by-coding/) を進めるためのリポジトリです。

## 🎯 学習の目標
- AWS CDK（TypeScript/Python）の基本をマスターする
- dockerの使い方をハンズオンで学ぶ
- IaC (Infrastructure as Code) の考え方を身につける
- AWSの主要サービス（EC2, Lambda, S3, etc.）の連携を理解する

## 📊 進捗管理表
| 章 | タイトル | ステータス | 完了日 | 内容 |
| :--- | :--- | :--- | :--- | :--- |
| 15,1-3.3 | 開発環境の構築 | 済 | 12/24 | AWSアカウントの取得、シークレットキーの作成、CLI,CDKのインストール、WSL2/Dockerのセットアップ |
| 3.4- | 最初のアプリ作成 | 済 | 12/26 | AWS CLIを使ってみた、 |
| 4.44- | dploy | 済 | 12/28 | EC2インスタンスを起動できなかった、一旦飛ばす |
| 6- | :--- | :--- | :--- | :--- |

## 💡 詰まったポイント・学び
### 2025/12/25: deploy時のnodeのバージョンが古かった
- **事象:** `cdk deploy` でエラー
- **原因:** IAMユーザーの権限不足
- **解決:** ファイルを編集して最新のパッケージを入れなおした、app.py内のauto_delete_objectsをTrueからFaslseにした

### 2025/12/28: deployできなかった
- **事象:** `cdk deploy` でエラー
- **原因:** 指定されたインスタンスタイプは無料枠アカウントの対象外だった
- **解決:** アカウントの制限は詰み、なので一旦#1は飛ばす
