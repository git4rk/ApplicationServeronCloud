---

copyright:
  years: 2017, 2018
lastupdated: "2018-12-13"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Updating your environment
{: #updating-your-environment}

## Maintenance strategy
{: #maintenance-strategy}

{{site.data.keyword.appserver_full}} is updated on a regular cadence, ensuring that new service instances are created with current fix packs and patches. The cloud brings easy and rapid provisioning of new service instances to middleware management.

You can create a WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} instance at the current or previous fix pack level (n or n-1) for a particular product version. Using current fix pack provides the latest updates and features, but the previous fix pack might be needed to conform with hybrid cloud deployment requirements.

When you create a new instance, you can choose from the following fix pack levels on the **Service Profile** tab in the service instance:

**Liberty**
  * 18.0.0.4
  * 18.0.0.3

**WebSphere Application Server traditional**
  * 9.0.0.10
  * 9.0.0.9
  * 8.5.5.14
  * 8.5.5.13

## Applying fixes and fix pack updates
{:#applying-fixes}

The fastest way to update to the latest maintenance level is to create a new instance. However, if you prefer to retain long-lived service instances, you can apply maintenance to your existing installation by running the provided `installService.sh` script or by using IBM Installation Manager as described in the following sections.

### Updating by using the installService.sh script

Your service instance is configured with an Installation Manager repository that is frequently updated with available security fixes and WebSphere Application Server fix packs. You can use the `/home/virtuser/installService.sh` script to apply these fixes and fix packs. The script must be run as the root user.

The amount of disk space that is required to install the updates varies depending on the types of updates that you install. Installing only interim fixes requires 1 GB of free space on the virtual machine. Installing fix packs increased the required disk space to 1.3 GB.

Running the script performs the following actions:

* Stops all running WebSphere Application Server and IBM HTTP Server instances
* Optionally installs the latest fix packs for Installation Manager, WebSphere Application Server, IBM HTTP Server, and the Java&trade; SDK
* Installs the latest interim fixes for WebSphere, IBM HTTP Server, and the Java&trade; SDK
* Restarts all instances

#### Options
* **`-fixpacks`**

    Updates all packages to the latest fix pack.
* **`-noprompt`**

    Does not prompt for confirmation before it updates.

#### Syntax examples

```
./installService.sh -?
```
{:.codeblock}

Displays help text.


```
./installService.sh
```
{:.codeblock}

Installs all applicable interim fixes, but no fix packs.


```
./installService.sh -fixpacks
```
{:.codeblock}

Installs all available fix packs, and then installs all applicable interim fixes.

### Updating by using Installation Manager
{:#installation-manager}

[Installation Manager](http://www.ibm.com/support/knowledgecenter/SSDV2W_1.8.3/com.ibm.cic.agent.ui.doc/helpindex_imic.html){: new_window} is installed in the `/home/virtuser/IBM/Installation Manager` directory and can be run directly to apply fixes and fix packs.

**Avoid trouble:** Because the underlying binary files are installed as `virtuser`, a limited administrative virtual user, ensure that Installation Manager is always run as `virtuser`.

## Applying system updates to virtual machines
{:#vm-system-updates}

Applying system updates on a virtual machine is similar to updating a physical Red Hat Enterprise Linux&reg; (RHEL) system. By using the Yum package manager, you can install, update, uninstall, and otherwise manage packages. WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} systems are configured to receive updates from IBM's Red Hat Satellite server, which provides safe and secure packages from the Red Hat network. The Satellite server is managed by IBM and cannot be modified from your system.

For more information, see [Applying package updates on Red Hat Enterprise Linux](https://access.redhat.com/articles/11258#rhel6){: new_window} and [Yum, the Red Hat package manager](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/6/html/Deployment_Guide/ch-yum.html){: new_window}.
