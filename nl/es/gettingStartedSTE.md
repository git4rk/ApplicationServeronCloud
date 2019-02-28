---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-15"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Entornos de un solo arrendatario
{: #getting_startedSTE}

El entorno de un solo arrendatario de {{site.data.keyword.appserver_full}} ofrece a los clientes con una carga de trabajo de WebSphere aislada un entorno híbrido completamente integrado y datos seguros. Esta guía de iniciación se ha diseñado para identificar los elementos clave que le ayudan a acceder y a gestionar su entorno de un solo arrendatario.
{: shortdesc}

## Solicitud de un entorno de un solo arrendatario
{:#ordering}

Los entornos de un único arrendatario no se pueden crear a través del catálogo {{site.data.keyword.Bluemix_notm}} y deben solicitarse poniéndose en contacto con el departamento de ventas de IBM. Cuando pida su entorno, puede elegir entre un entorno de un solo arrendatario estándar o con su propia licencia. Los entornos estándar de un solo arrendatario incluyen toda la infraestructura necesaria y las licencias de WebSphere Application Server. En los entornos de un solo arrendatario de tipo BYOL (traer su propia licencia), puede utilizar licencias independientes de WebSphere Application Server.

Para pedir un entorno de un solo arrendatario, [póngase en contacto con el equipo de ventas de IBM](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#contacting-sales). El equipo de ventas puede ayudarle a configurar un entorno ajustado a sus necesidades.

## Visión general de WebSphere Application Server en el entorno de un solo arrendatario de {{site.data.keyword.Bluemix_notm}}
{: #overviewSTE}

En el entorno de un solo arrendatario dispone de su propia instancia del servicio, su red privada y recursos aislados. Aunque la oferta se gestiona de forma independiente, se puede acceder al servicio y a los paneles de control de instancia de servicio creada a través de una región pública específica de {{site.data.keyword.Bluemix_notm}}, tal como se muestra en la figura siguiente.

Figura 1. Arquitectura de WebSphere Application Server en el entorno de un solo arrendatario de {{site.data.keyword.Bluemix_notm}}

![Figura 1. Arquitectura del entorno de un solo arrendatario](images/WASaaS.png)


## Gestión de la organización
{: #organization_management}

El entorno de un solo arrendatario de WebSphere Application Server en {{site.data.keyword.Bluemix_notm}} se configura según su pedido. Si ha proporcionado uno o varios nombres de organización de {{site.data.keyword.Bluemix_notm}} como parte del pedido, ya puede empezar a acceder al entorno. Si no ha especificado ningún nombre de organización o si desea cambiar este valor, abra una [incidencia de soporte](/docs/services/ApplicationServeronCloud?topic=wasaas-reporting_issues#reporting_issues) para **servicios de aplicación** desde la consola de {{site.data.keyword.Bluemix_notm}} de su región. Encontrará el nombre de su organización en la consola de {{site.data.keyword.Bluemix_notm}}, en **Gestionar > Cuenta > Organizaciones de Cloud Foundry**.

**Nota:** para acceder a su entorno de un solo arrendatario, consulte [Acceso a un entorno de un solo arrendatario](/docs/services/ApplicationServeronCloud?topic=wasaas-singleTenantEnvironment#singleTenantEnvironment).
