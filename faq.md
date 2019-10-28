---

copyright:
  years: 2019
lastupdated: "2019-10-24"

keywords: bug, problem, faqs, Frequently Asked Questions, question

subcollection: wasaas

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:faq: data-hd-content-type='faq'}

# FAQs
{: #wasaas-faqs}

Review frequently asked questions for {{site.data.keyword.appserver_short}} for {{site.data.keyword.cloud}}. To find all FAQs for {{site.data.keyword.cloud_notm}}, see the [FAQ library](/docs/faqs){: new_window}.
{: shortdesc}

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


For information about T-shirt and block sizing, see [Virtual machine sizing](/docs/ApplicationServeronCloud?topic=wasaas-about#vm-size){: new_window}.

### Different network connectivity

The upgraded infrastructure is set up on a different network than old infrastructure and requires you to set up separate OpenVPN connectivity. You cannot access virtual machines on both the old and the upgraded infrastructure with the same OpenVPN connectivity.

For more information, see [VPN access](/docs/ApplicationServeronCloud?topic=wasaas-networkEnvironment#vpnAccess){: new_window} and [Setting up OpenVPN](/docs/ApplicationServeronCloud?topic=wasaas-system_access#setup_openvpn){: new_window}.

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

## How do I migrate my application from the old infrastructure to the upgraded infrastructure?
{: #faq-migrate-infrastructure}
{: faq}

You cannot migrate the virtual machine to the upgraded infrastructure. You must move your application, data, and any other setting manually.

1. Create a new resource from https://cloud.ibm.com. When creating a resource, you can keep your existing instance or application running. See [Creating and managing resource groups](/docs/resources?topic=resources-rgs){: new_window} in the {{site.data.keyword.cloud_notm}} documentation.
2. Deploy or migrate your application and then test it.
3. After the application tests are successful, switch the traffic to the new virtual machine. Switching the traffic depends on your network setup and might require you to work with your networking team.
4. Delete the old resource.
</br></br>


**Notes**:
  * You can no longer create resources under your organization name. Similar to other {{site.data.keyword.cloud_notm}} services, {{site.data.keyword.appserver_short}} for {{site.data.keyword.cloud_notm}} supports resource groups. You must use Resource Group to [create your new resource](/docs/resources?topic=resources-rgs){: new_window}. You still will be able to access your existing resources created under your organization name. It is recommended that you rename your resource group to a meaningful name instead of `Default`.
  * You will get one or more new IP addresses and must set up new OpenVPN connectivity to access the virtual machines.
  * If you are currently using public IP, the public IP also changes. You might need to update your DNS settings to direct your customers to the new resources.
  * You might be able to [use a migration tool](#faq-migrate-tools) to move your application.


## Are there any migration tools that I can use to migrate my application?
{: #faq-migrate-tools}
{: faq}

{{site.data.keyword.appserver_short}} provides two ways to migrate your application, but each option has a limitation. Refer to documentation about the options for details.

- Use wsadmin commands to export and import profiles.

  1. Use the [`exportWasprofile` command](https://www.ibm.com/support/knowledgecenter/SSEQTP_9.0.5/com.ibm.websphere.base.doc/ae/rxml_atconfigarchive.html#rxml_atconfigarchive__cmd3){: new_window} to export the entire cell configuration to a configuration archive.
  2. Use the [`importWasprofile` command](https://www.ibm.com/support/knowledgecenter/SSEQTP_9.0.5/com.ibm.websphere.base.doc/ae/rxml_atconfigarchive.html#rxml_atconfigarchive__cmd5){: new_window} and the exported archive file to restore the configuration or to clone the original profile on another virtual machine.
</br></br>

  **Limitation**: Only a base server configuration with a single node is supported for the `exportWasprofile` command.

- Use the WebSphere Configuration Migration Tool for IBM Cloud.

  1. [Download the WebSphere Configuration Migration Tool for IBM Cloud]( https://developer.ibm.com/wasdev/downloads/#asset/tools-WebSphere_Configuration_Migration_Tool_for_IBM_Cloud){: new_window}.
  2. To migrate your application, follow instructions in the [WebSphere Configuration Migration Tool for IBM Cloud documentation](https://developer.ibm.com/wasdev/docs/websphere-config-migration-cloud/){: new_window}.
</br></br>

  **Limitation**: The tool supports migration only among {{site.data.keyword.appserver_short}} Version 9.x releases.



<!-- For detailed guidance on what to include on this page, see [FAQs guidance](/docs/developing/writing/faq.html#faqs). You can also check out some examples here: [IBM Cloud IAM FAQs](/docs/developing/Access-Management/iamfaq.html#faqs) and [Account FAQs](/docs/account/account_faq.html#accountfaqs). -->
