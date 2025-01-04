## 第６回課題

### 実施内容
1.最後にAWSを利用した日の記録をCloudTrailのイベントから3つ探し出す<br>
"eventTime": "2024-07-13T04:53:06Z"<br>
"eventSource": "ec2.amazonaws.com"<br>
"eventName": "DeleteNetworkInterface"<br>
![1.最後にAWSを利用した日の記録をCloudTrailのイベントから3つ探し出す](/image/1.最後にAWSを利用した日の記録をCloudTrailのイベントから3つ探し出す.png)

2.AmazonSNS作成<br>
![2.AmazonSNS作成](/image/2.AmazonSNS作成.png) 

3.CloudWatchにてアラームの作成<br>
![3.CloudWatchにてアラームの作成](/image/3.CloudWatchにてアラームの作成.png)

4.アラート状態(Helthyの時)<br>
![4.アラート状態(Helthyの時)](/image/4.アラート状態(Helthyの時).png)

5.アラート状態(unhelthyの時)<br>
![5.アラート状態(unhelthyの時)](/image/5.アラート状態(unhelthyの時).png)　

6.アラートメール(Helthyの時)<br>
![6.アラートメール(Helthyの時)](/image/6.アラートメール(Helthyの時).png)

7.アラートメール(unhelthyの時)<br>
![7.アラートメール(unhelthyの時)](/image/7.アラートメール(unhelthyの時).png)

8.AWS利用料の見積もりを作成<br>
![8.AWS利用料の見積もりを作成](/image/8.AWS利用料の見積もりを作成.png) 
https://calculator.aws/#/estimate?id=f5c28564012475c5cbd73fc46815c476a1ea6af1

9.現在のAWS利用料の報告<br>
・VPCの料金とEC2の料金でUSD1.82となっている。<br>
・そのうち、VPC（public IPv4 address per hour）がUSD 1.81となっておりほぼVPC料金である。<br>
・EC2インスタンスでパブリックIPアドレスを解放し、利用料を減らすことを検討したい。<br>
![9.現在のAWS利用料の報告](/image/9.現在のAWS利用料の報告.png)

- 感想
    - アラートの閾値設定について0以上なのか0を含まないのか等設定ミスがあった。
    - 第５回のボリュームが大きく、第６回は比較的すんなり実装できた。
    - 見積作成やコスト管理など、改めて意識すべきだと感じた。