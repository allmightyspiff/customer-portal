---

copyright:

  years: 1994, 2019

lastupdated: "2019-06-28"

keywords: SoftLayer API, development environment, direct API calls, access API, 

subcollection: customer-portal

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}


# SoftLayer API
{: #customerportal_api}

この API を使用すると、カスタマー・ポータルを使用する代わりに開発環境で直接 API 呼び出しを使用することによって、アカウント、製品、およびサービスと対話することができます。
{:shortdesc}

この API の目標は、カスタマー・ポータルのすべての作業を API で実行できる環境を提供することです。 最良のオプションが確実に使用可能になるよう、API 環境は頻繁な追加と更新によって保守されます。 これには、さまざまな言語でプログラムを作成する機能や、SOAP ベース、XML-RPC ベース、および REST ベースの API を使用するオプションが含まれます。 カスタマー・ポータルでの作業と同様に、API で主にアカウント対話を行う場合にもサポートのための存続可能なソースが必要です。

[SoftLayer Development Network (SLDN) ![外部リンク・アイコン](../icons/launch-glyph.svg)](http://sldn.softlayer.com/){:new_window} は、API を使用してアカウント、製品、およびサービスと対話するユーザーのサポートを専門としています。 [SLDN ![外部リンク・アイコン](../icons/launch-glyph.svg)](http://sldn.softlayer.com/){:new_window} には、SoftLayer API、サポートされるプログラミング言語、使用可能な API 呼び出しなどに関する資料が含まれています。 SLDN は、さまざまな API 機能に関する情報、API 呼び出しの完全なリスト、および、API の最良の使用方法についてのヒントを得られるさまざまなブログ投稿を参照するために使用できるリソースです。

API についての質問がある場合、カスタマー・フォーラムに投稿するか、記事への直接のフィードバックとして投稿できます。

## API へのアクセス 
{: #cp_getapikey}

API には、ユーザー固有の API キーを使用してアクセスできます。 API キーは、ユーザーが安全に API にアクセスできるようにするための固有の英数字の識別子です。 API キーは、ユーザー ID に明確にリンクしており、カスタマー・ポータルで所有するのと同じアクセス権を API で提供します。 API キーを生成するのは 1 回で、その後は、それを取り出し、継続して使用できます。 API キーを生成するには、以下の手順を使用します。

1. 固有の資格情報を使用してカスタマー・ポータルにアクセスします。
2. ナビゲーション・バーから**「アカウント」** > **「ユーザー」**を選択します。
3. ユーザー資格情報を含む行の**「API キー」**列の下で、**「生成」**リンクをクリックします。

API キーが生成されると**「生成」**リンクは**「表示」**リンクに変わり、このリンクを使用して、いつでも API にアクセスすることができます。
