---

copyright:
  years: 2017, 2019
lastupdated: "2019-10-22"

keywords: single tenant, access, catalog, create service, block, pricing, vpn, openvpn

subcollection: ApplicationServeronCloud

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Single Tenant Environment access
{: #singleTenantEnvironment}


The following steps discuss accessing your Single Tenant Environment, along with methods of creating a service instance.
{: shortdesc}


## Accessing your Single Tenant Environment
{: #accessSTE}

1. In your browser, go to the [{{site.data.keyword.cloud_notm}} catalog](https://{DomainName}/catalog/){: new_window}.

2. Click **Log in**, and log in with your IBMid.

6. In the catalog search filter, enter **WebSphere Application Server**.

    ![Search filter](images/filter.png)

7. Under **Application Services**, click the **WebSphere Application Server** tile.

    ![WebSphere Application Server tile](images/iconWAS.png)

8. In the **Environment** menu, select your Single Tenant Environment.

    ![Single Tenant Environment name](images/environmentSTE.png)

    **Avoid trouble:** The public environment might be shown as the default. Displaying the correct environment name assumes that you are logged in to the correct region, and have appropriate access to a resource group that is allowed to access your Single Tenant Environment.

    **Note:** If you select one of the public environments, you might incur an hourly charge. Therefore, if you do not see your Single Tenant Environment name, then open a Support Ticket as described in [Getting help](/docs/ApplicationServeronCloud?topic=ApplicationServeronCloud-reporting_issues#reporting_issues){: new_window} page.

9. Select the appropriate plan, and click **Create**.

    ![Choose a plan and create your service](images/createSTE.png)


**Note:** Hourly pricing does not apply for Single Tenant environments. A Single Tenant environment includes a fixed number of **blocks** that are called a quota. A small environment contains 64 blocks. A medium contains 128 blocks, and a large contains 256 blocks.

A **block** is defined as follows.
  * 1 vCPU
  * 25 GB disk
  * 2 GB RAM

For each virtual machine you create, specify the T-shirt size you desire: S, M, L, XL, or XXL, which corresponds to 1, 2, 4, 8, and 16 blocks. When you select a T-shirt size, the corresponding number of blocks is decremented from your quota.

For example, suppose that you have a small environment, which contains 64 blocks. Within this environment, you configured service instances that contain two XXLs, three XLs, and 1 L for a total of 60 used blocks. If you select a Medium T-shirt size for a new Liberty Core subscription, a message might be displayed that states your quota and the number of blocks still available:

> **Your Single-Tenant memory quota for this service is 64 blocks. Including your current configuration, you have 2 blocks remaining. To increase your memory quota, contact IBM Sales.**


## Private Network Environment
{: #private_network}

After your Single Tenant Environment is provisioned, you can download your VPN credentials and establish an OpenVPN connection. For more information, see the following links:

* [VPN Access](/docs/ApplicationServeronCloud?topic=ApplicationServeronCloud-networkEnvironment#vpnAccess){: new_window}
* [Setting up OpenVPN](/docs/ApplicationServeronCloud?topic=ApplicationServeronCloud-system_access#setup_openvpn){: new_window}

## Managing your Single Tenant Environment
{: #manageSTE}

To add extra capacity to your existing Single Tenant Environment or to order capacity in another datacenter, contact your Americas Call Centers, local IBM representative, or your IBM Business Partner. See [Contacting sales](/docs/ApplicationServeronCloud?topic=ApplicationServeronCloud-reporting_issues#contacting-sales) for details.
