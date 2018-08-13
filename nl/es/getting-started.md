---

copyright:
  years: 2018
lastupdated: "2018-06-08"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}


# Guía de aprendizaje de iniciación
{:#getting-started}

Con {{site.data.keyword.appserver_full}}, puede configurar un entorno tradicional o Liberty de WebSphere Application Server preconfigurado en cuestión de minutos. Esta guía de aprendizaje de iniciación le guiará a través del proceso de suministro de un entorno de WebSphere Application Server en una máquina virtual con unos pocos pasos.
{: shortdesc}

## Antes de empezar
{: #prereqs}

Si desea un entorno con recursos de máquina virtual más dedicados, como un contrato de reserva o un entorno de un solo arrendatario, tendrá que ponerse en contacto con el equipo de ventas de IBM antes de crear el servicio. Obtenga más información sobre estas opciones en la sección [Acerca de](index.html).

## Paso 1: Crear el servicio
{: #create}

1. Vaya a la página [{{site.data.keyword.appserver_short}}](https://console.bluemix.net/catalog/services/websphere-application-server) del catálogo de {{site.data.keyword.cloud_notm}}.
1. Inicie una sesión con su IBMid, o regístrese para una cuenta de {{site.data.keyword.cloud_notm}}.
1. En la página del catálogo, revise las selecciones correspondientes a la configuración del servicio.

  En el caso de entornos de pago según uso, utilice las selecciones predeterminadas o modifíquelas para que se ajusten a sus necesidades. Si tiene un contrato de reserva o un entorno de un solo arrendatario, preste especial atención a las opciones siguientes.

  * **Contrato de reserva:** en **Elegir una región/ubicación de despliegue**, verifique que la región seleccionada es la región correcta para el contrato.

  * **Entorno de un solo arrendatario: ** en **Elegir una región/ubicación de despliegue**, compruebe que la región seleccionada es la región en la que está desplegado su entorno de un solo arrendatario. En **Entorno**, seleccione su entorno de un solo arrendatario. De forma predeterminada, es posible que se muestre el entorno público.

    Si no ve en la lista su entorno de un solo arrendatario, compruebe que está en la región correcta y que su organización tiene acceso a su entorno de un solo arrendatario.
    {: tip}
1. Seleccione el plan de precios correspondiente a la edición de {{site.data.keyword.appserver_short}} que desea desplegar.
1. Pulse **Crear**.


## Paso 2: Elegir el entorno
{: #choose_env}

Los planes básico y Liberty Core de {{site.data.keyword.appserver_short}} solo tienen servidores únicos; si elige estos planes, puede saltarse este paso.

Para el plan de despliegue de red, seleccione el perfil y la arquitectura para el entorno.

* **Perfil:** elija {{site.data.keyword.appserver_short}} tradicional o Liberty
* **Arquitectura:** elija un entorno de un solo servidor o un entorno en clúster con las células tradicionales o los colectivos de Liberty


## Paso 3: Seleccionar el tamaño de las máquinas virtuales
{: #vm_sizing}

Puede seleccionar el tamaño de la máquina virtual individualmente para cada componente del entorno. El tamaño de la máquina virtual se fragmenta en [tamaños de camiseta](index.html#vm-size) de bloques de recursos.

Pulse el separador correspondiente al componente, como el servidor, el gestor de despliegue o el nodo de aplicación, y seleccione el tamaño de camiseta para su máquina virtual.

## Paso 4: Suministrar el entorno
{: #service_profile}

Revise los detalles del resumen de la configuración del servicio, incluido el tiempo estimado que tardará en suministrarse. Pulse **Suministrar** para configurar el entorno de {{site.data.keyword.appserver_short}}.

## Pasos siguientes
{: #anchor_value}

Obtenga información sobre cómo acceder y gestionar el nuevo entorno de {{site.data.keyword.appserver_short}} en la sección [Acceso al sistema](systemAccess.html).