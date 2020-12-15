---

copyright:
  years: 2018, 2020
lastupdated: "2020-12-15"

keywords: migrate websphere, create service, profile, architecture, vm, virtual machine, provision, resource group, lease

subcollection: ApplicationServeronCloud

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}


# Getting started tutorial
{: #getting-started}

With {{site.data.keyword.appserver_full}}, you can set up a pre-configured WebSphere Application Server traditional or Liberty environment in minutes. This getting started tutorial guides you through provisioning a WebSphere Application Server environment on a virtual machine in just a few steps.
{: shortdesc}

## Before you begin
{: #prereqs}

If you want an environment with more dedicated virtual machine resources, such as a reserve contract or a Single Tenant Environment, contact IBM Sales before you create the service. Learn more about these options in [About](/docs/ApplicationServeronCloud?topic=ApplicationServeronCloud-about#about).

The following steps walk you through creating a new environment in {{site.data.keyword.appserver_full}}.

## Step 1: Create the service
{: #create}

1. Go to the [{{site.data.keyword.appserver_short}}](https://{DomainName}/catalog/services/websphere-application-server) page in the {{site.data.keyword.cloud_notm}} catalog.
1. Log in with your IBMid, or sign up for an {{site.data.keyword.cloud_notm}} account.
1. On the catalog page, review the selections for the service configuration.

  For pay-as-you-go environments, use the default selections or modify them to suit your needs.

  If you have a reserve contract or Single Tenant Environment, pay careful attention to the following options.

  * **Reserve contract:** Under **Choose a region/location to deploy in**, verify that the selected region is the correct region for your contract.

  * **Single Tenant Environment:** Under **Choose a region/location to deploy in**, verify that the selected region is the region where your Single Tenant Environment is deployed. Under **Environment**, select your Single Tenant Environment. By default, the public environment might be shown.

    If your Single Tenant Environment is not listed, check that you're in the correct region and that your resource group has access to your Single Tenant Environment.
    {: tip}
1. Select the pricing plan for the edition of {{site.data.keyword.appserver_short}} that you want to deploy.
1. Click **Create**.


## Step 2: Choose your environment (Network Deployment only)
{: #choose_env}

{{site.data.keyword.appserver_short}} Base and Liberty Core plans have only single servers, so if you chose these plans, you can skip this step.

For the Network Deployment plan, choose the profile and architecture for your environment.

* **Profile:** Choose {{site.data.keyword.appserver_short}} traditional or Liberty
* **Architecture:** Choose a single-server environment or a clustered environment with traditional cells or Liberty collectives


## Step 3: Size your virtual machines
{: #vm_sizing}

You can individually size the virtual machine for each component in your environment. Virtual machines are chunked in [T-shirt sizes](/docs/ApplicationServeronCloud?topic=ApplicationServeronCloud-about#vm-size) of blocks of resources.

Click the tab for the component, such as the server, deployment manager, or application node, and select the T-shirt size for its virtual machine.

## Step 4: Provision your environment
{: #service_profile}

Review the details in the service configuration summary, including the estimated time that it takes to provision.

**Reserve contract:** Make sure that the **Billing** option is set to _Reserve Contract_. If you don't see the option, verify that [your resource group](/docs/account?topic=account-rgs){:new_window} is exactly the same, including case and blank space, as the resource group name for your contract. Also verify that you are in the correct account for the specified resource group name, because resource group names are not required to be unique. If you provision the service without selecting reserve contract billing, pay-as-you-go billing is used.

Click **Provision** to set up your {{site.data.keyword.appserver_short}} environment.

## Next steps
{: #anchor_value}

Learn about how to access and manage your new {{site.data.keyword.appserver_short}} environment in [System access](/docs/ApplicationServeronCloud?topic=ApplicationServeronCloud-system_access) and [Network environment](/docs/ApplicationServeronCloud?topic=ApplicationServeronCloud-networkEnvironment).


### Trial account lease
{: #triallease}

If you have a trial account, your WebSphere Application Server service resource has a lease. The UI shows when the lease was created, expires, and can be renewed. Initial leases last 14 days and can be renewed for 30 days at a time. To renew a lease, click **RENEW** in the UI for the service resource after the **Lease Renewal Available** date and time and before lease expiration.

**Important**: If you do not renew before the lease expires, your service resource is deleted.

In the REST API output, resources have a non-null `expireTime` field if the subscription has a lease. You cannot renew your lease by using the REST API; you must use the UI.

If your account changes to a non-trial (or paid) account, the lease is removed from your service resource and is no longer shown in the UI. If a lease is still shown in the UI after the change to a non-trial account, [contact IBM](/docs/ApplicationServeronCloud?topic=ApplicationServeronCloud-reporting_issues) to ensure that your account is updated before the lease expires.
