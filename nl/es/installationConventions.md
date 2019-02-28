---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-15"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Convenios de instalación
{: #installation_conventions}

## Consejos de administración
{: admin_tips}

Cuando esté administrando el entorno {{site.data.keyword.appserver_full}} y tenga que determinar el usuario que debe utilizar, es importante que comprenda los siguientes conceptos:

 * El mantenimiento se puede aplicar mediante el [gestor de instalación](http://www.ibm.com/support/knowledgecenter/SSDV2W_1.8.5/){: new_window} que está instalado en el directorio `/home/virtuser/IBM/Installation Manager`. Dado que los archivos binarios subyacentes se han instalado como `virtuser`, un usuario virtual administrativo limitado, asegúrese de que todos los fixpacks y arreglos temporales se instalen como `virtuser`.

 * Sin embargo, cuando inicie y detenga servidores desde la línea de mandatos, asegúrese de utilizar `wsadmin`, el ID de administración de WebSphere, no `virtuser`.

## Convenios de instalación de células
{: cell_installation_conventions}

Una célula de WebSphere Application Server en {{site.data.keyword.Bluemix_notm}} se instala y se configura siguiendo una estructura de directorios estandarizada. En la lista siguiente se indican algunos de los valores importantes.  Vea `/etc/virtualimage.properties` para obtener una lista completa de valores.

* IHS_HOME=/opt/IBM/WebSphere/HTTPServer
* IHS_INSTALL_ROOT=/opt/IBM/WebSphere/HTTPServer
* PLG_HOME=/opt/IBM/WebSphere/Plugins
* PROFILES_HOME=/opt/IBM/WebSphere/Profiles
* WAS_HOME=/opt/IBM/WebSphere/AppServer
* WAS_INSTALL_ROOT=/opt/IBM/WebSphere/AppServer
* WCT_HOME=/opt/IBM/WebSphere/Toolbox

## Convenios de instalación del colectivo de Liberty

Un colectivo de Liberty se instala y se configura siguiendo una estructura de directorios estandarizada. En la lista siguiente se indican algunos de los valores importantes.  Vea `/etc/virtualimage.properties` para obtener una lista completa de valores.

* IHS_HOME=/opt/IBM/WebSphere/HTTPServer
* IHS_INSTALL_ROOT=/opt/IBM/WebSphere/HTTPServer
* PLG_HOME=/opt/IBM/WebSphere/Plugins
* PROFILES_HOME=/opt/IBM/WebSphere/Profiles
* WLP_HOME=/opt/IBM/WebSphere/Liberty
