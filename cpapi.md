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

You can use the API to interact with your account, products, and services by using direct API calls instead of using the customer portal.
{:shortdesc}

The goal of the API is to provide a method of programatically interacting with SoftLayer. Any action that can be performed in the control portal can be performed via the API as the customer portal itself uses the SoftLayer API to perform its actions. The API is maintained with frequent additions and updates to ensure that you have the best options available. This includes the ability to program in various languages and options to use SOAP, XML-RPC and REST-based APIs. Similar to working in the customer portal, if you primarily make account interactions in the API, you need a viable source for support as well.

The [SoftLayer Development Network (SLDN) ![External link icon](../icons/launch-glyph.svg)](http://sldn.softlayer.com/){:new_window} is dedicated to supporting you when interacting with your account, products, and services by using the API. The [SLDN ![External link icon](../icons/launch-glyph.svg)](http://sldn.softlayer.com/){:new_window} contains documentation on SoftLayer APIs, supported programming languages, available API calls, and more. The SLDN is the resource to use for information on various API features, a complete list of API calls, and various blog posts to give you ideas on how to best use the API.

If you are unsure how a specific service works, or would like an example created to solve a generic problem, feel free to open an issue on our [SLDN github ![External link icon](../icons/launch-glyph.svg)]](https://github.com/softlayer/softlayer.github.io){:new_window}. If you encounter any unexpected errors or incorrect data being returned from the API, a support ticket should be opened about the issue instead.

## Accessing the API 
{: #cp_getapikey}

You can access the API with a user-specific API key. API keys are unique, alpha-numeric identifiers that allow you to securely access the API. Your API key is linked specifically to your user ID and it provides the same permissions in the API that you have in the Customer Portal. You generate the API key once and then you can retrieve it and continue to use it. Use the following steps to generate your API key:

1. Access the customer portal by using your unique credentials.
2. Select **Account** > **Users** from the navigation bar.
3. Under the **API KEY** column of the row with the user credentials, click the **Generate** link.

After the API key is generated, the **Generate** link changes to a **View** link that you can use to access your API key at any time.
