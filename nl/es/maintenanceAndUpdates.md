---

copyright:
  years: 2017, 2018
lastupdated: "2018-12-13"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Actualización del entorno
{: #updating-your-environment}

## Estrategia de mantenimiento
{: #maintenance-strategy}

{{site.data.keyword.appserver_full}} se actualiza de forma periódica, lo que garantiza que las nuevas instancias de servicio se crean con los fixpacks y parches actuales. La nube ofrece de forma rápida y sencilla nuevas instancias de servicio para la gestión de middleware.

Puede crear un WebSphere Application Server en la instancia de {{site.data.keyword.Bluemix_notm}} en el nivel de fixpack actual o anterior (n o n-1) para una determinada versión del producto. Si se utiliza el fixpack actual, se proporcionan las actualizaciones y características más recientes, pero es posible que sea necesario el fixpack anterior para que se ajuste a los requisitos de un despliegue de nube híbrido.

Cuando crea una instancia nueva, puede elegir entre los siguientes niveles de fixpack en el separador **Perfil de servicio** de la instancia de servicio:

**Liberty**
  * 18.0.0.4
  * 18.0.0.3

**WebSphere Application Server tradicional**
  * 9.0.0.10
  * 9.0.0.9
  * 8.5.5.14
  * 8.5.5.13

## Aplicación de arreglos y actualizaciones de fixpack
{:#applying-fixes}

La forma más rápida de actualizar al nivel de mantenimiento más reciente consiste en crear una instancia nueva. Sin embargo, si prefiere conservar las instancias de servicio de larga duración, puede aplicar mantenimiento a la instalación existente ejecutando el script `installService.sh` proporcionado o utilizando el Gestor de instalación de IBM tal como se describe en las secciones siguientes.

### Actualización mediante el script installService.sh

La instancia de servicio se configura con un repositorio de Installation Manager que se actualiza con frecuencia con los arreglos de seguridad disponibles y los fixpacks de WebSphere Application Server. Puede utilizar el script `/home/virtuser/installService.sh` para aplicar estos arreglos y fixpacks. El script se debe ejecutar como usuario root.

La cantidad de espacio de disco que se necesita para instalar las actualizaciones varía en función de los tipos de actualizaciones que instale. Si solo se instalan los arreglos temporales, se necesita 1 GB de espacio libre en la máquina virtual. La instalación de fixpacks aumentada el espacio de disco necesario a 1,3 GB.

La ejecución del script lleva a cabo las acciones siguientes:

* Detiene todas las instancias de WebSphere Application Server y de IBM HTTP Server en ejecución
* Opcionalmente instala los fixpacks más recientes para Installation Manager, WebSphere Application Server, IBM HTTP Server y el SDK de Java&trade;
* Instala los arreglos temporales más recientes para WebSphere, IBM HTTP Server y el SDK de Java&trade;
* Reinicia todas las instancias

#### Opciones
* **`-fixpacks`**

    Actualiza todos los paquetes el fixpack más reciente.
* **`-noprompt`**

    No se solicita confirmación antes de actualizar.

#### Ejemplos de sintaxis

```
./installService.sh -?
```
{:.codeblock}

Muestra texto de ayuda.


```
./installService.sh
```
{:.codeblock}

Instala todos los arreglos temporales aplicables, pero no los fixpacks.


```
./installService.sh -fixpacks
```
{:.codeblock}

Instala todos los fixpacks disponibles y luego instala todos los arreglos temporales aplicables.

### Actualización mediante Installation Manager
{:#installation-manager}

[Installation Manager](http://www.ibm.com/support/knowledgecenter/SSDV2W_1.8.3/com.ibm.cic.agent.ui.doc/helpindex_imic.html){: new_window} se instala en el directorio `/home/virtuser/IBM/Installation Manager` y luego se puede ejecutar directamente para aplicar arreglos y fixpacks.

**Evite problemas:** puesto que los archivos binarios subyacentes se instalan como `virtuser`, un usuario virtual administrativo limitado, asegúrese de que Installation Manager siempre de ejecute como `virtuser`.

## Aplicación de actualizaciones del sistema a máquinas virtuales
{:#vm-system-updates}

La aplicación de actualizaciones del sistema en una máquina virtual es similar a la actualización de un sistema físico Red Hat Enterprise Linux&reg; (RHEL). Mediante el gestor de paquetes Yum, puede instalar, actualizar, desinstalar y realizar otras gestiones con paquetes. WebSphere Application Server en los sistemas {{site.data.keyword.Bluemix_notm}} se configura para recibir actualizaciones del servidor de Red Hat Satellite de IBM, que proporciona paquetes seguros de la red Red Hat. El servidor Satellite está gestionado por IBM y no se puede modificar desde su sistema.

Para obtener más información, consulte [Aplicación de actualizaciones de paquetes en Red Hat Enterprise Linux](https://access.redhat.com/articles/11258#rhel6){: new_window} e [Yum, el gestor de paquetes de Red Hat](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/6/html/Deployment_Guide/ch-yum.html){: new_window}.
