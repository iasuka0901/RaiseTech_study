## 第１０回課題

### 実施内容
1. 第５回でAWSマネジメントコンソールを使って構築した環境をCloudFormationで構築する
   テンプレートファイル [stack-lecture10.yml](/file/stack-lecture10.yml) を作成しスタックを作成
   <br>
   
| 構築したもの                                         | 
| :--------------------------------------------------- | 
| VPC                                                  | 
| サブネット                                           | 
| インターネットゲートウェイ                           | 
| VPCGatewayAttachment                                 | 
| ルートテーブル                                       | 
| サブネットとルートテーブルの関連付け                 | 
| インターネットゲートウェイとルートテーブルの関連付け | 
| セキュリティグループ                                 | 
| S3バケット                                           | 
| IAMロールの定義                                      | 
| IAMインスタンスプロファイルの定義                    | 
| EC2インスタンス                                      | 
| RDSインスタンス                                      | 
| RDSのサブネットグループ                              | 
| ELB（ALB）のターゲットグループ                       | 
| ELB（ALB）                                           | 
| ELB（ALB）のHTTPリスナー                             | 

- CloudFormationの結果<br>
![CloudFormationの結果](/image/CloudFormationの結果.png) 

- EC2へSSH接続確認<br>
![EC2へSSH接続確認](/image/EC2へSSH接続確認.png)

- EC2からRDSへ接続確認<br>
![EC2からRDSへ接続確認](/image/EC2からRDSへ接続確認.png)

2. 感想
    - ただテンプレートを作成するのではなく、1行ごとに何を意味しているのか意識して作成をした。
    - スタックの変更（テンプレートの上書きの仕方等）やCloudformationで作成したものに対する手動変更についての注意点など調べた。
    - 第11回以降も頑張ります。