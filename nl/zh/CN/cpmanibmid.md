---

copyright:

  years: 1994, 2019

lastupdated: "2019-05-03"

keywords: IBMid accounts, softLayer account, IBM Cloud infrastructure authentication

subcollection: customer-portal
---

{:shortdesc: .shortdesc}
{:screen: .screen}
{:tip: .tip}
{:codeblock: .codeblock}
{:pre: .pre}
{:new_window: target="_blank"}

# 将 IBM 标识帐户用于 {{site.data.keyword.BluSoftlayer_notm}} 基础架构
{: #customerportal_ibmid}

现在，{{site.data.keyword.BluSoftlayer_notm}} 基础架构中的认证使用 IBM 标识来提供对{{site.data.keyword.Bluemix_notm}} 的单点登录。
{:shortdesc}

如果您已有 SoftLayer 帐户，那么可以切换到 IBM 标识。迁移向导有助于指导您完成此切换。有关更多信息，请参阅[切换到 IBM 标识](/docs/account?topic=account-unifyingaccounts#switchtoIBMid)。

## 将多个 SoftLayer 帐户映射到一个 IBM 标识
{: #cp_mapmultclinfrto1ibmid}

在设置帐户时，通过使用现有的 IBM 标识电子邮件地址，可以将一个 IBM 标识与多个 SoftLayer 帐户关联。每个帐户只有一个 {{site.data.keyword.BluSoftlayer_notm}} 基础架构用户可以映射到这个 IBM 标识。该 IBM 标识在每个 SoftLayer 帐户中必须唯一。但是，有权访问多个 SoftLayer 帐户的用户可以使用一个 IBM 标识来访问多个 SoftLayer 帐户。

例如，一个 IBM 标识可以映射到帐户 A 和 B 中的主用户，并映射到帐户 C 和 D 中的另一个用户。映射到该 IBM 标识的其中一个帐户是缺省帐户。通常，缺省帐户是最先映射到该 IBM 标识的帐户。您可以通过客户门户网站中的帐户切换功能来切换作为缺省帐户的帐户。

![多个 SoftLayer 帐户映射到一个 IBM 标识](images/ibmid-image.png)

如果某用户可以使用 IBM 标识访问多个帐户并启用了双因子认证，那么需要有双因子认证验证码。在帐户登录期间和切换缺省帐户时，每个帐户都需要该验证码。
