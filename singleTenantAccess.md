---

copyright:
  years: 2017, 2018
lastupdated: "2018-06-08"

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

1. In your browser, go to the [{{site.data.keyword.cloud_notm}} catalog](https://console.bluemix.net/catalog/){: new_window}.

2. Click **Log in**, and log in with your IBMid.

6. In the Catalog search filter, enter **WebSphere Application Server**.

    ![alt text](images/filter.png "Search Filter")

7. Under **Application Services**, click the **WebSphere Application Server** tile.

    ![alt text](images/iconWAS.png "WebSphere Application Server tile")

8. In the **Environment** menu, select your Single Tenant Environment.

    ![alt text](images/environmentSTE.png "Single Tenant Environment name")

    **Avoid trouble:** The public environment might be shown as the default. Displaying the correct environment name assumes that you are logged in to the correct region, and a member of an organization that is allowed to access your Single Tenant Environment.

    **Note:** If you select one of the public environments, you might incur an hourly charge. Therefore, if you do not see your Single Tenant Environment name, then open a Support Ticket as defined on the [Getting Customer Support](https://console.bluemix.net/docs/support/index.html#contacting-support){: new_window} page.

9. Select the appropriate plan, and click **Create**.

    ![alt text](images/createSTE.png "Choose a plan and create your service")


**Note:** Hourly pricing does not apply for Single Tenant environments. A Single Tenant environment includes a fixed number of **blocks** that are called a quota. A small environment contains 64 blocks. A medium contains 128 blocks, and a large contains 256 blocks.

A **block** is defined as follows:
  * 1 vCPU
  * 12.5 GB disk[1]
  * 2 GB RAM

[1] *Technically, a small system contains only 12 GB of disk. A medium system contains 25 GB of disk, and a large contains 50 GB, and so on.*

For each virtual machine you create, specify the T-shirt size you desire: S, M, L, XL, or XXL, which corresponds to 1, 2, 4, 8, and 16 blocks. When you select a T-shirt size, the corresponding number of blocks is decremented from your quota.

For example, suppose that you have a small environment, which contains 64 blocks. Within this environment, you configured service instances that contain two XXLs, three XLs, and 1 L for a total of 60 used blocks. If you select a Medium T-shirt size for a new Liberty Core subscription, a message might be displayed that states your quota and the number of blocks still available:

> **Your Single-Tenant memory quota for this service is 64 blocks. Including your current configuration, you have 2 blocks remaining. To increase your memory quota, contact IBM Sales.**


## Private Network Environment
{: #private_network}

After your WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: Single Tenant Environment is provisioned, you can download your VPN credentials and establish an OpenVPN connection. For more information, see the following links:

* [VPN Access](https://console.bluemix.net/docs/services/ApplicationServeronCloud/networkEnvironment.html#vpnAccess){: new_window}
* [Setting up OpenVPN](https://console.bluemix.net/docs/services/ApplicationServeronCloud/systemAccess.html#setup_openvpn){: new_window}

## Managing your Single Tenant Environment
{: #manageSTE}

To add extra capacity to your existing WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}: Single Tenant Environment or to order capacity in another datacenter, contact your Americas Call Centers, local IBM representative, or your IBM Business Partner. To identify your representative or partner call 800-426-4968. For more information, contact the Americas Call Centers. Phone: 800-IBM-CALL (426-2255) Fax: 800-2IBM-FAX (242-6329).


## Supporting your Single Tenant Environment
{: #supportingSTE}

If you experience issues, you can receive assistance by opening a Support Ticket as defined on the [Getting Customer Support](https://console.bluemix.net/docs/support/index.html#contacting-support){: new_window} page.
