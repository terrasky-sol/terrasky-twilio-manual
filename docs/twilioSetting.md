# Twilioの設定

SMS送信に必要なTwilioの設定をしていきます。

##　連携に必要な情報

以下の情報がインストール後設定手順で必要となりますので、ご用意ください。

|  項目  | 取得方法 |  使用箇所  |
| ---- | ---- | ---- |
| LIVE Credentials ACCOUNT SID | Twilioダッシュボード [Settings](https://www.twilio.com/console/project/settings)のAPI Credentialsの欄  |  指定ログイン情報「TwilioSMSCredential」 |
| LIVE Credentials AUTH TOKEN | Twilioダッシュボード [Settings](https://www.twilio.com/console/project/settings)のAPI Credentialsの欄  |  指定ログイン情報「TwilioSMSCredential」 |
|  Test Credentials TEST ACCOUNT SID | Twilioダッシュボード [Settings](https://www.twilio.com/console/project/settings)のAPI Credentialsの欄  |  指定ログイン情報「TestTwilioSMSCredential」 |
| Test Credentials TEST AUTHTOKEN  | Twilioダッシュボード [Settings](https://www.twilio.com/console/project/settings)のAPI Credentialsの欄  |  指定ログイン情報「TestTwilioSMSCredential」 |
|  Api key SID  |  Twilioダッシュボード [API Keys](https://www.twilio.com/console/project/api-keys)  |  指定ログイン情報「TwilioSMSCredential」 |
|  Api key SECRET  |  Api key作成時のみ表示される。  |指定ログイン情報「TwilioSMSCredential」 |
|  MessagingServiceSID  | Twilioダッシュボード [Messaging Services](https://www.twilio.com/console/project/api-keys)  |  指定ログイン情報「TwilioSMSCredential」 |

## ログイン

[Twilio USログイン](https://www.twilio.com/login)

Twilioアカウント未取得の場合は[こちら](https://www.twilio.com/try-twilio)から作成してください。

## 電話番号の取得

Messaging Serviceを作成する際に、1つ以上電話番号を登録する必要があります。<br>電話番号を未取得の場合は、[こちら](https://jp.twilio.com/docs/usage/tutorials/how-to-use-your-free-trial-account#get-your-first-twilio-phone-number)をご参考に取得してください。
<br>※SMS送信が可能な電話番号であるUS電話番号を取得してください。

## Programmable SMSのMessaging Serviceを新規作成

[こちら](https://www.twilio.com/console/sms/services)からMessaging Serviceを未作成の場合は、新規作成します。

## API KEYの作成
[こちら](https://www.twilio.com/console/project/api-keys)からAPI KEYを未作成の場合は新規作成します。