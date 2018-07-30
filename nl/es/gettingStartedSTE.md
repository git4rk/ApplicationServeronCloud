---

copyright:
  years: 2017, 2018
lastupdated: "2018-06-08"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Entornos de un solo arrendatario
{: #getting_startedSTE}

El entorno de un solo arrendatario de {{site.data.keyword.appserver_full}} es una oferta que ofrece a los clientes con una carga de trabajo de WebSphere aislada un entorno híbrido completamente integrado y datos seguros. Esta guía de iniciación se ha diseñado para identificar los elementos clave que ayudan a los clientes a acceder y a gestionar su WebSphere Application Server en un entorno de {{site.data.keyword.Bluemix_notm}} de un solo arrendatario.
{: shortdesc}


## Software recomendado
{: #recommended_software}

Necesita el software siguiente para acceder a su entorno de un solo arrendatario:
* Un navegador web que reciba soporte de {{site.data.keyword.Bluemix_notm}}:
    * Chrome: la versión más reciente para su sistema operativo
    * Firefox: la versión más reciente para su sistema operativo o la última versión de ESR
    * Internet Explorer: versión 10 u 11
    * Safari: la versión más reciente para Mac
* La interfaz de línea de mandatos de Cloud Foundry, Versión 6.5.1 o posterior (puede utilizar el release más reciente)
* Git Bash (recomendado)
    * Descargue e instale [Git Bash](https://git-scm.com/downloads){: new_window}


## Visión general de WebSphere Application Server en {{site.data.keyword.Bluemix_notm}}: entorno de un solo arrendatario
{: #overviewSTE}

WebSphere Application Server en {{site.data.keyword.Bluemix_notm}}: la oferta de un solo arrendatario único proporciona a los consumidores su propia instancia privada del servicio, servicios de red y recursos aislados. Aunque la oferta se gestiona de forma independiente, se puede acceder al servicio y a los paneles de control de instancia de servicio creada a través de una región pública específica de {{site.data.keyword.Bluemix_notm}}, tal como se muestra en la figura siguiente:

Figura 1. Arquitectura de WebSphere Application Server en {{site.data.keyword.Bluemix_notm}}: entorno de un solo arrendatario

![Figura 1. Arquitectura de un entorno de un solo arrendatario](images/WASaaS.png)


## Gestión de la organización
{: #organization_management}

El entorno de un solo arrendatario de WebSphere Application Server en {{site.data.keyword.Bluemix_notm}} se configura según su pedido. Si ha proporcionado uno o varios nombres de organización de {{site.data.keyword.Bluemix_notm}} como parte del pedido, ya puede empezar a acceder al entorno. Si no ha especificado uno o varios nombres de organización o si desea cambiar este valor, abra una [incidencia de soporte](reportingIssues.html#reporting_issues) para **servicios de aplicación** desde la consola de {{site.data.keyword.Bluemix_notm}} de su región. Encontrará el nombre de la organización (ORG) en la esquina superior derecha de la consola de {{site.data.keyword.Bluemix_notm}}, tal como se muestra en la siguiente figura:

Figura 2. Ubicación del nombre de la organización

![Figura 2. Ubicación del nombre de la organización](images/myORG.png)


**Nota:** para acceder a su entorno de un solo arrendatario, consulte [Acceso a un entorno de un solo arrendatario](singleTenantAccess.html#singleTenantEnvironment).
