---
title: プライバシーポリシー / Privacy Policy
lang: ja
---

# Hotaru プライバシーポリシー

最終更新日：2026年9月29日

[English](#hotaru-privacy-policy)

Hotaru（以下「本アプリ」）は、sea-edge（以下「開発者」）が提供する、端末の中で AI を動かすアプリです。本アプリでどのような情報が端末の外に送られるかを説明します。

## 1. 基本方針

- 会話、写真、音声、ドキュメント、生成した画像は、端末の中で処理・保存され、開発者のサーバーには送られません。
- アカウント登録は不要です。
- 広告は表示せず、広告のためのツール（SDK）も組み込んでいません。利用状況を分析するためのツールは、2.1 の ML Kit を除いて組み込んでいません。

## 2. 端末の外に送られる情報

以下の場合にだけ、情報が端末の外に送られます。

### 2.1 Gemini Nano を使うとき（Google の ML Kit）

対応端末で Gemini Nano を使うため、Google の ML Kit を組み込んでいます。ML Kit は、機能の診断と改善のために、次の情報を Google に送ります。

- 端末の情報（メーカー、機種、OS のバージョン）
- 本アプリの情報（パッケージ名、バージョン）
- インストールごとの識別子
- 性能の指標（処理にかかった時間など）、機能の設定、イベントの種類、エラーコード、設定された言語

**入力した文章・画像や、AI の回答は送られません。** 詳しくは [ML Kit のデータ開示](https://developers.google.com/ml-kit/android-data-disclosure) と [Google のプライバシーポリシー](https://policies.google.com/privacy) をご覧ください。

### 2.2 Web 検索をオンにしたとき

メッセージごとに「Web 検索」をオンにした場合にだけ、次の処理を行います。

- そのメッセージの本文を検索語として、Brave Search API または DuckDuckGo に送ります。
- 検索結果の上位のウェブページを読み込みます。このとき、各サイトには通常のウェブ閲覧と同じく、IP アドレスなどが伝わります。

送られた情報は、各サービスのプライバシーポリシーに従って扱われます（[Brave Search](https://search.brave.com/help/privacy-policy)、[DuckDuckGo](https://duckduckgo.com/privacy)）。

### 2.3 AI モデルを検索・ダウンロードするとき

AI モデルの検索とダウンロードのために、Hugging Face に接続します。検索した語句と、設定した場合は Hugging Face のアクセストークンが送られます。アクセストークンは端末内で暗号化して保存します。

### 2.4 不適切な出力を報告するとき

AI の回答や生成した画像を報告すると、報告の理由、コメント、対象の内容（回答の文章）、使ったモデル名、本アプリのバージョンが開発者に送られます。報告は、ユーザーが送信を選んだときにだけ送られます。

報告は、開発者が管理する Google スプレッドシートに（Google Apps Script を通して）保存し、不適切な出力を減らすためのフィルターの改善にだけ使います。受け取ってから 1 年後に削除します。

## 3. 端末内に保存される情報

会話の履歴、読み込んだドキュメントの検索用データ、生成した画像、ダウンロードした AI モデル、設定は、本アプリ専用の領域に保存されます。アプリ内で削除できるほか、本アプリをアンインストールするとすべて消えます。

## 4. 第三者への提供

2 章に書いたサービスへの送信と、報告の保存に使う Google のサービスを除き、開発者が情報を第三者に提供・販売することはありません。

## 5. 子どもの利用

本アプリは 13 歳未満の子どもを対象としていません。

## 6. 削除の依頼・お問い合わせ

開発者に送られた報告の削除や、このポリシーについてのお問い合わせは、次のメールアドレスまでご連絡ください。

kaihatsu.dev@gmail.com

## 7. 改定

このポリシーを変更する場合は、このページで告知します。

---

# Hotaru Privacy Policy

Last updated: September 29, 2026

Hotaru ("the app") is an app by sea-edge ("the developer") that runs AI on your device. This page explains what information leaves your device.

## 1. Our approach

- Your conversations, photos, voice, documents and generated images are processed and stored on your device. They are never sent to the developer's servers.
- No account is required.
- The app shows no ads and contains no advertising SDKs. Apart from ML Kit (section 2.1), it contains no analytics SDKs.

## 2. Information sent off the device

Information leaves the device only in the following cases.

### 2.1 When you use Gemini Nano (Google ML Kit)

The app uses Google ML Kit to run Gemini Nano on supported devices. For diagnostics and improvement, ML Kit sends Google:

- Device information (manufacturer, model, OS version)
- App information (package name, version)
- A per-installation identifier
- Performance metrics (such as latency), feature configuration, event types, error codes and configured languages

**Your prompts, images and the AI's answers are not sent.** See [ML Kit data disclosure](https://developers.google.com/ml-kit/android-data-disclosure) and the [Google Privacy Policy](https://policies.google.com/privacy).

### 2.2 When you turn on web search

Only for messages where you turn on "Web search", the app:

- Sends the text of that message as a search query to the Brave Search API or DuckDuckGo.
- Loads the top result pages. As with normal browsing, those sites receive your IP address and similar request information.

That information is handled under each service's privacy policy ([Brave Search](https://search.brave.com/help/privacy-policy), [DuckDuckGo](https://duckduckgo.com/privacy)).

### 2.3 When you search for or download AI models

The app connects to Hugging Face to search for and download models. Your search terms and, if you set one, your Hugging Face access token are sent. The token is stored encrypted on the device.

### 2.4 When you report an output

When you report an AI answer or generated image, the reason, your comment, the reported content (the answer text), the model name and the app version are sent to the developer — only when you choose to send the report.

Reports are stored in a Google Sheets spreadsheet managed by the developer (received through Google Apps Script), used only to improve content filtering, and deleted one year after they are received.

## 3. Information stored on the device

Chat history, document search indexes, generated images, downloaded models and settings are stored in the app's private storage. You can delete them in the app, and uninstalling the app removes everything.

## 4. Sharing with third parties

Apart from the services listed in section 2 and the Google services used to store reports, the developer does not share or sell your information.

## 5. Children

The app is not directed at children under 13.

## 6. Deletion requests and contact

To request deletion of a report you sent, or for questions about this policy, contact:

kaihatsu.dev@gmail.com

## 7. Changes

Changes to this policy will be announced on this page.
