---

copyright:
  years: 2017, 2019
lastupdated: "2019-01-16"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Entorno de red
{: #networkEnvironment}

Una vez suministrada la instancia de servicio de {{site.data.keyword.appserver_full}}, puede acceder a VM de varias formas. Puede conectarse sobre una VPN segura para obtener SSH, puede utilizar la consola de administración de WebSphere tradicional y puede acceder por aplicación a VM. También puede conectar VM a Internet con una dirección IP pública.

En el siguiente diagrama se muestran estos métodos de red:

Figura 1. Vista de cliente con red multiarrendatario con IP pública

![Figura 1. Vista de cliente con una red multiarrendatario con IP pública](images/wasaas_multi_tenant_publicIP.png)

## Acceso VPN
{: #vpnAccess}

Después de suministrar una instancia de servicio de WebSphere Application Server en {{site.data.keyword.Bluemix_notm}} desde el panel de control de servicios de la interfaz de usuario de {{site.data.keyword.Bluemix_notm}}, puede establecer una conexión OpenVPN. Para crear la conexión, expanda el menú desplegable y pulse **Descargar configuración de VPN** para descargar la configuración de VPN. La configuración de VPN contiene un archivo `.ovpn` y los certificados que se utilizan para autenticarse con el servidor OpenVPN. Una vez que se ha establecido la conexión OpenVPN, puede acceder a la máquina virtual a través de SSH. También puede acceder a Liberty Admin Center, a la consola de administración de WebSphere tradicional y a las aplicaciones.

La configuración de VPN se circunscribe a su organización y su región. Es válida durante un año a partir de la hora de creación. Se pueden establecer varias conexiones de cliente OpenVPN simultáneamente utilizando la misma configuración de VPN.

**Nota:** la configuración de VPN solo es válida si la organización contiene suscripciones **activas**. Cuando se suprime la última suscripción de una organización, se suspenden todas las configuraciones de VPN de la organización. Las configuraciones de VPN que no han vencido se reactivan automáticamente cuando se activa una nueva suscripción.

## Gestión avanzada de configuración de VPN
{: #advancedVPN}

En la mayoría de los casos, solo necesita una única configuración de VPN, que se pueda descargar con el botón **Descargar configuración de VPN**. Sin embargo, la página de gestión avanzada de VPN, a la que se accede pulsando **Gestión avanzada de VPN** en el panel de control de servicios, le permite crear y gestionar varias configuraciones de VPN. El hecho de tener varias configuraciones puede ser útil para la transición sin problemas a una nueva configuración de VPN cuando la antigua está a punto de caducar. También puede solicitar varias configuraciones de VPN para gestionar el acceso a sus VM con distintos usuarios o equipos de la organización.  

**Nota:** se le permite un **máximo** de 10 configuraciones de VPN activas para su organización en cualquier momento.

Si las configuraciones de VPN están comprometidas o caducadas, puede revocar la configuración de VPN mediante la página de gestión avanzada de VPN. Además, desde una perspectiva de auditoría, puede ver un historial de toda la actividad de gestión de VPN y descargar las configuraciones de VPN activas que se han creado anteriormente desde la página de gestión avanzada de VPN.

También se pueden crear scripts de todas las características disponibles en el panel de control de servicios de la IU de {{site.data.keyword.Bluemix_notm}} mediante las API REST. Para obtener más información, consulte el apartado sobre WebSphere Application Server en la [Documentación de la API REST](https://wasaas-broker.us-south.websphereappsvr.cloud.ibm.com/wasaas-broker/api#/){: new_window} de {{site.data.keyword.Bluemix_notm}}.


## Acceso a Internet pública
{: #publicInternetAccess}

Si lo desea, puede gestionar el acceso a Internet pública desde el panel de control de servicios en la IU de {{site.data.keyword.Bluemix_notm}}. Puede **solicitar** una dirección IP pública de la agrupación y **abrir** la conexión desde
Internet en su WebSphere Application Server en la instancia de servicio de {{site.data.keyword.Bluemix_notm}}. A la inversa, puede **cerrar** el acceso a Internet desde la instancia de servicio y **devolver** la dirección IP pública a la agrupación.

### Solicitar una dirección IP y abrir una conexión
{: #request-open-ip}

1. Pulse **Gestionar acceso a IP pública** en el panel de control de servicios de la consola de {{site.data.keyword.Bluemix_notm}}.
2. Se muestra la dirección IP del host, pero no la dirección IP pública. Pulse **Solicitar dirección IP pública**.

    Volverá al panel de control de servicios con una IP pública asignada. Sin embargo, se mostrará el mensaje siguiente:

    > _El acceso está cerrado actualmente. Pulse Gestionar IP pública para abrir el acceso._
3. Pulse **Gestionar acceso a IP pública** en el panel de control de servicios.
4. Se muestran las direcciones IP del host y la nueva IP pública, pero el acceso está cerrado. Pulse **Abrir acceso**.

    Volverá al panel de control de servicios, donde se mostrará el siguiente mensaje:

    > _El acceso está abierto actualmente. Pulse Gestionar IP pública para cerrar el acceso._

### Cerrar una conexión y volver a una dirección IP pública
{: #close-return-ip}

1. Pulse **Gestionar acceso a IP pública** en el panel de control de servicios.
2. Pulse **Cerrar acceso**.

    Volverá al panel de control de servicios, donde se mostrará el siguiente mensaje:

    > _El acceso está cerrado actualmente. Pulse Gestionar IP pública para abrir el acceso._
3. Pulse **Gestionar acceso a IP pública** en el panel de control de servicios de la IU de {{site.data.keyword.Bluemix_notm}}.
4. Pulse **Devolver dirección IP pública**.

    Volverá al panel de control de servicios, donde se mostrará la dirección IP del host con el siguiente mensaje:

    > _Se ha devuelto la IP pública._

## Puertos IP públicos
{: #publicIPports}

Cuando abre el acceso a IP pública, la dirección IP se asocia a VM y se abren los puertos 80 y 443 en la pasarela. Sin embargo, de forma predeterminada, Liberty Core y los servidores WebSphere Base tradicionales no abren los puertos 80 y 443. Por el contrario, los puertos 80 y 443 se abren de forma predeterminada en IBM HTTP Server. Por lo tanto, es posible que tenga que configurar los servidores Liberty Core y WebSphere Base tradicional para el tráfico de las aplicaciones en el puerto 80 y 443 cuando utilice una IP pública.
* Para configurar el servidor Liberty Core, consulte [Configuración de Liberty Core Server para el acceso público](networkEnvironment.html#configureLibertyForPublicAccess).
* Para configurar el servidor WebSphere Base tradicional, añada una escucha de cadena de transporte de contenedor web en el puerto 80 y 443 tal como se describe en [Configuración de cadenas de transporte](http://www.ibm.com/support/knowledgecenter/SSEQTP_8.5.5//com.ibm.websphere.nd.doc/ae/trun_chain_transport.html){: new_window}.

**Evite problemas:** Linux reserva los puertos inferiores a 1024 para los usuarios con privilegios, como por ejemplo **root**. Sin embargo, es una práctica común ejecutar los servidores básicos de WebSphere Base como usuario **no root**. Por lo tanto, cuando añada una cadena de transporte de contenedor Web, cambie la configuración de **iptables** como usuario **root**. En concreto, redirija los puertos restringidos 80 y 443 a otro puerto por encima de 1024, como por ejemplo 9080 y 9443. Los mandatos siguientes contienen un ejemplo de este proceso:

```
-bash-4.1# sudo iptables -t nat -A PREROUTING -p tcp --dport 80 -j REDIRECT --to-port 9080
-bash-4.1# sudo iptables -I INPUT -p tcp -m tcp --dport 80 -j ACCEPT
-bash-4.1# sudo iptables -I INPUT -p tcp -m tcp --dport 9080 -j ACCEPT

-bash-4.1# sudo iptables -t nat -A PREROUTING -p tcp --dport 443 -j REDIRECT --to-port 9443
-bash-4.1# sudo iptables -I INPUT -p tcp -m tcp --dport 443 -j ACCEPT
-bash-4.1# sudo iptables -I INPUT -p tcp -m tcp --dport 9443 -j ACCEPT
```

**Nota:** los cambios en **iptables** son efímeros. Por ejemplo, si se reinicia el invitado o si se reinicia el servicio **iptables**, las reglas se desechan y se restablecen automáticamente. Para guardar las reglas de forma que se conserven cuando se inicie el servicio iptables o se reinicie el invitado, utilice el mandato siguiente como usuario **root**:

```
-bash-4.1# service iptables save
iptables: Saving firewall rules to /etc/sysconfig/iptables:[  OK  ]

bash-4.1# cat /etc/sysconfig/iptables
# Generated by iptables-save v1.4.7 on Wed May 31 19:44:11 2017
*nat
:PREROUTING ACCEPT [0:0]
:POSTROUTING ACCEPT [23:1706]
:OUTPUT ACCEPT [23:1706]
-A PREROUTING -p tcp -m tcp --dport 80 -j REDIRECT --to-ports 9080
-A PREROUTING -p tcp -m tcp --dport 443 -j REDIRECT --to-ports 9443
COMMIT
# Completed on Wed May 31 19:44:11 2017
# Generated by iptables-save v1.4.7 on Wed May 31 19:44:11 2017
*filter
:INPUT DROP [0:0]
:FORWARD DROP [0:0]
:OUTPUT DROP [0:0]
-A INPUT -p tcp -m tcp --dport 9443 -j ACCEPT
-A INPUT -p tcp -m tcp --dport 443 -j ACCEPT
-A INPUT -p tcp -m tcp --dport 9080 -j ACCEPT
-A INPUT -p tcp -m tcp --dport 80 -j ACCEPT

```


**Nota:** **iptables** se invocan en las solicitudes que se desplazan a través de la interfaz externa del invitado. **iptables** no procesa las solicitudes que se desplazan por el bucle de retorno local (127.0.0.1), por lo que los puertos de redirección, como se ha indicado anteriormente, no se invocarían sobre un bucle de retorno.

## Puertos IP privados VPN
{: #privateIPports}

Se establece conexión con la dirección IP privada de VM a través de la conexión VPN. Solo se puede acceder a Liberty Admin Center (9080, 9443), a la consola de administración de WebSphere tradicional (9060, 9043), a SSH (22) y a los puertos que no son 80 ni 443 a través de la conexión VPN, tal como se muestra en la Figura 1. Consulte los archivos **server.xml** e **ibm-web-bnd.xml** de ejemplo de Liberty Core para ver detalles sobre cómo separar Liberty Admin Center de los puertos de la aplicación.

**Evite problemas:** para los servidores Liberty Core y WebSphere Base tradicional, los puertos del cortafuegos están preconfigurados cuando se suministra VM. Sin embargo, para configuraciones de Network Deployment donde el gestor de despliegue o el controlador colectivo está situado junto a IBM HTTP Server, es posible que tenga que abrir los puertos en el cortafuegos. Consulte [Puertos del cortafuegos](systemAccess.html#firewall_ports) para ver detalles.

## Configuración de un servidor Liberty Core para un acceso de IP pública
{: #configureLibertyForPublicAccess}

Tiene que configurar Liberty Core de modo que escuche el tráfico de la aplicación en los puertos 80 y 443 cuando utilice IP pública.

De forma predeterminada, Liberty está configurado con Liberty Admin Center y las aplicaciones disponibles en el host virtual **default_host**, que está asociado a **defaultHttpEndpoint** en el puerto 9080 y 9443. Vuelva a configurar el servidor para separar Liberty Admin Center del host virtual de la aplicación y del punto final y haga que estén disponibles en distintos puertos.

El siguiente fragmento de código es un ejemplo de ajustes en la configuración de server.xml:

```    
    <!-- open port 9080/9443 for incoming http connections -->
    <httpEndpoint id="defaultHttpEndpoint"
        host="*"
        httpPort="9080"
        httpsPort="9443">
        <tcpOptions soReuseAddr="true"/>
    </httpEndpoint>

    <!-- define a new endpoint for public app traffic -->
    <httpEndpoint id="publicHttpEndpoint"
        host="*"
        httpPort="80"
        httpsPort="443">
        <tcpOptions soReuseAddr="true"/>
    </httpEndpoint>

    <!–- restrict default_host to vpn so the Liberty Admin Center is not public -->
    <virtualHost id="default_host" allowFromEndpointRef="defaultHttpEndpoint">
      <hostAlias>*:9080</hostAlias>
      <hostAlias>*:9443</hostAlias>
    </virtualHost>

    <virtualHost id="external_host">
      <hostAlias>*:80</hostAlias>
      <hostAlias>*:443</hostAlias>
    </virtualHost>
```
{: codeblock}

Ahora asocie la aplicación con el host virtual `external_host` incluyendo el siguiente fragmento de código en el archivo `WEB-INF/ibm-web-bnd.xml` de la aplicación:

```
    <?xml version="1.0" encoding="UTF-8"?>
    <web-bnd
        xmlns="http://websphere.ibm.com/xml/ns/javaee"
        xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
        xsi:schemaLocation="http://websphere.ibm.com/xml/ns/javaee
        http://websphere.ibm.com/xml/ns/javaee/ibm-web-bnd_1_0.xsd"
        version="1.0">

        <virtual-host name="external_host" />
    </web-bnd>
```
{: codeblock}

## Configuración de DNS
{: #dnsConfig}

Es importante tener en cuenta que WebSphere Application Server en las máquinas virtuales de {{site.data.keyword.Bluemix_notm}} se configura con dos aplicaciones de resolución de DNS. Las aplicaciones de resolución se configuran en el archivo **/etc/resolv.conf** en la VM. El servidor DNS primario es un servidor no acreditado que proporciona WebSphere Application Server en el servicio {{site.data.keyword.Bluemix_notm}}. El servidor DNS secundario es un servidor no acreditado que proporciona {{site.data.keyword.Bluemix_notm}}.

Le recomendamos que revise la configuración de DNS para ver si se ajusta a sus necesidades. Puede actualizar el archivo `/etc/resolv.conf`
para que haga referencia al servidor DNS que elija si los que proporciona IBM no cumplen con sus requisitos.

**Nota:** es posible que las VM de WebSphere Application Server en {{site.data.keyword.Bluemix_notm}} antiguas solo tengan un servidor DNS primario configurado en el archivo `/etc/resolv.conf`. Si desea una solución de alta disponibilidad, puede liberar la máquina virtual y suministrar una nueva o actualizar el archivo `/etc/resolv.conf` para añadir un servidor DNS secundario. El servidor DNS secundario puede ser su servidor DNS preferido o el que proporciona {{site.data.keyword.Bluemix_notm}} (10.0.80.11).


## Apertura de puertos para servidores nuevos en nodos personalizados
{: #serversOnCustom}

Cuando crea un servidor en un nodo personalizado, los puertos adicionales que necesita el servidor deben estar abiertos en el gestor de despliegue y en las VM del nodo personalizado antes de que inicie el servidor. Después de crear el servidor, pero antes de iniciarlo, abra los puertos ejecutando el script `openWASPorts.sh`.

 1. Inicie una sesión en cada gestor de despliegue y VM personalizada como usuario root.
 1. Ejecute el script `/opt/IBM/WebSphere/AppServer/virtual/bin/openWASPorts.sh` para abrir los puertos.

Después de ejecutar el script, puede iniciar el servidor desde la consola de administración del gestor de despliegue.
