---
title: プライバシーポリシー / Privacy Policy
lang: ja
---

# Hotaru プライバシーポリシー

最終更新日：2026年11月20日

[English](#hotaru-privacy-policy)

Hotaru（以下「本アプリ」）は、sea-edge（以下「開発者」）が提供する、端末の中で AI を動かすアプリです。本アプリでどのような情報が端末の外に送られるかを説明します。

## 1. 基本方針

- 通常のチャット、文書への質問、画像生成は端末内で処理します。Web 検索や報告など、選んだ機能に応じて外部に送られる内容は下記のとおりです。
- アカウント登録は不要です。
- 広告は表示せず、広告のためのツール（SDK）も組み込んでいません。利用状況を分析するためのツールは、2.1 の ML Kit を除いて組み込んでいません。

## 2. 外部サービスや他のアプリに渡す情報

### 2.1 Gemini Nano の対応状況を確認するとき・利用するとき

Hotaru は初回案内やモデル画面などで Google の ML Kit を使い、Gemini Nano の利用可否を確認します。対応端末では Google のシステムサービス AICore を使って推論します。ML Kit は診断と利用状況の分析のため、次の情報を Google に送ります。

- 端末の情報（メーカー、機種、OS のバージョン、利用可能な機械学習アクセラレータ）
- 本アプリの情報（パッケージ名、バージョン）
- ユーザー・端末などの識別子、インストールごとの識別子
- 入力と出力のサイズ、処理時間などの性能指標、機能の設定・バージョン、設定言語、イベントの種類、エラーコード

入力した文章・画像や回答の内容は端末内で処理されます。診断情報の詳細は Google の資料をご覧ください。[ML Kit のデータ開示](https://developers.google.com/ml-kit/android-data-disclosure)・[Google のプライバシーポリシー](https://policies.google.com/privacy)

### 2.2 Web 検索をオンにしたとき

送信時に「Web 検索」がオンなら、そのメッセージの本文を検索語として Brave Search または DuckDuckGo に送ります。既定はオフです。設定でオンの状態を次のメッセージにも引き継げます。自動設定では登録済みの API キーを Brave Search に送り、キーがない場合や検索が失敗した場合は DuckDuckGo を利用します。

上位の検索結果のページに接続して関連箇所を読み込みます。検索サービスと接続したサイトには、IP アドレス、Hotaru のバージョン、端末の言語などの通信情報が伝わります。出典の URL や引用を、端末内の会話履歴に保存します。

送られた情報は、各サービスのプライバシーポリシーに従って扱われます（[Brave Search](https://search.brave.com/help/privacy-policy)、[DuckDuckGo](https://duckduckgo.com/privacy)）。

### 2.3 AI モデルを検索・ダウンロードするとき

Hugging Face または Civitai で検索すると、検索語や指定したモデルの ID がそのサービスに伝わります。モデルを選んで取得すると、配布元や配信用のサーバーには、リクエストしたファイル、IP アドレスなどが伝わります。認証情報を登録している場合は、Hugging Face へは Hugging Face のトークン、Civitai へは Civitai の API キーを送ります。これらと Brave Search のキーは、Android Keystore の鍵を使って端末内に暗号化して保存します。

### 2.4 不適切な出力を報告するとき

報告を確定すると、報告 ID、対象の種類、理由、任意のコメント、モデル ID、アプリのバージョンと、次の対象内容を開発者へ送ります。

- チャットの回答は、その回答の本文。
- 生成画像は、画像の生成に使ったプロンプト、seed（生成時の乱数の値）、モデル名。
- 合成音声は、読み上げ用の入力文、声の種類、モデル名。

画像ファイルや音声ファイルは添付しません。報告対象のテキストやコメントに個人情報が含まれる場合は、その情報も送られます。端末には報告と送信状態が保存されます。オフラインなどで配信が保留になった報告は、接続の回復後に再送されることがあります。

報告は、開発者が管理する Google スプレッドシートに（Google Apps Script を通して）保存し、不適切な出力を減らすためのフィルターの改善にだけ使います。受け取ってから 1 年後に削除します。

### 2.5 マイク・読み上げ・通知

音声入力を選んだときは、マイクの許可を求めます。音声は Android の端末内音声認識または対応する端末内モデルで処理します。Hotaru の音声合成モデルを導入した場合は、端末内で音声を生成します。システム読み上げを選ぶと、読み上げる本文を Android で選択中の音声エンジンに渡します。エンジンが音声の情報を提供しない場合もあり、そのエンジンによる本文の取り扱いや通信は、提供元と端末の設定に従います。

通知の許可は、モデルのダウンロード、回答生成、画像生成の進行を Android に表示するために使います。ダウンロードの通知にはモデル名と進捗が表示されます。

## 3. 端末内に保存される情報

会話履歴、取り込んだ文書の本文と検索用データ、添付・録音、生成画像・音声、モデル、設定、報告の控えは本アプリ専用の領域に保存されます。会話、文書、モデルなどはそれぞれの画面から削除できます。Android の設定でアプリのストレージを消去するか、アンインストールすると、アプリ専用領域のデータが削除されます。開発者がすでに受け取った報告の削除は、6 章の窓口で受け付けます。

## 4. 第三者への提供

画像を共有すると、その画像を Android の共有画面で選択したアプリへ渡します。画像や音声を端末の共有ストレージに書き出した場合は、保存先にコピーが残ります。本アプリを削除しても、共有先のコピーや、取り込み元の写真・文書は残ります。削除するには保存先や共有先の機能をご利用ください。開発者が情報を第三者に提供するのはこのポリシーに記載した場合に限り、情報を販売することはありません。

## 5. 子どもの利用

本アプリは 13 歳未満の子どもを対象としていません。

## 6. 削除の依頼・お問い合わせ

開発者に送られた報告の削除や、このポリシーについてのお問い合わせは、次のメールアドレスまでご連絡ください。

kaihatsu.dev@gmail.com

## 7. 改定

このポリシーを変更する場合は、このページで告知します。

---

# Hotaru Privacy Policy

Last updated: November 20, 2026

Hotaru ("the app") is an app by sea-edge ("the developer") that runs AI on your device. This page explains what information leaves your device.

## 1. Our approach

- Ordinary chat, document questions and image generation run on your device. The information sent when you use features such as web search or reporting is described below.
- No account is required.
- The app shows no ads and contains no advertising SDKs. Apart from ML Kit (section 2.1), it contains no analytics SDKs.

## 2. Information sent to other services or apps

### 2.1 Checking or using Gemini Nano

Hotaru uses Google ML Kit to check whether Gemini Nano is available, including during onboarding and on the models screen. On supported devices, Google's AICore system service runs inference. ML Kit sends the following information to Google for diagnostics and usage analytics.

- Device information (manufacturer, model, OS version and available machine learning accelerators)
- App information (package name, version)
- User, device or other identifiers, as well as per-installation identifiers
- Input and output sizes, performance metrics such as latency, feature configuration and version, configured languages, event types and error codes

The content of your prompts, images and answers is processed on your device. Google describes the diagnostic information in its documentation. [ML Kit data disclosure](https://developers.google.com/ml-kit/android-data-disclosure) and [Google Privacy Policy](https://policies.google.com/privacy)

### 2.2 When you turn on web search

If web search is on when you send a message, Hotaru sends the message text as a query to Brave Search or DuckDuckGo. Web search is off by default. You can choose to keep it on for subsequent messages. In automatic mode, Hotaru sends your configured API key to Brave Search. It uses DuckDuckGo when no key is configured or the Brave search fails.

Hotaru opens top result pages to read relevant passages. Search providers and the sites contacted receive request information including your IP address, Hotaru version and device language. Source URLs and excerpts are saved in your local chat history.

That information is handled under each service's privacy policy ([Brave Search](https://search.brave.com/help/privacy-policy), [DuckDuckGo](https://duckduckgo.com/privacy)).

### 2.3 When you search for or download AI models

When you search Hugging Face or Civitai, that service receives your search terms or the model ID you entered. When you choose a model to download, the provider and its delivery servers receive the file request and information such as your IP address. If you configure credentials, Hotaru sends your Hugging Face token to Hugging Face and your Civitai API key to Civitai. Hotaru stores these credentials and any Brave Search key encrypted on your device using a key in Android Keystore.

### 2.4 When you report an output

When you confirm a report, Hotaru sends the developer a report ID, output type, reason, optional comment, model ID, app version and the following information about the selected output.

- For a chat answer, the text of that answer.
- For a generated image, its prompt, seed (the random value used in generation) and model name.
- For synthesized speech, the input text, voice and model name.

Image and audio files are not attached. Any personal information in the reported text or your comment is included. A copy of the report and its delivery status are stored on your device. Pending reports may be retried when a connection becomes available.

Reports are stored in a Google Sheets spreadsheet managed by the developer (received through Google Apps Script), used only to improve content filtering, and deleted one year after they are received.

### 2.5 Microphone, read-aloud and notifications

Hotaru requests microphone permission when you choose voice input. Android's on-device speech recognizer or a compatible local model processes the audio. Hotaru's downloadable speech synthesis model also runs on your device. When you choose system read-aloud, Hotaru passes the text to the speech engine selected in Android. Some engines do not identify their available voices. How the engine handles text and uses the network depends on its provider and your device settings.

Hotaru uses notification permission to show model downloads, answer generation and image generation in progress. Download notifications show the model name and progress.

## 3. Information stored on the device

The app's private storage holds chat history, imported document text and indexes, attachments, recordings, generated images and audio, models, settings and local report copies. You can delete conversations, documents and models from their respective screens. Clearing the app's storage in Android settings or uninstalling removes the data in its private storage. To delete a report already received by the developer, use the contact in section 6.

## 4. Sharing with third parties

When you share an image, Hotaru passes it to the app you choose in the Android share sheet. Saving an image or audio file to shared storage creates a separate copy. Shared copies and original photos or documents you imported remain after you uninstall Hotaru. Use the destination app or storage location to delete those copies. The developer shares information only as described in this policy and does not sell it.

## 5. Children

The app is not directed at children under 13.

## 6. Deletion requests and contact

To request deletion of a report you sent, or for questions about this policy, contact:

kaihatsu.dev@gmail.com

## 7. Changes

Changes to this policy will be announced on this page.
