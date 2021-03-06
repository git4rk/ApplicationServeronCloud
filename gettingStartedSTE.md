---

copyright:
  years: 2017, 2020
lastupdated: "2020-06-15"

keywords: single tenant, websphere, sales, order, resource group

subcollection: ApplicationServeronCloud

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Single Tenant Environments
{: #getting_startedSTE}

The {{site.data.keyword.appserver_full}} Single Tenant Environment provides customers with an isolated WebSphere workload, a fully integrated hybrid environment, and secure data. This getting started guide is designed to identify key elements that assist you in accessing and managing your Single Tenant Environment.
{: shortdesc}

## Ordering a Single Tenant Environment
{:#ordering}

Single Tenant Environments cannot be created through the {{site.data.keyword.Bluemix_notm}} catalog and must be ordered by contacting IBM sales. When you order your environment, you can choose from a standard or bring-your-own-license Single Tenant Environment. Standard Single Tenant Environments include all required infrastructure and WebSphere Application Server licenses. In bring-your-own-license Single Tenant Environments, you can use separate WebSphere Application Server licenses.

To order a Single Tenant Environment, [contact IBM Sales](/docs/ApplicationServeronCloud?topic=ApplicationServeronCloud-reporting_issues#contacting-sales). The sales team can assist you in setting up an environment that is tailored to your needs.

## Overview of WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Single Tenant Environment
{: #overviewSTE}

The Single Tenant Environment provides your own private instance of the service, private networking, and isolated resources. Although the offering is managed independently, the service and created service instance dashboards are accessible through a specific {{site.data.keyword.Bluemix_notm}} public region as indicated in the following figure.

Figure 1. Architecture of the WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Single Tenant Environment

![Figure 1. Architecture of Single Tenant Environment](images/WASaaS.png)


## Resource Group Management
{: #organization_management}

The WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Single Tenant Environment is configured according to your order. If you provided one or more {{site.data.keyword.Bluemix_notm}} resource group names and IDs as part of the order, you can start accessing your environment now. If you did not provide a resource group name and ID or if you want to change this setting, open a [support ticket](/docs/ApplicationServeronCloud?topic=ApplicationServeronCloud-reporting_issues#reporting_issues) for **Application Services** from the {{site.data.keyword.Bluemix_notm}} console of your region. You can find your resource group names and IDs by running the following command from the [{{site.data.keyword.Bluemix_notm}} command-line interface](/docs/cli?topic=cli-install-ibmcloud-cli){: new_window}:

```
ibmcloud resource groups
```
{: .codeblock}  

**Note:** To access your Single Tenant Environment, see [Single Tenant Environment access](/docs/ApplicationServeronCloud?topic=ApplicationServeronCloud-singleTenantEnvironment#singleTenantEnvironment).
