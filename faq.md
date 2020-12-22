---

copyright:
  years: 2019, 2020
lastupdated: "2020-12-08"

keywords: bug, problem, faqs, Frequently Asked Questions, question

subcollection: ApplicationServeronCloud

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:note: .note}
{:external: target="_blank" .external}
{:codeblock: .codeblock}
{:tip: .tip}
{:faq: data-hd-content-type='faq'}

# FAQs
{: #wasaas-faqs}

Review frequently asked questions for {{site.data.keyword.appserver_short}} for {{site.data.keyword.cloud}}. To find all FAQs for {{site.data.keyword.cloud_notm}}, see the [FAQ library](/docs/faqs){: new_window}.
{: shortdesc}

## What are the deprecation details for {{site.data.keyword.appserver_short}} in {{site.data.keyword.cloud_notm}}?
{: #faq-deprecation}
{: faq}

{{site.data.keyword.appserver_short}} in {{site.data.keyword.cloud_notm}} service is deprecated. You can use [IBM WebSphere Application Server for VSI](https://cloud.ibm.com/catalog/content/.-b9f20fe3-baac-459b-b047-cb4ae9eb46f2-global){: external} offering to migrate your existing WebSphere applications to a new Virtual Service Instance (VSI) on IBM Cloud. See "Migration Options" section below for more details.

### Important Dates 

### End of Marketing : January 15, 2021
As of January 15, 2021, new WebSphere Application Server instances will not be provisioned. However, existing instances will continue to be supported until the End of Service date.


### End of Service : March 31, 2021 
Any instance still active as of the End of Service date **will be deleted**. Please migrate your applications and delete WebSphere Application Server instances before the End of Service date.


### Migration Options 
There are other options to leverage WebSphere Application Server on IBM Cloud and we are committed to help. We encourage you to explore and use our recently announced [IBM WebSphere Application Server for VSI](https://cloud.ibm.com/catalog/content/.-b9f20fe3-baac-459b-b047-cb4ae9eb46f2-global){: external} in IBM Cloud, which allows you to quickly install and configure your licensed WebSphere Application Server or Liberty on your VSI (Virtual Server Instance) in IBM Cloud VPC (Virtual Private Cloud). Please refer to the [migration FAQ](#faq-migrate-to-vsi) for more details.

### Special Offer for You
We recognize migrating your resources can be complex and time consuming, so IBM Cloud is offering a credit of up to USD 2000. Use Code "VPC500" to get USD 500 off when creating your new virtual servers for VPC. Contact IBM Sales team and ask about the special offer for the additional USD 1500. Please refer to [VPC pricing](https://www.ibm.com/cloud/vpc/pricing){: external} for more details.


## How do I migrate from {{site.data.keyword.appserver_short}} in {{site.data.keyword.cloud_notm}}?
{: #faq-migrate-to-vsi}
{: faq}

You can migrate from {{site.data.keyword.appserver_short}} for {{site.data.keyword.cloud_notm}} to {{site.data.keyword.was4vsi_notm}}.

1. Obtain a [{{site.data.keyword.appserver_short}}](https://www.ibm.com/cloud/websphere-application-server){: external} license, if you do not have one.
2. Gather details about the number and size of the {{site.data.keyword.appserver_short}} for {{site.data.keyword.cloud_notm}} VMs. You can use this information when you create virtual server instances (VSIs) in {{site.data.keyword.cloud_notm}}.
3. Follow the [Deploying {{site.data.keyword.was4vsi_notm}} tutorial](/docs/was-for-vsi?topic=was-for-vsi-getting-started).
   1. Review the prerequisites.
   2. Set up a Virtual Private Cloud (VPC) and VSIs in {{site.data.keyword.cloud_notm}}. You are charged for the VSIs.
   3. Install a WebSphere product. You are not charged for the product installation.
4. Deploy your application on the new installation. You can use [IBM {{site.data.keyword.appserver_short}} Migration Tool](https://www.ibm.com/support/pages/websphere-application-server-migration-toolkit){: external} to deploy your application on the new installation.

    You also can use [{{site.data.keyword.cloud_notm}} Transformation Advisor](https://www.ibm.com/support/knowledgecenter/SS5Q6W){: external} to modernize your application and move it to the target environment.
    {: tip}
5. Test your deployed application.
6. Delete your {{site.data.keyword.appserver_short}} for {{site.data.keyword.cloud_notm}} subscription.


## What is the difference between the old infrastructure and the upgraded infrastructure?
{: #faq-old-or-updated}
{: faq}

The upgraded infrastructure differs from the old infrastructure in two ways:

### Twice the disk size

The upgraded infrastructure has the same CPU and memory for a block size but the disk size doubled.

|T-Shirt Size| Blocks | Old Infrastructure HD (GB) | Upgraded Infrastructure HD (GB)|
|:-------:|:------:|:--------:|:--------:|
|S|1|12|25|
|M|2|25|50|
|L|4|50|100|
|XL|8|100|200|
|XXL|16|200|400|
{: caption="Table 1. Disk size per T-shirt" caption-side="top"}


For information about T-shirt and block sizing, see [Virtual machine sizing](/docs/ApplicationServeronCloud?topic=ApplicationServeronCloud-about#vm-size){: new_window}.

### Different network connectivity

The upgraded infrastructure is set up on a different network than old infrastructure and requires you to set up separate OpenVPN connectivity. You cannot access virtual machines on both the old and the upgraded infrastructure with the same OpenVPN connectivity.

For more information, see [VPN access](/docs/ApplicationServeronCloud?topic=ApplicationServeronCloud-networkEnvironment#vpnAccess){: new_window} and [Setting up OpenVPN](/docs/ApplicationServeronCloud?topic=ApplicationServeronCloud-system_access#setup_openvpn){: new_window}.

## How do I know whether my virtual machine is on old infrastructure or upgraded infrastructure?
{: #faq-check-machine}
{: faq}

Check the disk size of your virtual machine and refer to the [Disk size per T-shirt table](#faq-old-or-updated) in the previous FAQ.

To check the disk size of your VM, you can run the `df -H --total | grep total` command. The following example outputs show different disk sizes for old and upgraded infrastructures:

### Old infrastructure

  ```
  $ df -H --total | grep total
  Filesystem Size Used Avail Use%
  total      12G  5.1G 6.4G  45%
  ```

### Upgraded infrastructure

  ```
  $ df -H --total | grep total
  Filesystem Size Used Avail Use%
  total      29G  6.3G 23G   22%
  ```


  ## After a virtual machine is provisioned, can I increase its block or RAM size?
  {: #faq-vm-size}
  {: faq}

  {{site.data.keyword.appserver_short}} provides [T-shirt sizing with virtual machines sized and priced in *blocks*](/docs/ApplicationServeronCloud?topic=ApplicationServeronCloud-about#vm-size){: new_window}. For each block in the T-shirt size, the virtual machine is provisioned with the following resources.
  * 1 virtual CPU (vCPU)
  * 2 GB RAM
  * 25 GB of hard drive space

After a virtual machine is provisioned, its number of blocks and RAM cannot be increased.


## How do I reset an expired virtual machine password?
{: #faq-reset-pd}
{: faq}

A VM password in the upgraded environment expires after 90 days. To reset the password, log in with your SSH key and change the `virtuser` and `wsadmin` passwords.

1. Download the `sshkey` from the **Private SSH Key for virtuser** {{site.data.keyword.cloud_notm}} service instance. See [Using SSH to access WebSphere Application Server in {{site.data.keyword.cloud_notm}} VMs](/docs/ApplicationServeronCloud?topic=ApplicationServeronCloud-system_access#using_ssh){: new_window}.
2. Use SSH and the key to connect to the VM.
  ```
  ssh -i _privateKey_rsa_ virtuser@PRIVATE_IP
  ```
  {: codeblock}

  At this step, you might get prompted to change the password. If so, change the `virtuser` and `wsadmin` passwords.

3. Switch to the root user.
  ```
  sudo su
  ```
  {: codeblock}
4. Change your `virtuser` password.
  ```
  passwd virtuser
  ```
  {: codeblock}
5. Change your `wsadmin` password.
  ```
  passwd wsadmin
  ```
  {: codeblock}

**Note**: The changed password is not shown on your service details pages in the {{site.data.keyword.cloud_notm}} console.


<!-- For detailed guidance on what to include on this page, see [FAQs guidance](/docs/developing/writing/faq.html#faqs). You can also check out some examples here: [IBM Cloud IAM FAQs](/docs/developing/Access-Management/iamfaq.html#faqs) and [Account FAQs](/docs/account/account_faq.html#accountfaqs). -->
