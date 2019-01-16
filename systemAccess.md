---

copyright:
  years: 2017, 2019
lastupdated: "2019-01-16"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# System access
{: #system_access}

Learn methods of creating and managing a service instance, and explore ways to access and set up access to your systems.
{: shortdesc}

## REST API usage in WebSphere Application Server in {{site.data.keyword.Bluemix_notm}}
{: #restapi_usage}

Instances in WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} are created, provisioned, managed, and deleted in one of the following ways:

* From the {{site.data.keyword.Bluemix_notm}} catalog and service dashboard.
* From the creation of an application or script that uses RESTful APIs.

Through use of Swagger 2.0 compliant REST APIs, clients have access to the same function as provided through the portal and dashboard. For more information about supported REST APIs and resources, see the WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} [REST API Documentation](https://wasaas-broker.us-south.websphereappsvr.cloud.ibm.com/wasaas-broker/api#/){: new_window}. For sample code that demonstrates usage of the REST APIs, download the Git hosted WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} [REST API Samples](https://github.com/IBM-Cloud/WebSphere-in-IBM-Cloud/tree/master/WebSphere-In-IBM-Cloud-API-Examples){: new_window}.

**Note:** After you create a service instance, depending on the T-shirt size that is created, your service might not be immediately ready for use. It is recommended that you query the **Status** field of the JSON returned to determine the current state of the service instance.

**Note:** The **apiEndpoint** URL referenced in the [REST API Samples](https://github.com/IBM-Cloud/WebSphere-in-IBM-Cloud/tree/master/WebSphere-In-IBM-Cloud-API-Examples){: new_window} points to the Dallas region. If you are using other regions, ensure that your application references the appropriate **apiEndpoint**.

*Table 1. API Endpoint URLs for REST API Implementation*

| **Region name** | **Region prefix** | **API Endpoint URL** |       
|:-------------:|:--------------:|:-------------:|
| Dallas | `us-south` | https://wasaas-broker.us-south.websphereappsvr.cloud.ibm.com/wasaas-broker/api  |
| London | `eu-gb` | https://wasaas-broker.eu-gb.websphereappsvr.cloud.ibm.com/wasaas-broker/api  |
| Frankfurt | `eu-de` | https://wasaas-broker.eu-de.websphereappsvr.cloud.ibm.com/wasaas-broker/api  |
| Sydney | `au-syd` | https://wasaas-broker.au-syd.websphereappsvr.cloud.ibm.com/wasaas-broker/api  |

## Service dashboard
{: #service_dashboard}

After you create your service instance, you are taken to the service dashboard. You can always get back to the service dashboard by clicking the service icon from your organization dashboard.
From the service dashboard you can access:

* A link to this documentation
* A link to download the required OpenVPN configuration files
* The ability to start and stop the virtual machine. The VM is initially started
* The host name
* The admin user and admin password
* A private SSH key
* The WebSphere&reg; admin user and admin password
* The Admin Center and Admin Console URLs


## Setting up openVPN for WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} instances
{: #setup_openvpn}

OpenVPN is required for access to any WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} virtual machine. It must be installed and running with administrator privileges.

### Set up openVPN on Windows

1. Download the openVPN Windows installer for your system architecture from the openVPN website:
  * 64-bit systems: [openvpn-install-2.3.4-I001-x86_64.exe](https://swupdate.openvpn.org/community/releases/openvpn-install-2.3.4-I001-x86_64.exe){: new_window}
  * 32-bit systems:  [openvpn-install-2.3.4-I001-i686.exe](https://swupdate.openvpn.org/community/releases/openvpn-install-2.3.4-I001-i686.exe){: new_window}
2. Ensure you [run as a Windows Administrator](https://technet.microsoft.com/en-us/magazine/ff431742.aspx){: new_window} and openVPN is installed.
3. Download the VPN configuration files from the OpenVPN download link of the WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} instance in the service dashboard. Extract all four files in the compressed file to the `{OpenVPN home}\config` directory. For example:

  ```  
  C:\Program Files\OpenVPN\Config
  ```

4. Start the openVPN client program "OpenVPN GUI". Ensure that you select **Run as a Windows Administrator** to start the program. If you do not, you might not be able to connect.

### Set up openVPN on Linux

1. To install openVPN, follow the [openVPN instructions for Linux](https://openvpn.net/index.php/access-server/docs/admin-guides/182-how-to-connect-to-access-server-with-linux-clients.html){: new_window}.

   If you need to manually download and install the RPM Package Manager, go to [openVPN unix/linux download](https://openvpn.net/index.php/access-server/download-openvpn-as-sw.html){: new_window}. You might need assistance from your Linux administrator.
3. Download the VPN configuration files from the OpenVPN download link of the WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} instance in the service dashboard. Extract the files into the directory from which you plan to start the openVPN client. You need all four files in the same directory.
3. Start the openVPN client program. Open a terminal window and go to the directory that contains the configuration files. Run the following command as root:

  ```
  openvpn --config vt-wasaas-wasaas.ovpn
  ```
  {: .codeblock}  

### Set up openVPN on Mac
1. One method is to install [Tunnelblick](https://tunnelblick.net/){: new_window}, an open source software product.
2. Extract the VPN configuration files from the WebSphere service. Tunnelblick prompts for your admin password for Mac and adds the config to the set of VPNs you can use to connect.
3. Connect to the VPN network and then you can access your virtual machine. After your first access, Tunnelblick caches the configuration and you can connect from Tunnelblick. You can put an icon on the menu bar for easy access.


## Using SSH to access WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} VMs
{: #using_ssh}

These instructions assume that you are using OpenSSH as your client. OpenSSH is normally available on Linux or in Cygwin running on Windows. It also can be installed to run from a Windows command prompt.

To verify installation of OpenSSH, run the following command.
  ```
  ssh -V
  ```
  {: codeblock}

The following message is an example of the response:
  ```
  OpenSSH_6.6p1, OpenSSL 1.0.1g 7 Apr 2014
  ```

Use the following instructions to set up SSH access to your WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} VMs.

1. Review the warning message that appears the first time you connect, "The authenticity of host x.x.x.x cannot be established." This message is normal. When prompted, select yes. The public key is now installed on your VM for the user **virtuser**.
2. Log in to **virtuser** by using the private key. For best results, use the private key authentication method.
3. Copy the contents of the private key into a file.
4. Connect using SSH by running the following command.

  ```
  ssh virtuser@169.53.246.xxx -i /path/privateKeyFileName
  ```
  {: codeblock}

5. Gain full sysadmin authority by switching **virtuser** to **root** by running the following command.

  ```
  sudo su root
  ```
  {: codeblock}

6. If you experience problems when you access the system with the private ssh key, use the root password that is provided. Log in as root by running the command that follows and provide the password.

  ```
  ssh root@169.53.246.x
  ```
  {: codeblock}

7. Whether you access the system with the private ssh key or the root password, immediately change the root password.
8. To simplify your SSH commands, create a file that is named `config` in the `%HOME%/.ssh` directory. For example:

   ```
   Host VM1
      Hostname 169.53.246.xxx
      User virtuser
      IdentityFile /path/privateKeyFileName
   ```
   {: codeblock}

9. Run the following command to connect as **virtuser**.

   ```
   ssh VM1
   ```
   {: codeblock}

## System paths
{: #system_paths}

* The Liberty commands can be issued from `/opt/IBM/WebSphere/Liberty/bin`.
* The Liberty server profile location is `/opt/IBM/WebSphere/Profiles/Liberty/servers/server1`.
* The Traditional WebSphere Application Server core product files, which are shared by all profiles, are located in `/opt/IBM/WebSphere/AppServer/`.
* The Traditional WebSphere Application Server commands can be issued from the default profile location in `/opt/IBM/WebSphere/Profiles/Default<profile_type><profile_number>/bin` where:
  * `<profile_type>` is a value of `AppSrv`, `Dmgr`, `Custom`, `AdminAgent`, `JobMgr`, or `SecureProxySrv`.
  * `<profile_number>` is a sequential number that is used to create a unique profile name.


## Managing servers from the command line
{: #start_servers}

**Avoid trouble:** When you manage WebSphere servers from the command line, be sure to use **wsadmin**, the WebSphere Administrative ID, not **virtuser**. When you manage the IHS server from the command line, be sure to use **root**.

## Using the Admin Center and Admin Console links
{: #console_links}

When you click the link to the Admin Center or the Admin Console, you might receive an *Untrusted Connection* warning. The exact message text varies by browser, as do the exact steps to bypass or eliminate the warning.

Since you are using links that are provided by {{site.data.keyword.IBM}}, you can safely ignore the warning and connect. If your browser offers to store a security exception, doing so is the easiest way to prevent the warning in the future.

Another option is to export the incoming signer certificate and then import it into your browser as a trusted root certificate. This option would require you to make an entry in your *hosts* file that maps the VM's IP address to the certificate issuer's common name. This name is in the following format: `wl<pureapplication.ibmcloud.com`. If you now use the host name instead of the IP address in the URL, you can connect cleanly. You then must access the Admin Center or Admin Console by using that host name instead of the IP address in the URL.

Lastly, customers often install their own root certificates for applications they make external. For more information, refer to the [WebSphere Application Server](https://www.ibm.com/support/knowledgecenter/SSAW57_9.0.0/com.ibm.websphere.nd.multiplatform.doc/ae/tsec_securecomm.html){: new_window} or [Liberty Core](https://www.ibm.com/support/knowledgecenter/SSD28V_9.0.0/com.ibm.websphere.wlp.core.doc/ae/twlp_sec_comm.html){: new_window} documentation in IBM Knowledge Center.

## Firewall ports
{: #firewall_ports}

You might find it necessary to open ports on the firewall to allow access to applications and databases. You can open firewall ports by using the `openFirewallPorts.sh` script, which you can find in the following locations.
  * On each WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} node, the `openFirewallPorts.sh` script is in the `WAS_HOME/virtual/bin` directory.
  * On each Liberty collective host, the `openFirewallPorts.sh` is in the `WAS_HOME/virtual/bin` directory.

### Usage

Run the `openFirewallPorts.sh` script using the following command syntax.

  ```
  openFirewallPorts.sh -ports <PORT>:<PROTOCOL>,... -persist true|false
  ```
  {: codeblock}

where:
* PORT is a port number
* PROTOCOL is either TCP or UDP
* `-persist` is either `true` or `false`

You can specify multiple ports in a comma-separated list.

**Note**: The sport and dport of the port that is opened is open in the INPUT and OUTPUT sections of the firewall. You must run this script as root by using `sudo`. You can also modify iptables directly.

## Configuring the web server
{: #configure_webserver}

When you provision a cell or a collective, you receive a preconfigured environment. Specifically, for a Traditional Network Deployment cell, you receive the following environment:

* A Deployment Manager that is collocated with the IBM HTTP Server for development and testing purposes.
* A custom node federated to the Deployment Manager.
* The Deployment Manager, the IHS Server, and the Node Agent all initially provisioned to the STARTED state.

If you require the web server to handle all user requests, then you might need to generate and propagate the plug-in after you deploy your application.

**Avoid trouble:** Before you generate and propagate the plug-in, ensure that the following prerequisite tasks are complete.

* In your local Windows, Linux or MAC environment, ensure that [openVPN](systemAccess.html#setup_openvpn) is configured, started and you are connected to the appropriate region.
* From the WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} service dashboard, click **Open the admin console** and log in with wsadmin and the Admin Password that is provided in the service dashboard.
* From the Admin Console, create an application server (for example, ***server1***), because the Deployment Manager is federated with an empty custom node.
* Start the server that you created.
* During application installation, ensure that the modules of your application are mapped to the server you just started and to the web server (for example, ***webserver1***).

The following high-level steps assume that the prerequisite tasks are complete.

1. From the Admin Console, generate the plug-in from the Environment option.
   1. Choose **Environment > Update global web server plug-in configuration**.
   2. Click **OK** or **Overwrite to generate a new plug-in configuration file**.
2. From the Deployment Manager, copy the plug-in to the web server configuration.

  ```
   cp /opt/IBM/WebSphere/Profiles/DefaultDmgr01/config/cells/plugin-cfg.xml /opt/IBM/WebSphere/Plugins/config/webserver1/plugin-cfg.xml
  ```
  {: codeblock}
3. Open the `httpd.conf` file in the `IHS_HOME/conf` (for example, `/opt/IBM/WebSphere/HTTPServer/conf`), and ensure that the following two lines exist.

    ```
    LoadModule was_ap22_module /opt/IBM/WebSphere/Plugins/bin/64bits/mod_was_ap22_http.so
    WebSpherePluginConfig /opt/IBM/WebSphere/Plugins/config/webserver1/plugin-cfg.xml
    ```
    {: codeblock}  
4. Open the ports by running the following commands.

   ```
   export serverPorts=2810:TCP,2810:UDP,8880:TCP,8880:UDP,9101:TCP,9101:UDP,9061:TCP,9061:UDP,9080:TCP,9080:UDP,9354:TCP,9354:UDP,9044:TCP,9044:UDP,9443:TCP,9443:UDP,5060:TCP,5060:UDP,5061:TCP,5061:UDP,11005:TCP,11005:UDP,11007:TCP,11007:UDP,9633:TCP,9633:UDP,7276:TCP,7276:UDP,7286:TCP,7286:UDP,5558:TCP,5558:UDP,5578:TCP,5578:UDP

   sudo /opt/IBM/WebSphere/AppServer/virtual/bin/openFirewallPorts.sh -ports $serverPorts -persist true
   ```
   {: codeblock}
5. Stop and start the web server by running the following commands:
    ```
    sudo /opt/IBM/WebSphere/HTTPServer/bin/apachectl -k stop
    sudo /opt/IBM/WebSphere/HTTPServer/bin/apachectl -k start
    ```
    {: codeblock}
8. Access your application through the plug-in.
  ```
   http://169.53.246.xxx/contextRoot/
  ```
  {: codeblock}

**Note:** The steps that are provided represent one path of many when you're attempting to configure a web server. If further assistance is needed, see [IBM Knowledge Center](https://www.ibm.com/support/knowledgecenter/search/configure%20web%20server?scope=SSAW57_9.0.0){: new_window}.

If you cannot access your application, you are likely facing a port access issue on your firewall. Therefore, you might need to restart any of the following servers: the application server, the node agent, the web server, and the deployment manager. Additionally, it is possible that you might need to access the WebSphere Application Server in {{site.data.keyword.Bluemix_notm}} Service Dashboard and restart each virtual machine.
{: tip}

## SSL configuration
{: #ssl_configuration}

WebSphere Application Server traditional and Liberty are configured with the [SSL_TLSv2](https://www.ibm.com/support/knowledgecenter/SSYKE2_8.0.0/com.ibm.java.security.component.80.doc/security-component/jsse2Docs/protocols.html){: new_window} protocol. You can change the protocol by modifying the SSL configuration.

### WebSphere Application Server traditional
{: #ssl-was}

1. Open the `security.xml` file in the `/opt/IBM/WebSphere/Profiles/<profile_name>/config/cell/<cell_name>` directory, and modify the following line.

   ```
   sslProtocol="SSL_TLSv2"
   ```
   {: codeblock}

2. Open the `ssl.client.props` file in the `/opt/IBM/WebSphere/Profiles/<profile_name>/properties` directory, and modify the following line.

   ```
   com.ibm.ssl.protocol=SSL_TLSv2
   ```
   {: codeblock}

### Liberty
{: #ssl-liberty}

1. Open the `server.xml` file in the `/opt/IBM/WebSphere/Profiles/Liberty/servers/server1` directory, and modify the following line within the `defaultSSLConfig` SSL configuration element.

   ```
   sslProtocol="SSL_TLSv2"
   ```
   {: codeblock}
