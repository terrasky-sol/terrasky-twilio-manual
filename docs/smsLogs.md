# SMS送信履歴

SMS送信履歴の確認方法について説明します。

## 活動履歴での確認

### SMS送信API呼び出し成功時

SMS送信API呼び出し成功時に、以下のような活動履歴が生成されます。

![SMS送信API呼び出し成功時活動履歴](img/smsLogs/smsLogSuccess.png)

|  項目  | API参照名 |  内容  |
| ---- | ---- | ---- |
|  件名  |  Subject  |  SMS送信：メッセージ内容(20文字以上の場合省略表記)  |
|  期日  |  ActivityDate  |  ジョブ実行日  |
|  優先度  |  Priority  |  Normal  |
|  コメント  |  Description  |To: 宛先電話番号 <br> Direction: outbound-api <br> Twilio URL: TwilioダッシュボードSMS送信ログURL <br> Body: 送信メッセージ |
|  状況  |  Status  |  完了  |
|  名前  |  WhoId  |  リードや取引先責任者など、人を表すオブジェクトの関連先を表示  |
|  関連先  |  WhatId  | 取引先、商談、キャンペーン、ケース、カスタムオブジェクトなど、人以外のオブジェクトの関連先を表示 |
|  Twilio SMS送信ステータス  |  TerraSkyTwilio__Twilio_SMS_SID__c  | StatusCallbackURLを設定している場合に設定される |
|  Twilio SMS　SID  |  Twilio_SMS_Status__c  | StatusCallbackURLを設定している場合に設定される |

### SMS送信API呼び出し失敗時

SMS送信API呼び出し失敗時に、以下のような活動履歴が生成されます。

![SMS送信API呼び出し失敗時活動履歴](img/smsLogs/smsLogError.png)

|  項目  | API参照名 |  内容  |
| ---- | ---- | ---- |
|  件名  |  Subject  |  SMS送信が失敗しました。管理者にお問い合わせください。  |
|  期日  |  ActivityDate  |  ジョブ実行日  |
|  優先度  |  Priority  |  Normal  |
|  コメント  |  Description  |statusCode= 200番台以外 <br> requestBody= リクエスト内容 <br> responseBody= エラーメッセージを含むレスポンス内容 |
|  状況  |  Status  |  完了  |
|  名前  |  WhoId  |  リードや取引先責任者など、人を表すオブジェクトの関連先を表示  |
|  関連先  |  WhatId  | 取引先、商談、キャンペーン、ケース、カスタムオブジェクトなど、人以外のオブジェクトの関連先を表示 |
|  Twilio SMS送信ステータス  |  TerraSkyTwilio__Twilio_SMS_SID__c  | なし |
|  Twilio SMS　SID  |  Twilio_SMS_Status__c  | なし |

## Apexジョブでの確認

ガバナ制限を回避するために、リクエストを20件づつのジョブに分けて実行しています。
それぞれのジョブ実行について、Apex ジョブにて確認できます。

[Apex ジョブキューの監視](https://help.salesforce.com/articleView?err=1&id=code_apex_job.htm&type=5)

![Apexジョブ](img/smsLogs/apexJob.png)

## Twilioダッシュボードでの確認

活動履歴のコメントにある、Twilio URL（https://www.twilio.com/console/sms/logs/SM*******）からTwilioダッシュボードで詳細なログを確認できます。
[SMS送信ログ確認の詳細はこちら](https://jp.twilio.com/docs/sms/debugging-tools#explore-your-message-logs)

![SMS送信ログ](img/smsLogs/smsLogs.png)

!!! Tips
    こちらのリンクからもSMS送信のログ一覧が確認できます。[Programmable SMS Logs](https://www.twilio.com/console/sms/logs)
