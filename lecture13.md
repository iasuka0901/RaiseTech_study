## 第１３回課題

### 概要
- CircleCIのサンプルにServerspecやAnsibleの処理を追加する
- 感想
※ 作成したコード等の詳細については[第13回課題リポジトリ](https://github.com/iasuka0901/AWS-lecture13)を参照

#### AWS構成図
![AWS構成図](/image/lecture13/AWS構成図.jpg)

### 実施内容
#### 1. 事前準備
- EC2の接続に使うキーペアは事前に作成したものを使用
- CircleCIの環境変数の設定

#### 2. CircleCIの実行結果
- 全てのワークフロー<br>![Workflowが全て成功](/image/lecture13/Workflowが全て成功.png)
- cfn-lint<br>![cfn-lint成功](/image/lecture13/cfn-lint成功.png)
- execute-cloudformation<br>![cloudformation成功](/image/lecture13/execute-cloudformation成功.png)
- execute-ansible<br>![ansible成功](/image/lecture13/execute-ansible成功.png)
- execute-serverspec<br>![execute-serverspec成功](/image/lecture13/execute-serverspec成功.png)

####  3. サンプルアプリケーションの動作確認
-  ALBのDNSにアクセスして画像をアップロード<br>![ALBへアクセス](/image/lecture13/ALBへアクセス.png)
- 保存先がS3になっているか確認<br>![保存先がS3になっている](/image/lecture13/保存先がS3になっている.png)

####  4. 感想
- 環境変数がキャッシュされたり、RDSのパスワード（SercretManager利用）をうまく連携できなかったりかなりの時間を要してしまったが非常に勉強となる課題だった。
- CircleCIなどのCI/CDツールとAnsibleを組み合わせると、コード管理やビルド・テストが素早くできて、もっと理解を深めて活用すれば開発に役立つと感じた。