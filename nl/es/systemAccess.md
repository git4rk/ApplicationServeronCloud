---

copyright:
  years: 2017, 2018
lastupdated: "2018-11-20"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:tip: .tip}

# Acceso al sistema
{: #system_access}

Aquí encontrará métodos de creación y gestión de una instancia de servicio, junto con varias formas de acceder a los sistemas y configurar el acceso.
{: shortdesc}

## Uso de la API REST en WebSphere Application Server en {{site.data.keyword.Bluemix_notm}}
{: #restapi_usage}

Las instancias de WebSphere Application Server en {{site.data.keyword.Bluemix_notm}} se crean, suministran, gestionan y suprimen de una de las siguientes formas:

* En el catálogo de {{site.data.keyword.Bluemix_notm}} y el panel de control de servicios.
* En la creación de una aplicación o script que utiliza API RESTful.

Mediante el uso de las API REST compatibles con Swagger 2.0, los clientes tienen acceso a la misma función como se ha proporcionado a través del portal y panel de control. Para obtener más información sobre las API REST y los recursos soportados, consulte WebSphere Application Server en {{site.data.keyword.Bluemix_notm}} [Documentación de la API REST](https://wasaas-broker.ng.bluemix.net/wasaas-broker/api#/){: new_window}. Para consultar código de ejemplo que muestra el uso de las API REST, descargue el Git alojado en WebSphere Application Server en {{site.data.keyword.Bluemix_notm}} [Ejemplos de API REST](https://github.com/IBM-Cloud/WebSphere-in-Bluemix/tree/master/WebSphere-In-Bluemix-API-Examples){: new_window}.

**Nota:** después de crear una instancia de servicio, en función del tamaño de camiseta que se crea, puede que el servicio no esté listo inmediatamente para su uso. Se recomienda consultar el campo **Estado** del JSON devuelto para determinar el estado actual de la instancia de servicio.

**Nota:** el URL de **apiEndpoint** al que se hace referencia en los [ejemplos de las API REST](https://github.com/IBM-Cloud/WebSphere-in-Bluemix/tree/master/WebSphere-In-Bluemix-API-Examples){: new_window} apunta a la región de Dallas. Si utiliza otras regiones, asegúrese de que la aplicación hace referencia al **apiEndpoint** apropiado.

*Tabla 1. URL de punto final de API para la implementación de la API REST*

| **Nombre de la región** | **Prefijo de la región** | **URL de punto final de API** |       
|:-------------:|:--------------:|:-------------:|
| Dallas | `ng` | https://wasaas-broker.ng.bluemix.net/wasaas-broker/api  |
| Londres | `eu-gb` | https://wasaas-broker.eu-gb.bluemix.net/wasaas-broker/api  |
| Frankfurt | `eu-de` | https://wasaas-broker.eu-de.bluemix.net/wasaas-broker/api  |
| Sídney | `au-syd` | https://wasaas-broker.au-syd.bluemix.net/wasaas-broker/api  |

## Panel de control de servicio
{: #service_dashboard}

Después de crear la instancia de servicio, se le dirigirá al panel de control de servicios. Siempre puede volver al panel de control de servicio pulsando el icono de servicio desde el panel de control de la organización.
Desde el panel de control del servicio puede acceder a:

* Un enlace a esta documentación
* Un enlace para descargar los archivos de configuración de OpenVPN necesarios
* La capacidad de iniciar y detener la máquina virtual. La VM se inicia al principio
* El nombre del host
* El usuario administrador y la contraseña del administrador
* Una clave SSH privada
* El usuario administrador y la contraseña del administrador de WebSphere&reg;
* Los URL del centro de administración y la consola de administración


## Configuración de openVPN para instancias de WebSphere Application Server en {{site.data.keyword.Bluemix_notm}}
{: #setup_openvpn}

OpenVPN es necesario para acceder a cualquier máquina virtual de WebSphere Application Server en {{site.data.keyword.Bluemix_notm}}. Debe estar instalado y en ejecución con privilegios de administrador.

### Configurar openVPN en Windows

1. Descargue el programa de instalación de openVPN en Windows para su arquitectura del sistema desde el sitio web de openVPN:
  * Sistemas de 64 bits: [openvpn-install-2.3.4-I001-x86_64.exe](https://swupdate.openvpn.org/community/releases/openvpn-install-2.3.4-I001-x86_64.exe){: new_window}
  * Sistemas de 32 bits:  [openvpn-install-2.3.4-I001-i686.exe](https://swupdate.openvpn.org/community/releases/openvpn-install-2.3.4-I001-i686.exe){: new_window}
2. Asegúrese de que [trabaja como administrador de Windows](https://technet.microsoft.com/en-us/magazine/ff431742.aspx){: new_window} y de que openVPN está instalado.
3. Descargue los archivos de configuración de VPN desde el enlace de descarga de OpenVPN de la instancia de WebSphere Application Server en {{site.data.keyword.Bluemix_notm}} en el panel de control de servicios. Extraiga los cuatro archivos en el archivo comprimido en el directorio `{inicio OpenVPN}\config`. Por ejemplo:

  ```  
  C:\Program Files\OpenVPN\Config
  ```

4. Inicie el programa cliente openVPN "OpenVPN GUI". Asegúrese de que selecciona **Ejecutar como administrador de Windows** para iniciar el programa. Si no lo hace, no podrá conectarse.

### Configurar openVPN en Linux

1. Para instalar openVPN, siga las [instrucciones de openVPN para Linux](https://openvpn.net/index.php/access-server/docs/admin-guides/182-how-to-connect-to-access-server-with-linux-clients.html){: new_window}.

   Si necesita descargar e instalar manualmente el gestor de paquetes de RPM, vaya a la [descarga de openVPN unix/linux](https://openvpn.net/index.php/access-server/download-openvpn-as-sw.html){: new_window}. Es posible que necesite ayuda del administrador de Linux.
3. Descargue los archivos de configuración de VPN desde el enlace de descarga de OpenVPN de la instancia de WebSphere Application Server en {{site.data.keyword.Bluemix_notm}} en el panel de control de servicios. Extraiga los archivos en el directorio desde el que tiene previsto iniciar el cliente openVPN. Necesita los cuatro archivos en el mismo directorio.
3. Inicie el programa cliente openVPN. Abra una ventana de terminal y vaya al directorio que contiene los archivos de configuración. Ejecute el mandato siguiente como usuario root:

  ```
  openvpn --config vt-wasaas-wasaas.ovpn
  ```
  {: .codeblock}  

### Configurar openVPN en Mac
1. Un método consiste en instalar [Tunnelblick](https://tunnelblick.net/){: new_window}, un producto de software de código abierto.
2. Extraiga los archivos de configuración de VPN desde el servicio de WebSphere. Tunnelblick le solicita la contraseña de administrador para Mac y añade la configuración al conjunto de VPN que puede utilizar para conectarse.
3. Conéctese a la red de VPN y, a continuación, podrá acceder a la máquina virtual. Después del primer acceso, Tunnelblick almacena en memoria caché la configuración y puede conectarse desde Tunnelblick. Puede colocar un icono en la barra de menús para facilitar el acceso.


## Utilización de SSH para acceder a máquinas virtuales de WebSphere Application Server en {{site.data.keyword.Bluemix_notm}}
{: #using_ssh}

En estas instrucciones se da por supuesto que utiliza OpenSSH como cliente. OpenSSH está disponible normalmente en Linux o en Cygwin ejecutándose en Windows. También puede instalarse para ejecutarse desde un indicador de mandatos de Windows.

Para verificar la instalación de OpenSSH, ejecute el siguiente mandato.
  ```
  ssh -V
  ```
  {: codeblock}

El siguiente mensaje es un ejemplo de respuesta:
  ```
  OpenSSH_6.6p1, OpenSSL 1.0.1g 7 Apr 2014
  ```

Siga las instrucciones siguientes para configurar el acceso SSH a las VM de WebSphere Application Server en {{site.data.keyword.Bluemix_notm}}.

1. Revise el mensaje de aviso que aparece la primera vez que se conecta, "La autenticidad del host x.x.x.x no se puede establecer." Este mensaje es normal. Cuando se le solicite, seleccione Sí. Ahora la clave pública está instalada en la máquina virtual para el usuario **virtuser**.
2. Inicie la sesión en **virtuser** utilizando la clave privada. Para obtener mejores resultados, utilice el método de autenticación de clave privada.
3. Copie el contenido de la clave privada en un archivo.
4. Conecte mediante SSH ejecutando el siguiente mandato.

  ```
  ssh virtuser@169.53.246.xxx -i /path/privateKeyFileName
  ```
  {: codeblock}

5. Obtenga la autorización sysadmin completa pasando de **virtuser** a **root** con el siguiente mandato.

  ```
  sudo su root
  ```
  {: codeblock}

6. Si experimenta problemas al acceder al sistema con la clave ssh privada, utilice la contraseña de usuario root proporcionada. Inicie sesión como usuario root ejecutando el mandato siguiente y especifique la contraseña.

  ```
  ssh root@169.53.246.x
  ```
  {: codeblock}

7. Tanto si accede al sistema con la clave SSH privada como si lo hace con la contraseña de root, cambie inmediatamente la contraseña de root.
8. Para simplificar los mandatos SSH, cree un archivo llamado `config` en el directorio `%HOME%/.ssh`. Por ejemplo:

   ```
   Host VM1
      Hostname 169.53.246.xxx
      User virtuser
      IdentityFile /path/privateKeyFileName
   ```
   {: codeblock}

9. Ejecute el siguiente mandato para conectarse como **virtuser**.

   ```
   ssh VM1
   ```
   {: codeblock}

## Vías de acceso del sistema
{: #system_paths}

* Los mandatos de Liberty pueden emitirse desde `/opt/IBM/WebSphere/Liberty/bin`.
* La ubicación del perfil de servidor de Liberty es `/opt/IBM/WebSphere/Profiles/Liberty/servers/server1`.
* Los archivos del producto WebSphere Application Server tradicional, que comparten todos los perfiles, se encuentran en `/opt/IBM/WebSphere/AppServer/`.
* Los mandatos de WebSphere Application Server tradicional se emiten desde la ubicación del perfil predeterminado en `/opt/IBM/WebSphere/Profiles/Default<profile_type><profile_number>/bin` donde:
  * `<profile_type> tiene el valor `AppSrv`, `Dmgr`, `Custom`, `AdminAgent`, `JobMgr` o `SecureProxySrv`.
  * `<profile_number>` es un número secuencial que se utiliza para crear un nombre de perfil exclusivo.


## Gestión de servidores desde la línea de mandatos
{: #start_servers}

**Evite problemas:** cuando gestione servidores WebSphere desde la línea de mandatos, asegúrese de utilizar **wsadmin**, el ID de administración de WebSphere, no **virtuser**. Cuando gestione el servidor IHS desde la línea de mandatos, asegúrese de utilizar **root**.

## Utilización de los enlaces del centro de administración y la consola de administración
{: #console_links}

Al pulsar el enlace con el centro de administración o con la consola de administración, puede recibir un aviso parecido a *Conexión no fiable*. El texto del mensaje exacto varía según el navegador, así como los pasos exactos para omitir o eliminar el aviso.

Puesto que está utilizando enlaces proporcionados por {{site.data.keyword.IBM}},
puede ignorar sin problemas el aviso y conectarse. Si el navegador ofrece almacenar una excepción de seguridad, si lo hace será la forma más fácil de impedir el aviso en el futuro.

Otra opción exportar el certificado de firmante entrante y, a continuación, importarlo al navegador como certificado raíz de confianza. Esta opción podría requerir que realizara una entrada en el archivo *hosts* que correlaciona la dirección IP de VM con el nombre común del emisor de certificado. Este nombre tiene el siguiente formato: `wl<pureapplication.ibmcloud.com`. Si ahora utiliza el nombre del host en lugar de la dirección IP en el URL, podrá conectarse sin problemas. A continuación debe acceder al centro de administración o a la consola de administración utilizando ese nombre de host en lugar de la dirección IP en el URL.

Por último, los clientes a menudo instalan sus propios certificados raíz para las aplicaciones que hacen externas. Para obtener más información, consulte la documentación de [WebSphere Application Server](https://www.ibm.com/support/knowledgecenter/SSAW57_9.0.0/com.ibm.websphere.nd.multiplatform.doc/ae/tsec_securecomm.html){: new_window} o de [Liberty
Core](https://www.ibm.com/support/knowledgecenter/SSD28V_9.0.0/com.ibm.websphere.wlp.core.doc/ae/twlp_sec_comm.html){: new_window} en IBM Knowledge Center.

## Puertos de cortafuegos
{: #firewall_ports}

Es probable que deba abrir puertos en el cortafuegos para permitir el acceso a aplicaciones y bases de datos. Puede abrir puertos de cortafuegos con el script `openFirewallPorts.sh`, que encontrará en las siguientes ubicaciones.
  * En cada WebSphere Application Server del nodo de {{site.data.keyword.Bluemix_notm}}, el script `openFirewallPorts.sh` está en el directorio `WAS_HOME/virtual/bin`.
  * En cada host colectivo de Liberty, el script `openFirewallPorts.sh` está en el directorio `WAS_HOME/virtual/bin`.

### Utilización

Ejecute el script `openFirewallPorts.sh` con la siguiente sintaxis del mandato.

  ```
  openFirewallPorts.sh -ports <PORT>:<PROTOCOL>,... -persist true|false
  ```
  {: codeblock}

donde:
* PUERTO es un número de puerto
* PROTOCOLO es TCP o UDP
* `-persist` puede ser `true` o `false`

Puede especificar varios puertos en una lista separada por comas.

**Nota**: los parámetros sport y dport del puerto abierto se abren en las secciones INPUT y OUTPUT del cortafuegos. Debe ejecutar este script como root utilizando `sudo`. También puede
modificar iptables directamente.

## Configuración del servidor web
{: #configure_webserver}

Si suministra un entorno de célula o colectivo, recibirá un entorno preconfigurado. En concreto, para una célula Traditional Network Deployment, recibirá el siguiente entorno:

* Un gestor de despliegue colocado junto a un IBM HTTP Server para desarrollo y prueba.
* Un nodo personalizado federado con el gestor de despliegue.
* El gestor de despliegue, el servidor IHS y el agente de nodo, todos inicialmente en estado INICIADO.

Si necesita el servidor web para manejar todas las solicitudes de usuario, es posible que tenga que generar y propagar el plugin después de desplegar la aplicación.

**Evite problemas:** antes de generar y propagar el plugin, asegúrese de haber completado las siguientes tareas previas necesarias.

* En el entorno Windows, Linux o MAC local, asegúrese de que [openVPN](systemAccess.html#setup_openvpn) esté configurado e iniciado y de que esté conectado a la región adecuada.
* En el panel de control de servicio de WebSphere Application Server en {{site.data.keyword.Bluemix_notm}}, pulse **Abrir la consola de administración** e inicie una sesión con wsadmin y la contraseña del administrador que se proporciona en el panel de control de servicio.
* En la consola de administración, cree un servidor de aplicaciones (por ejemplo, ***server1***), ya que el gestor de despliegue está federado con un nodo personalizado vacío.
* Inicie el servidor que ha creado.
* Durante la instalación de la aplicación, asegúrese de que los módulos de la aplicación estén correlacionados con el servidor que acaba de iniciar y con el servidor web (por ejemplo, ***webserver1***).

En los pasos siguientes se da por supuesto que se han llevado a cabo las tareas previas necesarias.

1. En la consola de administración, genere el plugin desde la opción Entorno.
   1. Elija **Entorno > Actualizar configuración global de plugin de servidor web**.
   2. Pulse **Aceptar** o **Sustituir para generar un nuevo archivo de configuración de plugin**.
2. En el gestor de despliegue, copie el plugin en la configuración del servidor web.

  ```
   cp /opt/IBM/WebSphere/Profiles/DefaultDmgr01/config/cells/plugin-cfg.xml /opt/IBM/WebSphere/Plugins/config/webserver1/plugin-cfg.xml
  ```
  {: codeblock}
3. Abra el archivo `httpd.conf` en `IHS_HOME/conf` (por ejemplo, `/opt/IBM/WebSphere/HTTPServer/conf`), y asegúrese de que contiene las dos líneas siguientes.

    ```
    LoadModule was_ap22_module /opt/IBM/WebSphere/Plugins/bin/64bits/mod_was_ap22_http.so
    WebSpherePluginConfig /opt/IBM/WebSphere/Plugins/config/webserver1/plugin-cfg.xml
    ```
    {: codeblock}  
4. Abra los puertos con los siguientes mandatos.

   ```
   export serverPorts=2810:TCP,2810:UDP,8880:TCP,8880:UDP,9101:TCP,9101:UDP,9061:TCP,9061:UDP,9080:TCP,9080:UDP,9354:TCP,9354:UDP,9044:TCP,9044:UDP,9443:TCP,9443:UDP,5060:TCP,5060:UDP,5061:TCP,5061:UDP,11005:TCP,11005:UDP,11007:TCP,11007:UDP,9633:TCP,9633:UDP,7276:TCP,7276:UDP,7286:TCP,7286:UDP,5558:TCP,5558:UDP,5578:TCP,5578:UDP

   sudo /opt/IBM/WebSphere/AppServer/virtual/bin/openFirewallPorts.sh -ports $serverPorts -persist true
   ```
   {: codeblock}
5. Detenga e inicie el servidor web con los mandatos siguientes:
    ```
    sudo /opt/IBM/WebSphere/HTTPServer/bin/apachectl -k stop
    sudo /opt/IBM/WebSphere/HTTPServer/bin/apachectl -k start
    ```
    {: codeblock}
8. Acceda a la aplicación a través del plugin.
  ```
   http://169.53.246.xxx/contextRoot/
  ```
  {: codeblock}

**Nota:** los pasos proporcionados representan una vía de acceso de las muchas posibles cuando intenta configurar un servidor web. Si necesita ayuda, consulte [IBM Knowledge Center](https://www.ibm.com/support/knowledgecenter/search/configure%20web%20server?scope=SSAW57_9.0.0){: new_window}.

Si no puede acceder a la aplicación, es posible que se trate de un problema de acceso al puerto en el cortafuegos. Por lo tanto, es posible que tenga que reiniciar alguno de los siguientes servidores: el servidor de aplicaciones, el agente del nodo, el servidor web y el gestor de despliegue. Además, es posible que tenga que acceder a WebSphere Application Server en el panel de control del servicio de {{site.data.keyword.Bluemix_notm}} para reiniciar cada máquina virtual.
{: tip}

## Configuración de SSL
{: #ssl_configuration}

WebSphere Application Server tradicional y Liberty se configuran con el protocolo [SSL_TLSv2](https://www.ibm.com/support/knowledgecenter/en/SSYKE2_8.0.0/com.ibm.java.security.component.80.doc/security-component/jsse2Docs/protocols.html){: new_window}. Puede cambiar el protocolo modificando la configuración de SSL.

### WebSphere Application Server tradicional
{: #ssl-was}

1. Abra el archivo `security.xml` en el directorio `/opt/IBM/WebSphere/Profiles/<profile_name>/config/cell/<cell_name>` y modifique la siguiente línea.

   ```
   sslProtocol="SSL_TLSv2"
   ```
   {: codeblock}

2. Abra el archivo `ssl.client.props` en el directorio `/opt/IBM/WebSphere/Profiles/<profile_name>/properties` y modifique la siguiente línea.

   ```
   com.ibm.ssl.protocol=SSL_TLSv2
   ```
   {: codeblock}

### Liberty
{: #ssl-liberty}

1. Abra el archivo `server.xml` en el directorio `/opt/IBM/WebSphere/Profiles/Liberty/servers/server1` y modifique la siguiente línea en el elemento de configuración de SSL `defaultSSLConfig`.

   ```
   sslProtocol="SSL_TLSv2"
   ```
   {: codeblock}
