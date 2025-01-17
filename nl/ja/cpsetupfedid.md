---

copyright:

  years: 1994, 2019

lastupdated: "2019-06-18"

keywords: service provider, identity federation, IBM Cloud infrastructure SSO

subcollection: customer-portal 

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}

# ID 連携のセットアップ
{: #cp_setupidfed}

{{site.data.keyword.BluSoftlayer_full}} Infrastructure Management System (IMS) などのサービス・プロバイダーが、信頼できる ID システムから生成されたセキュリティー・トークンを認証および許可の目的のために取り込むことができるようにするため、ID 連携をセットアップできます。
{:shortdesc}

以下のいずれかの方法で、{{site.data.keyword.BluSoftlayer_notm}} インフラストラクチャー SSO で ID 連携をセットアップできます。
* ID プロバイダーおよび {{site.data.keyword.BluSoftlayer_notm}} インフラストラクチャー内にユーザーを作成する
* ID プロバイダー内にユーザーを作成する

役割は、サービス・プロバイダーに対して、ユーザーが認証後にユーザーのシステムにおいて (許可を通して) 何を行う権限があるのかを定義するものです。 例えば、*User* 役割は、さまざまな画面を表示することのみ許可され、更新や追加は許可されないといった例が考えられます。

1 つの役割に複数のユーザーを割り当てることができます。 また、役割が ID プロバイダー内に存在しているが、{{site.data.keyword.BluSoftlayer}} インフラストラクチャー内にはない場合、ユーザーはそれでも {{site.data.keyword.BluSoftlayer}} インフラストラクチャーにログインすることはできますが、ユーザーは役割に割り当てられた許可は保有しません。
{: tip}


## ID プロバイダーおよび {{site.data.keyword.BluSoftlayer_notm}} インフラストラクチャー内にユーザーを作成する
{: #cp_scenario1both}

このモデルでは、以下のプロセスが行われます。
* ID プロバイダーと {{site.data.keyword.BluSoftlayer_notm}} インフラストラクチャーの両方にユーザーが作成されます。
* {{site.data.keyword.BluSoftlayer}} インフラストラクチャーのカスタマー・ポータルまたは API を使用して、{{site.data.keyword.BluSoftlayer}} インフラストラクチャー IMS においてユーザー許可が割り当てられます。
* ユーザーは ID プロバイダーを使用して認証され、ユーザー ID が統合されます。
* {{site.data.keyword.BluSoftlayer}} インフラストラクチャーはそのユーザー ID を取り込み、アクセス制御は {{site.data.keyword.BluSoftlayer}} インフラストラクチャー IMS 内でユーザーに定義された許可に基づきます。

{{site.data.keyword.BluSoftlayer}} インフラストラクチャーへのアクセスを必要とするユーザーのアカウントは、まず最初に、ランダム・パスワードと共に {{site.data.keyword.BluSoftlayer}} インフラストラクチャー内に作成されます。 ユーザーが ID プロバイダーを介して SSO を使用できるためには、その前に {{site.data.keyword.BluSoftlayer}} インフラストラクチャー内ですべての許可が構成される必要があります。 現在、許可は個々のユーザーに基づいてセットアップされます。

### ユーザーのセットアップ
{: #cp_user-setup}

ユーザーをセットアップするには、以下の手順を使用します。

1. [SoftLayer アカウントにユーザーを追加します。](/docs/customer-portal?topic=customer-portal-customerportal_addusertocpacct#customerportal_addusertocpacct)
2. {{site.data.keyword.BluSoftlayer}} インフラストラクチャー内で許可を割り当てます。
3. ID プロバイダー内でユーザーを作成します。

個々のユーザー・プロファイル内の **E メール**または**ユーザ名**フィールドが、Security Assertion Markup Language&trade; (SAML&trade;) 2.0 トークン用に使用されます。 このトークンは、ID プロバイダーと {{site.data.keyword.BluSoftlayer}} インフラストラクチャーとの間でユーザーをマップします。

### ログイン認証のフローの例
{: #exlogauthflowidprovicloud}

以下のフロー例は、ID プロバイダーおよび {{site.data.keyword.BluSoftlayer_notm}} インフラストラクチャー内にユーザーを作成した場合にユーザーのログイン認証がどのように行われるのかを示します。
1. ユーザーは、ブラウザー・セッションから ID プロバイダー URL にアクセスします。
2. ID プロバイダーは、例えば LDAP を介して、ユーザーを認証します。
3. ID プロバイダーは、SAML 2.0 応答を返します。
4. ID プロバイダーは、ユーザー ID を認証するために、サービス・プロバイダー (この場合は {{site.data.keyword.BluSoftlayer}} インフラストラクチャー) に SAML 2.0 トークンを送信します。
5. {{site.data.keyword.BluSoftlayer}} インフラストラクチャーは、SAML 2.0 応答を検証します。
6. ID プロバイダーと {{site.data.keyword.BluSoftlayer}} インフラストラクチャーとの間の信頼できるセットアップに基づいて、ユーザーは {{site.data.keyword.BluSoftlayer}} インフラストラクチャーのカスタマー・ポータルにログインされます。


## ID プロバイダー内にユーザーを作成する
{: #cp_scenario2idp}

このモデルでは、以下のようになります。
* ID プロバイダー内で役割が作成され、ユーザーに割り当てられます。
* {{site.data.keyword.BluSoftlayer}} インフラストラクチャー API を使用して {{site.data.keyword.BluSoftlayer}} インフラストラクチャー IMS 内で役割および許可の割り当てがセットアップされます。
* ユーザーは ID プロバイダーを使用して認証され、ユーザー ID と役割の属性が統合されます。
* {{site.data.keyword.BluSoftlayer}} インフラストラクチャーは、ユーザー ID と役割の属性を検証します。ID プロバイダーによってユーザーに割り当てられた役割が、{{site.data.keyword.BluSoftlayer}} インフラストラクチャーにおける役割と一致している場合、ユーザーには、{{site.data.keyword.BluSoftlayer}} インフラストラクチャーにログインするときに、それらの役割の許可が付与されます。
* ID プロバイダーがユーザーを作成する場合、それらのユーザーは統合していると見なされます。これは、それらのユーザーおよびユーザーの役割が SAML 2.0 を介して認証されるためです。

### ユーザーの役割のセットアップ
{: #cp_set-up-user-role}

ユーザーの役割をセットアップするには、以下の手順を使用します。

1. {{site.data.keyword.BluSoftlayer}} インフラストラクチャー API を通して役割をセットアップします。
2. ID プロバイダー内で役割をセットアップします。
3. {{site.data.keyword.BluSoftlayer}} インフラストラクチャーおよび ID プロバイダー内に定義される役割が同じ名前であることを確認してください。

### ユーザーのセットアップ
{: #identity-setupuser}

ユーザーをセットアップするには、以下の手順を使用します。

1. ID プロバイダー内でユーザーをセットアップします。
2. ID プロバイダー内でユーザーに役割を割り当てます。

このシナリオでは、{{site.data.keyword.BluSoftlayer}} インフラストラクチャー内で手動でユーザーを作成する必要はありません。

### ユーザー・ログイン認証のフローの例
{: #exlogauthflowidprov}

以下のフロー例は、ID プロバイダー内にユーザーを作成した場合にユーザーのログイン認証がどのように行われるのかを示します。
1. ユーザーは、ブラウザー・セッションから ID プロバイダー URL にアクセスします。
2. ID プロバイダーは、例えば LDAP を介して、ユーザーを認証します。
3. ID プロバイダーは、SAML 2.0 応答を返します。
4. ID プロバイダーは、ユーザー役割を認証するために、サービス・プロバイダー (この場合は {{site.data.keyword.BluSoftlayer}} インフラストラクチャー) に SAML 2.0 トークンを送信します。
5. {{site.data.keyword.BluSoftlayer}} インフラストラクチャーは、SAML 2.0 応答を検証します。
6. {{site.data.keyword.BluSoftlayer}} インフラストラクチャーは、ユーザーをカスタマー・ポータルにリダイレクトします。
7. ユーザーは {{site.data.keyword.BluSoftlayer}} インフラストラクチャーのカスタマー・ポータルにログインされます。

新規役割をセットアップして、それらを {{site.data.keyword.BluSoftlayer}} インフラストラクチャーと関連付けるための、ID プロバイダーの手順をレビューしてください。
