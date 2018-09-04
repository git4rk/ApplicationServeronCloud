---

copyright:
  years: 2018
lastupdated: "2018-09-04"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}


# Getting started tutorial
{:#getting-started}

With {{site.data.keyword.appserver_full}}, you can set up a pre-configured WebSphere Application Server traditional or Liberty environment in minutes. This getting started tutorial guides you through provisioning a WebSphere Application Server environment on a virtual machine in just a few steps.
{: shortdesc}

## Before you begin
{: #prereqs}

If you want an environment with more dedicated virtual machine resources, such as a reserve contract or a Single Tenant Environment, you'll need to contact IBM Sales before you create the service. Learn more about these options in [About](index.html).

## Step 1: Create the service
{: #create}

1. Go to the [{{site.data.keyword.appserver_short}}](https://console.bluemix.net/catalog/services/websphere-application-server) page in the {{site.data.keyword.cloud_notm}} Catalog.
1. Log in with your IBMid, or sign up for an {{site.data.keyword.cloud_notm}} account.
1. On the catalog page, review the selections for the service configuration.

  For pay-as-you-go environments, use the default selections or modify them to suit your needs.

  If you have a reserve contract or Single Tenant Environment, pay careful attention to the following options.

  * **Reserve contract:** Under **Choose a region/location to deploy in**, verify that the selected region is the correct region for your contract.

  * **Single Tenant Environment:** Under **Choose a region/location to deploy in**, verify that the selected region is the region where your Single Tenant Environment is deployed. Under **Environment**, select your Single Tenant Environment. By default, the public environment might be shown.

    If you don't see your Single Tenant Environment listed, check that you're in the correct region and that your organization has access to your Single Tenant Environment.
    {: tip}
1. Select the pricing plan for the edition of {{site.data.keyword.appserver_short}} that you want to deploy.
1. Click **Create**.


## Step 2: Choose your environment (Network Deployment only)
{: #choose_env}

{{site.data.keyword.appserver_short}} Base and Liberty Core plans only have single servers, so if you chose these plans, you can skip this step.

For the Network Deployment plan, choose the profile and architecture for your environment.

* **Profile:** Choose {{site.data.keyword.appserver_short}} traditional or Liberty
* **Architecture:** Choose a single-server environment or a clustered environment with traditional cells or Liberty collectives


## Step 3: Size your virtual machines
{: #vm_sizing}

You can individually size the virtual machine for each component in your environment. Virtual machine sizing is chunked in [T-shirt sizes](index.html#vm-size) of blocks of resources.

Click the tab for the component, such as the server, deployment manager, or application node, and select the T-shirt size for its virtual machine.

## Step 4: Provision your environment
{: #service_profile}

Review the details in the service configuration summary, including the estimated time that it will take to provision.

**Reserve contract:** Make sure the **Billing** option is set to _Reserve Contract_. If you don't see the option, verify that [your org](../../account/orgs_spaces.html){:new_window} is exactly the same, including case and whitespace, as the org name for your contract. If you provision the service without selecting reserve contract billing, pay-as-you-go billing is used.

Click **Provision** to set up your {{site.data.keyword.appserver_short}} environment.

## Next steps
{: #anchor_value}

Learn about how to access and manage your new {{site.data.keyword.appserver_short}} environment in [System access](systemAccess.html).
