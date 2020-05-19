---

copyright:
  years: 2019
lastupdated: "2019-10-22"

keywords: bug, problem, troubleshoot, troubleshooting, question

subcollection: ApplicationServeronCloud

---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:note:.deprecated}
{:troubleshoot: data-hd-content-type='troubleshoot'}

# Troubleshooting
{: #troubleshoot}

General problems with using {{site.data.keyword.appserver_short}} in {{site.data.keyword.cloud}} might include the inability to connect to your application or to see your environment. In many cases, you can recover from these problems by following a few easy steps.
{: shortdesc}
<!-- where the first xxx is the long name of your service and the following xxx are pulled from your popular troubleshooting topics -->

## Why can't I connect to my application?
{: #troubleshoot-connect}
{: troubleshoot}

I am unable to connect to my application.
{: tsSymptoms}

The inability to connect to an application can have several causes. The **How to fix it** section lists several ways to determine the cause of the problem.
{: tsCauses}

To determine the problem with the connection to the application, investigate the following potential issues:
{: tsResolve}
1. Ensure that your openVPN is connected and that you have no other VPN connected. Disconnect all other VPNs before you connect to OpenVPN.
2. Try to ping your virtual machine.
3. If you cannot ping your virtual machine, check whether there is a reported network issue in the {{site.data.keyword.cloud_notm}} region where the virtual machine is provisioned.
4. Log in to the virtual machine and check whether your application is running.
5. If your application depends on other components, such as a database, ensure that all prerequisites are running.
6. Check the health, CPU, and memory usage of the virtual machine with the `top` command. If the values are high, try restarting your application or virtual machine.


## Why can't I see a provisioned resource?
{: #troubleshoot-lease}
{: troubleshoot}

I do not see the resource that I provisioned.
{: tsSymptoms}

If you do not renew a trial account lease before the lease expires, your service resource is deleted.
{: tsCauses}

If your account is a trial account, you must renew the lease to keep your resource active. See [Trial account lease](/docs/ApplicationServeronCloud?topic=ApplicationServeronCloud-getting-started#triallease){: new_window} for details.
{: tsResolve}

## Why can't I see my environment?
{: #troubleshoot-env}
{: troubleshoot}

I am a Single Tenant customer and I am not able to see my environment.
{: tsSymptoms}

If you cannot [access your Single Tenant Environment](/docs/ApplicationServeronCloud?topic=ApplicationServeronCloud-singleTenantEnvironment#singleTenantEnvironment){: new_window}, you might need to specify or change a resource group name and ID.
{: tsCauses}

Similar to other {{site.data.keyword.cloud_notm}} services, {{site.data.keyword.appserver_short}} in {{site.data.keyword.cloud_notm}} supports [resource groups](/docs/resources?topic=resources-rgs){:new_window}. If access to your environment was granted with the organization name, then you must request access for your resource group:
{: tsResolve}
1. Rename your resource group to a meaningful name, instead of using the default name, `Default`.
2. Click the **WebSphere Application Server** tile.
3. [Open a support ticket](/docs/ApplicationServeronCloud?topic=ApplicationServeronCloud-reporting_issues#reporting_issues){: new_window} for **Application Services** from the {{site.data.keyword.cloud_notm}} console of your region and provide your organization name, which you used to provide access, and the resource group name.

  You can find your resource group names and IDs by running the following command from the [{{site.data.keyword.cloud_notm}} command-line interface](/docs/cli?topic=cloud-cli-install-ibmcloud-cli){: new_window}:

  ```
  ibmcloud resource groups
  ```
  {: .codeblock}  
